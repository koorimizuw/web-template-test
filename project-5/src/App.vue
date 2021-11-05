<template>
  <Header />
  <Top />
  <Home />
  <Footer />
</template>

<script setup lang="ts">
import Header from "./components/Header.vue";
import Top from "./components/Top.vue";
import Home from "./components/Home.vue";
import Footer from "./components/Footer.vue";
</script>

<style lang="scss">
body {
  margin: 0;
  padding: 0;
}

:root {
  --black: rgba(0, 0, 0, 0.8);
  --white: #fff;
  --yellow: #fcf112;
  --p-main: clamp(16px, 0.94vw, 18px);
  --p-second: clamp(18px, 1.04vw, 20px);
  --p-third: clamp(14px, 0.83vw, 16px);
  --h1-: clamp(50px, 3.12vw, 60px);
  --h2-: clamp(42px, 2.6vw, 50px);
  --h3-: clamp(28px, 1.82vw, 30px);
  --h3-alter: clamp(22px, 1.3vw, 25px);
  --link-mid-font: clamp(30px, 1.56vw, 18px);
  --h-margin-bottom: clamp(20px, 2.6vw, 50px);
  --h-margin-bottom-second: clamp(15px, 1.56vw, 30px);
  --margin100: clamp(40px, 5.2vw, 100px);
  --margin50: clamp(20px, 2.6vw, 50px);
  --margin60: clamp(20px, 3.1vw, 60px);
  --margin150: clamp(35px, 7.8vw, 150px);
  --padding50: clamp(20px, 2.6vw, 50px);
  --padding100: clamp(40px, 5.2vw, 100px);
  --padding150: clamp(75px, 7.8vw, 150px);
}

p {
  font-family: "Galano", sans-serif;
  font-size: var(--p-main);
  margin-bottom: 20px;
  line-height: 1.75;
  font-weight: 400;
}

.container {
  max-width: 1678px;
  //max-height: 70px;
  margin-left: auto;
  margin-right: auto;
  @media (min-width: 960px) {
    padding-left: 40px;
    padding-right: 40px;
  }
  @media (min-width: 640px) {
    padding-left: 30px;
    padding-right: 30px;
  }
}

.section {
  border-bottom: 1px dashed rgba(0, 0, 0, 0.8);
  padding: var(--padding50) 0 var(--padding100);
  margin: var(--margin50) 0;
}

.flex {
  display: flex;
  flex-wrap: wrap;
  &.flex-wide {
    justify-content: space-between;
  }
}

h1 {
  font-size: clamp(50px, 3.12vw, 60px);
  font-family: "Galano", sans-serif;
  margin-bottom: clamp(20px, 2.6vw, 50px);
  color: #000;
  line-height: 1.2;
  font-weight: 500;
}

h2 {
  font-size: var(--h2-);
  font-family: "Galano", sans-serif;
  margin-bottom: var(--h-margin-bottom);
  color: var(--black);
  line-height: 1.2;
  font-weight: 500;
}

h3 {
  font-size: var(--h3-);
  font-family: "Galano", sans-serif;
  margin-bottom: var(--h-margin-bottom);
  color: var(--black);
  line-height: 1.2;
  font-weight: 500;
}

.uk-accordion {
  padding: 0;
  list-style: none;
}

.btn {
  font-family: "Galano", sans-serif;
  overflow: hidden;
  padding: 0;
  width: 200px;
  display: inline-block;
  padding: 20px;
  border: 1px solid var(--black);
  color: inherit;
  vertical-align: middle;
  position: relative;
  z-index: 1;
  -webkit-backface-visibility: hidden;
  letter-spacing: 2px;
  cursor: pointer;
  font-size: 17px;
  background: var(--black);
  font-weight: 500;
  line-height: 1.5;
  ::before {
    content: attr(data-text);
    position: absolute;
    padding: 8px 0 8px;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: var(--white);
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
  }
  span {
    /* font-family: 'Galano', sans-serif; */
    vertical-align: middle;
    position: absolute;
    width: 200px;
    left: 0;
    top: 0;
    padding: 8px 0 8px;
    color: #fff;
  }
  &:hover {
    &::before {
      -webkit-transform: translate3d(0, 0, 0);
      transform: translate3d(0, 0, 0);
    }
    span {
      -webkit-transform: translate3d(0, 100%, 0);
      transform: translate3d(0, 100%, 0);
    }
  }
}
</style>