<template>
  <div class="services-section section">
    <h2 class="text-center services-title">Our Services</h2>
    <div class="row justify-content-between services-cards">
      <div class="col-4 card service-card">
        <img src="../../assets/img/hero-img.png" alt="">
        <div class="overlay d-flex align-items-end">
          <div class="service-content">
            <strong>Web Development</strong>
            <div class="divider"></div>
            <p>Lorem ipsum dolor sit amet, consectetur adipscing elit.</p>
          </div>
        </div>
      </div>
      <div class="col-4 card service-card">
        <img src="../../assets/img/hero-img.png" alt="">
        <div class="overlay d-flex align-items-end">
          <div class="service-content">
            <strong>System Development</strong>
            <div class="divider"></div>
            <p>Lorem ipsum dolor sit amet, consectetur adipscing elit.</p>
          </div>
        </div>
      </div>
      <div class="col-4 card service-card">
        <img src="../../assets/img/hero-img.png" alt="">
        <div class="overlay d-flex align-items-end">
          <div class="service-content">
            <strong>Graphic Design</strong>
            <div class="divider"></div>
            <p>Lorem ipsum dolor sit amet, consectetur adipscing elit.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" src="./services.scss"></style>
<script lang="ts">
export default {
  name: "ServicesView",

}
</script>