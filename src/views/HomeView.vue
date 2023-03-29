
<template>
  <header>
    <navbar-view>
    </navbar-view>
  </header>
  <section class="position-relative">
    <div class="hero-bg">
      <hero-view></hero-view>
    </div>
  </section>
  <div class="d-flex justify-content-center">
    <div class="position-absolute scrolldown-btn"><i class="fa-solid fa-arrow-down fa-lg"></i></div>
  </div>
  <section>
    <div class="about-bg">
      <about-view></about-view>
    </div>
  </section>
  <section>
    <services-view></services-view>
  </section>
  <section>
    <div class="contact-bg">
      <contact-view></contact-view>
    </div>
  </section>
  <footer>
    <div class="footer-bg">
      <footer-view></footer-view>
    </div>
  </footer>
</template>

<style lang="scss">
.hero-bg {
  background-color: var(--bs-primary-color);
}

.about-bg {
  background-color: var(--bs-about-color);
}

.contact-bg {
  background-color: var(--bs-darker-primary-color);
  padding: 120px 0px;
}

.footer-bg {
  background-color: var(--bs-primary-color);
  padding-top: 70px;
}

.scrolldown-btn {
  background-color: var(--bs-secondary-color);
  border-radius: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  top: 108%;
  height: 50px;
  width: 50px;
  box-shadow: 0px 0px 4px 0px var(--bs-secondary-color);
  color: var(--bs-about-color);

  i {
    color: var(--bs-about-color);
  }
}

.scrolldown-btn:hover {
  background-color: var(--bs-darker-secondary-color);
  box-shadow: none;

  i {
    color: var(--bs-light-text);
  }
}
</style>

<script lang="ts">
import { defineComponent } from "vue";
import NavbarView from "../components/navbar/navbar.vue";
import HeroView from "../components/hero/hero.vue"
import AboutView from "../components/about/about.vue"
import ServicesView from "../components/our-services/services.vue"
import ContactView from "../components/contact/contact.vue"
import FooterView from "../components/footer/footer.vue"

export default defineComponent({
  components: {
    "navbar-view": NavbarView,
    "hero-view": HeroView,
    "about-view": AboutView,
    "services-view": ServicesView,
    "contact-view": ContactView,
    "footer-view": FooterView,
  }
});

</script>
