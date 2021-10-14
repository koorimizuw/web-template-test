<template>
  <canvas class="gl" />
</template>

<script setup lang="ts">
import { Fragment, onMounted } from "vue";

const interpolate = (
  templateString: TemplateStringsArray,
  ...args: string[]
) => {
  return (
    templateString[0] +
    args
      .map((arg, i) => {
        const next = templateString[1 + i];
        return arg + (next ? next : "");
      })
      .join("")
  );
};

function drawTriangele() {
  // 1. canvas
  const canvas = document.querySelector<HTMLCanvasElement>(".gl");
  if (!canvas) return;
  const gl = canvas.getContext("webgl");
  if (!gl) return;

  const createProgram = (
    vertexShader: WebGLShader,
    fragmentShader: WebGLShader
  ) => {
    const program = gl.createProgram() as WebGLProgram;
    gl.attachShader(program, vertexShader);
    gl.attachShader(program, fragmentShader);
    gl.linkProgram(program);
    const success = gl.getProgramParameter(program, gl.LINK_STATUS);
    if (success) {
      return program;
    }
    gl.deleteProgram(program);
    throw new Error("cannot create program");
  };

  const createShader = (type: number, source: string) => {
    const shader = gl.createShader(type) as WebGLShader;
    gl.shaderSource(shader, source);
    gl.compileShader(shader);
    const success = gl.getShaderParameter(shader, gl.COMPILE_STATUS);
    if (success) {
      return shader;
    }
    console.log(gl.getShaderInfoLog(shader));
    gl.deleteShader(shader);
    throw new Error("cannot create shader");
  };

  const vert = (templateString: TemplateStringsArray, ...args: string[]) => {
    const code = interpolate(templateString, ...args);
    return createShader(gl.VERTEX_SHADER, code);
  };
  const frag = (templateString: TemplateStringsArray, ...args: string[]) => {
    const code = interpolate(templateString, ...args);
    return createShader(gl.FRAGMENT_SHADER, code);
  };

  // 2. positions
  const positions = [-1, -1, 0, 1, 1, -1];

  // 3. vertex shader
  const vertexShader = vert`
  attribute vec4 a_position;
  varying vec4 v_color;
  void main() {
      gl_Position = a_position;
      v_color = gl_Position + 0.5;
  }`;

  const fragmentShader = frag`
  precision mediump float;
  varying vec4 v_color;
  void main() {
      gl_FragColor = v_color;
  }`;

  // resize
  const resize = () => {
    const displayWidth = canvas.clientWidth;
    const displayHeight = canvas.clientHeight;
    canvas.width = displayWidth;
    canvas.height = displayHeight;
  };

  resize();
  window.onresize = resize;

  // create program
  const program = createProgram(vertexShader, fragmentShader);

  // send date to gpu
  const aPosition = gl.getAttribLocation(program, "a_position");
  const positionBuffer = gl.createBuffer();
  gl.bindBuffer(gl.ARRAY_BUFFER, positionBuffer);
  gl.bufferData(gl.ARRAY_BUFFER, new Float32Array(positions), gl.STATIC_DRAW);

  // use program
  gl.useProgram(program);
  gl.enableVertexAttribArray(aPosition);

  const size = 2;
  const type = gl.FLOAT;
  const normalize = false;
  const stride = 0;
  const offset = 0;
  gl.vertexAttribPointer(aPosition, size, type, normalize, stride, offset);

  const primitiveType = gl.TRIANGLES;
  const count = 3;
  gl.drawArrays(primitiveType, offset, count);
}

onMounted(() => {
  drawTriangele();
});
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>
