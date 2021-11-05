<template>
  <footer>
    <div class="container">
      <div class="footer-logo">
        <a href="/"
          ><img
            alt="logo"
            data-src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/Logo.png"
            class="ls-is-cached lazyloaded"
            src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/Logo.png" /><noscript
            ><img
              src="https://beez.ba/wp-content/themes/wpog_beez/assets/img/Logo.png"
              alt="logo" /></noscript
        ></a>
        <p>busy made easy</p>
      </div>
      <!-- footer-logo -->
      <div class="grid footer-grid">
        <div class="footer-links">
          <h3><a href="https://beez.ba/beez-office/">Beez Office</a></h3>
          <h3><a href="https://beez.ba/beez-business/">Beez Business</a></h3>
          <h3>
            <a href="https://beez.ba/beez-enterprise/">Beez Enterprise</a>
          </h3>
        </div>
        <!-- footer-links -->

        <div class="footer-links">
          <h3><a href="https://beez.ba/why-choose-beez-now/">Why Beez</a></h3>
          <h3><a href="https://beez.ba/services/">Services</a></h3>
          <h3><a href="https://beez.ba/our-company/">Company</a></h3>
        </div>
        <!-- footer-links -->

        <div class="footer-links">
          <h3><a href="https://beez.ba/request-demo/">Request demo</a></h3>
          <h3><a href="https://beez.ba/contact-us/">Get in touch</a></h3>
          <h3><a href="tel: +387 65 693 073"> +387 65 693 073</a></h3>
        </div>
        <!-- footer-links -->
      </div>
      <!-- grid -->
      <div class="footer-copyright">
        <p>
          © 2021 beez Limited. All rights reserved. “beez” and “busy made easy“
          are trademarks of KKLAS.
        </p>
        <p>
          <a href="https://beez.ba/legal">Legal</a>&nbsp;<a
            href="https://beez.ba/privacy-notice/"
            >Privacy notice</a
          >
        </p>
      </div>
      <!-- footer-copyright -->
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  padding: var(--padding50) 0 var(--padding150);
}
.footer-logo {
  margin-bottom: 70px;
}
.footer-logo img {
  display: inline-block;
  margin-bottom: -2px;
}
.footer-logo p {
  display: inline-block;
  font-size: 14px;
  margin-left: 28px;
}
.footer-grid {
  width: 100%;
}
.footer-links h3 {
  font-size: var(--link-mid-font);
  line-height: 1;
  margin-bottom: 20px;
}
.footer-links h3 a {
  border-bottom: 1px solid var(--black);
  width: fit-content;
  background-image: linear-gradient(180deg, transparent 50%, #fcf113 0);
  background-size: 0 100%;
  background-repeat: no-repeat;
  text-decoration: none;
  transition: background-size 0.4s ease;
  cursor: pointer;
  font-family: "Galano", sans-serif;
}

.footer-links a:hover {
  background-size: 100% 100%;
  text-decoration: none;
}
.footer-links a:hover:active {
  background-size: 100% 100%;
  text-decoration: none;
}
.footer-copyright {
  width: 20%;
  margin-top: 100px;
  margin-left: auto;
  margin-right: calc(12% + 20px);
}
.footer-copyright p {
  font-size: 14px;
}
.footer-copyright a {
  font-size: 14px;
  text-decoration: underline;
  margin-right: 5px;
}

.grid {
  display: inline-grid;
  grid-template-columns: 1fr 1fr 1fr;
}

a,
a:hover,
a:focus {
  text-decoration: none;
  color: #242424;
}
</style>