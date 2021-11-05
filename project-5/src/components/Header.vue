<template>
  <header>
    <div class="header">
      <div class="container">
        <div class="flex flex-wide">
          <div class="logo">
            <a href="https://beez.ba/">
              <img
                class="lazyloaded"
                src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/Logo.svg"
              />
            </a>
          </div>
          <div class="header-msg">
            <p>
              <span class="yellow-link" id="openVideo">busy made easy</span>
            </p>
          </div>
          <div class="nav-holder">
            <img
              class="menu lazyloaded"
              src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/Hamburg.svg"
            />
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  padding: 25px 0;
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 50;
  background: #fff;
  transition: 0.1s all ease-in-out;
  margin-bottom: clamp(35px, 7.8vw, 150px);
  position: relative;
}

.logo {
  width: 30%;
  img {
    width: 140px;
  }
}

.menu {
  cursor: pointer;
  transition: 0.4s all ease;
}

.lazyloaded {
  opacity: 1;
  transition: opacity 400ms;
  transition-delay: 0ms;
}

.nav-holder {
  width: 30%;
  position: relative;
  text-align: right;
  padding-top: 25px;
}

.header-msg {
  width: 30%;
  padding-top: 25px;
  text-align: center;
}
</style>