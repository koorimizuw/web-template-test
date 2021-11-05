<template>
  <section class="section home-acc">
    <div class="container">
      <div class="flex flex-wide">
        <div class="home-acc-left">
          <h2>
            Made for small and mid-size businesses that want to save time and
            grow.
          </h2>
          <p>
            Beez bundles are created to meet various businesses needs – from
            most simple and budget friendly, to those that are highly complex
            and demanding.
          </p>
        </div>
        <!-- home-acc-left -->
        <div class="home-acc-right">
          <ul
            uk-accordion="multiple: true; duration:400;transition:ease;"
            class="uk-accordion"
          >
            <li>
              <div class="uk-accordion-title">
                <h3><span>It is simple, yet impactful.</span></h3>
                <span class="acc-btn"></span>
              </div>
              <div class="uk-accordion-content" aria-hidden="true"></div>
            </li>

            <li>
              <div class="uk-accordion-title">
                <h3>
                  <span>Integration is fast. Within weeks, not months.</span>
                </h3>
                <span class="acc-btn"></span>
              </div>
              <div class="uk-accordion-content" aria-hidden="true"></div>
            </li>

            <li>
              <div class="uk-accordion-title">
                <h3><span>It’s customizable. And agile.</span></h3>
                <span class="acc-btn"></span>
              </div>
              <div class="uk-accordion-content" aria-hidden="true"></div>
            </li>

            <li>
              <div class="uk-accordion-title">
                <h3><span>It’s safe and reliable.</span></h3>
                <span class="acc-btn"></span>
              </div>
              <div class="uk-accordion-content" aria-hidden="true"></div>
            </li>

            <li>
              <div class="uk-accordion-title">
                <h3><span>It is affordable.</span></h3>
                <span class="acc-btn"></span>
              </div>
              <div class="uk-accordion-content" aria-hidden="true"></div>
            </li>
          </ul>
          <a href="https://beez.ba/why-choose-beez-now/" class="link-off-acc">
            <div class="acc-off">
              <img
                alt=""
                data-src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/strelicaSvg.svg"
                class="lazyloaded"
                src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/strelicaSvg.svg"
              /><noscript
                ><img
                  src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/strelicaSvg.svg"
                  alt=""
              /></noscript>
              <h3><span>Learn more why Beez is good for you</span></h3>
            </div>
          </a>
        </div>
        <!-- home-acc-right -->
      </div>
      <!-- flex -->
    </div>
  </section>
</template>

<style lang="scss" scoped>
.home-acc-left {
  width: 47%;
}
.home-acc-left p {
  width: 55%;
  font-size: 20px;
  font-size: var(--p-second);
}
.home-acc-right {
  width: 50%;
  margin-top: 230px;
}
.home-acc-right li {
  position: relative;
}
.home-acc-right .uk-accordion-title {
  padding-top: 15px;
}
.home-acc-right .uk-accordion-title h3 {
  margin-bottom: 20px;
  margin-left: 100px;
  font-size: 28px;
}
.home-acc-right .uk-accordion-title h3 > span {
  font-family: "Galano", sans-serif;
  color: var(--black);
  background-image: linear-gradient(180deg, transparent 50%, #fcf113 0);

  background-size: 0 100%;
  background-repeat: no-repeat;
  text-decoration: none;
  transition: background-size 0.4s ease;
}

.acc-off {
  position: relative;
  padding-top: 15px;
}
.acc-off img {
  width: 60px;
  position: absolute;
  top: 2px;
}
.home-acc-right .link-off-acc {
  display: block;
  margin-top: 20px;
  text-decoration: none;
}
.home-acc-right .link-off-acc h3 {
  margin-bottom: 20px;
  margin-left: 100px;
  font-size: 28px;
}
.home-acc-right .link-off-acc h3 > span {
  font-family: "Galano", sans-serif;
  color: var(--black);
  background-image: linear-gradient(180deg, transparent 50%, #fcf113 0);

  background-size: 0 100%;
  background-repeat: no-repeat;
  text-decoration: none;
  transition: background-size 0.4s ease;
}
.home-acc-right .uk-accordion-title:hover span,
.home-acc-right .link-off-acc:hover span {
  background-size: 100% 100%;
  cursor: pointer;
}
.home-acc-right .uk-accordion-title::before {
  display: none;
}
.home-acc-right .acc-btn {
  left: 0;
  top: 2px;
}
.home-acc-right .uk-open > .uk-accordion-title::before {
  display: none;
}
.home-acc-right .uk-accordion-content {
  padding-left: 120px;
}

span.acc-btn {
  width: 60px !important;
  height: 60px;
  border-radius: 50%;
  background: var(--black);
  position: absolute;
  right: 0;
  top: 14px;
}
.accordion-head span.acc-btn {
  position: relative;
  display: block;
  float: right;
  top: unset;
  margin: auto 0;
}
span.acc-btn::before {
  content: "";
  width: 20px;
  height: 4px;
  background: #fff;
  top: 28px;
  position: absolute;
  left: 20px;
  transform: rotate(0deg);
  transition: 0.4s all ease-in-out;
}
span.acc-btn::after {
  content: "";
  width: 20px;
  height: 4px;
  background: #fff;
  top: 28px;
  position: absolute;
  left: 20px;
  transform: rotate(90deg);
  transition: 0.4s all ease-in-out;
  opacity: 1;
}

.acc-btn2 {
  width: clamp(36px, 3.12vw, 58px) !important;
  height: clamp(36px, 3.12vw, 58px);
  border-radius: 50%;
  border: 1px solid #fff;
  background: var(--white);
  position: absolute;
  right: 0;
  top: clamp(10px, 1.6vw, 20px);
  cursor: pointer;
}
.acc-btn2:hover {
  background: transparent;
}
.acc-btn2::before {
  content: "";
  width: clamp(16px, 1.04vw, 20px);
  height: 4px;
  background: var(--black);
  top: clamp(15px, 1.44vw, 28px);
  position: absolute;
  left: clamp(10px, 1vw, 19px);
  transform: rotate(0deg);
  transition: 0.4s all ease-in-out;
}
.acc-btn2::after {
  content: "";
  width: clamp(16px, 1.04vw, 20px);
  height: 4px;
  background: var(--black);
  top: clamp(15px, 1.44vw, 28px);
  position: absolute;
  left: clamp(10px, 1vw, 19px);
  transform: rotate(90deg);
  transition: 0.4s all ease-in-out;
  opacity: 1;
}
.acc-btn2:hover::after {
  background: #fff;
}
.acc-btn2:hover::before {
  background: #fff;
}

h3 {
  margin-top: 0;
}
</style>