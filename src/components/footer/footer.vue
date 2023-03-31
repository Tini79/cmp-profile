<template>
  <div class="section footer-section row justify-content-between">
    <div class="col-4">
      <div class="d-flex align-items-center mb-1">
        <img src="../../assets/img/hero-img.png" alt="" class="footer-img">
        <strong class="company-name">Shoshin Media</strong>
      </div>
      <!-- <div class="divider"></div> -->
      <p class="footer-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
        incididunt ut labore
        et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat.</p>
    </div>
    <div class="col-5 row justify-content-end">
      <div class="col-5">
        <strong>Sitemap</strong>
        <div class="divider footer"></div>
        <ul>
          <li>Home</li>
          <li>About</li>
          <li>Services</li>
          <li>Contact</li>
        </ul>
      </div>
      <div class="col-5">
        <strong>Services</strong>
        <div class="divider footer"></div>
        <ul>
          <li>Website Development</li>
          <li>System Development</li>
          <li>Graphic Design</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="copyright-container" style="color:#fff">
    <span>Copyright © 2024 <a href="">Shoshin Media</a> | All Rights reserved</span>
  </div>
</template>
<style scoped lang="scss" src="./footer.scss"></style>
<script lang="ts">
export default {
  name: "HeroView",

}
</script>