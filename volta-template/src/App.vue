<template>
  <header>
    <nav>
      <div class="logo">Logo</div>
      <ul class="navbar">
        <li v-for="nav in navs" :key="nav">{{ nav }}</li>
      </ul>
    </nav>
  </header>
  <div class="container">
    <h1>Title</h1>
    <h3>Subtitle and Subtitle and Subtitle</h3>
    <p>
      <button>Get Started -></button>
    </p>
    <div class="features">
      <div class="feature" v-for="feat in features" :key="feat.title">
        <div class="title">{{ feat.title }}</div>
        <div>{{ feat.content }}</div>
      </div>
    </div>
    <div class="content">
      <h2>Try it out!</h2>
      <div class="highlight">
        <code
          ><span class="c"># install Volta</span><br />
          curl https://get.volta.sh | bash<br /><br />
          <span class="c"># install Node</span><br />
          volta <span class="nb">install </span>node<br /><br />
          <span class="c"># start using Node</span><br />
          node
        </code>
      </div>
    </div>
  </div>
  <footer>
    <div class="footcontainer">
      <div>Built with ♥ by the Volta community ⚡</div>
      <div class="logos">
        Our sponsors:
        <div>Logo1</div>
        <div>Logo2</div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const navs = ["Home", "Guide", "Blog", "Other", "Github"];
const features = [
  {
    title: "⚡ Fast",
    content:
      "Install and run any JS tool quickly and seamlessly! Volta is built in Rust and ships as a snappy static binary.",
  },
  {
    title: "⚡ Reliable",
    content:
      "Ensure everyone in your project has the same tools—without interfering with their workflow.",
  },
  {
    title: "⚡ Universal",
    content:
      "No matter the package manager, Node runtime, or OS, one command is all you need: volta install.",
  },
];
</script>


<style lang="scss">
body {
  margin: 0;
  padding: 0;
}
.header {
  height: 57.6px;
}
nav {
  padding: 0 30px;
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #eaecef;
}
.logo {
  font-size: 1.2em;
  justify-items: center;
  line-height: 57.6px;
}
.navbar {
  display: flex;
  list-style: none;
  li {
    cursor: pointer;
  }
  li + li {
    margin-left: 30px;
  }
  @media (max-width: 480px) {
    display: none;
  }
}
.container {
  max-width: 960px;
  margin: 30px auto;
  h1 {
    margin: 20px auto;
    text-align: center;
    letter-spacing: 10px;
    font-size: 6em;
    width: 338px;
    height: 150px;
  }
  h3 {
    position: relative;
    top: -30px;
    font-size: 1.8em;
    text-align: center;
    font-weight: 100;
    color: #257a83;
  }
  p {
    text-align: center;
    button {
      display: inline-block;
      font-size: 1.2rem;
      color: #fff;
      font-weight: 500;
      background-color: #257a83;
      padding: 1rem 1.6rem;
      border-radius: 4px;
      border: none;
      transition: background-color 0.1s ease;
      box-sizing: border-box;
      border-bottom: 1px solid #051012;
      &:hover {
        background-color: #79bac1;
        border-bottom: 1px solid #2a7886;
      }
    }
  }
}
.features {
  margin-top: 40px;
  border-top: 1px solid #e2f0f1;
  display: flex;
  .feature + .feature {
    margin-left: 30px;
  }
  .feature {
    margin-top: 30px;
  }
  .title {
    color: #257a83;
    font-size: 1.3em;
    margin: 20px 0;
  }
  @media (max-width: 480px) {
    display: block;
    .feature {
      margin: 20px;
    }
  }
}
.content {
  h2 {
    font-size: 2em;
    font-weight: 500;
  }
  .highlight {
    border: 1px solid #262626;
    border-radius: 5px;
    background: #262626;
    color: #ffffff;
    padding: 20px;
    line-height: 1.2em;
    .c {
      color: #999;
    }
  }
  @media (max-width: 480px) {
    margin: 0 20px;
  }
}
footer {
  background: #257a83;
  border-top: 1px dotted #051012;
  color: white;
}
.footcontainer {
  max-width: 960px;
  display: flex;
  justify-content: space-between;
  margin: 4rem auto 0;
  padding: 5rem 2.5rem;
  .logos {
    div {
      font-size: 2em;
    }
  }
  @media (max-width: 480px) {
    display: block;
    .logos {
      margin-top: 50px;
    }
  }
}
</style>
