<template>
  <section class="section top-home">
    <div class="container">
      <div class="flex flex-wide">
        <div class="top-left">
          <h1>Teams, tasks and results. All in one place.</h1>
          <p>
            Business software to make the most of your company’s resources.
            Optimize your business operation, improve the workflow and
            accelerate efforts, while overseeing every step of the process.
            That’s Beez.
          </p>
          <a href="https://beez.ba/request-demo/">
            <button class="btn btn-black" data-text="Request demo">
              <span>Request demo</span>
            </button>
          </a>
          <p class="link-works">
            <img
              alt=""
              data-src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/play.svg"
              class="lazyloaded"
              src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/play.svg"
            /><noscript
              ><img
                src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/play.svg"
                alt="" /></noscript
            >See how it works
          </p>
        </div>
        <div class="top-right">IMAGE</div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.top-home .top-left h1 {
  margin-bottom: var(--margin60);
}
.top-left {
  width: 44%;
}
.top-left a {
  text-decoration: none;
}
.top-left p {
  width: 72%;
  margin-bottom: var(--margin60);
  font-size: var(--p-second);
}
.top-left .link-works {
  font-size: 17px;
  text-decoration: none;
  color: rgba(0, 0, 0, 0.8);
  font-family: "Galano", sans-serif;
  margin-left: var(--margin50);
  position: relative;
  top: 3px;
  display: inline;
  cursor: pointer;
}
.top-left .link-works img {
  position: relative;
  width: 40px;
  top: 14px;
  margin-right: 12px;
}
.top-right {
  width: 50%;
}
</style>