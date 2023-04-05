
<template>
  <header>
    <navbar-view>
    </navbar-view>
  </header>
  <section class="position-relative">
    <div class="hero-bg">
      <!-- <div class="container"> -->
      <hero-view></hero-view>
      <!-- </div> -->
    </div>
  </section>
  <div class="d-flex justify-content-center">
    <div class="position-absolute scrolldown-btn"><i class="fa-solid fa-arrow-down fa-lg"></i></div>
  </div>
  <section id="about">
    <div class="about-bg">
      <!-- <div class="container"> -->
      <about-view></about-view>
      <!-- </div> -->
    </div>
  </section>
  <section id="services">
    <!-- <div class="container"> -->
    <services-view></services-view>
    <!-- </div> -->
  </section>
  <section id="contact">
    <div class="contact-bg">
      <!-- <div class="container"> -->
      <contact-view :contactButton="contactButtonData"></contact-view>
      <!-- </div> -->
    </div>
  </section>
  <footer>
    <div class="footer-bg">
      <!-- <div class="container"> -->
      <footer-view></footer-view>
      <!-- </div> -->
    </div>
  </footer>
</template>

<style lang="scss">
.hero-bg {
  // background-color: var(--bs-primary-color);
  background-image: linear-gradient(var(--bs-primary-color), var(--bs-about-color));
  // background-image: linear-gradient(var(--bs-primary-color), white);
}

.about-bg {
  background-color: var(--bs-about-color);
}

#services {
  margin-top: 150px;
  margin-bottom: 100px !important;
}

.contact-bg {
  background-color: var(--bs-lighter-primary-color);
  padding: 120px 0px;
}

.footer-bg {
  background-color: var(--bs-primary-color);
  padding: 70px 0px 0px;
}

.scrolldown-btn {
  background-color: var(--bs-secondary-color);
  border-radius: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  top: 90%;
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
    color: var(--bs-light-color);
  }
}

@media (max-width: 767.98px) {
  .scrolldown-btn {
    top: 725px !important;
  }

  .contact-bg {
    padding: 100px 0px;
  }
}

@media (max-width: 991.98px) {
  .scrolldown-btn {
    top: 1025px;
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
  },
  setup() {
    const contactButtonData: any = [
      {
        "id": 0,
        "buttonName": "fa-solid fa-location-dot",
        "buttonDetail": "asa"
      },
      {
        "id": 1,
        "buttonName": "fa-brands fa-whatsapp",
        "buttonDetail": "+62 819-3628-1299"
      },
      {
        "id": 2,
        "buttonName": "fa-brands fa-instagram",
        "buttonDetail": "i_g"
      },
      {
        "id": 3,
        "buttonName": "fa-regular fa-envelope",
        "buttonDetail": "mail"
      }
    ]

    return {
      contactButtonData
    }
  }
});

</script>
