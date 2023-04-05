<template>
  <nav class="navbar navbar-expand-lg navbar-main">
    <a class="navbar-brand" href="#">Shoshin Media</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav"
      aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon-custom"><i class="fa-solid fa-bars"></i></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a href="/" class="nav-link active">Home</a>
        </li>
        <li class="nav-item">
          <!-- <RouterLink class="nav-link" to="#about">About</RouterLink> -->
          <a href="#about" class="nav-link">About</a>
        </li>
        <li class="nav-item">
          <a href="#services" class="nav-link">Services</a>
        </li>
        <!-- <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown"
            aria-haspopup="true" aria-expanded="false">Services</a>
          <div class="dropdown-menu" id="parentDropdownMenu" aria-labelledby="navbarDropdown">
            <div class="dropdown">
              <a class="dropdown-toggle dropdown-toggle-child dropdown-item" href="#" id="navbarDropdown2"
                role="button">Website Development</a>
              <div class="dropdown-menu-child d-none" id="childDropdownMenu" aria-labelledby="navbarDropdown2">
                <a class="dropdown-item" href="#">Company Profile Website</a>
                <a class="dropdown-item" href="#">Property Website</a>
                <a class="dropdown-item" href="#">Dealer Website</a>
                <a class="dropdown-item" href="#">Hospitality Website</a>
              </div>
            </div>
            <a class="dropdown-item" href="#">System Development</a>
            <a class="dropdown-item" href="#">Graphic Design</a>
          </div>
        </li> -->
        <li class="nav-item">
          <a href="#contact" class="nav-link">Contact</a>
        </li>
      </ul>
    </div>
  </nav>
</template>
<style lang="scss" src="./navbar.scss"></style>
<script lang="ts">
import { onBeforeMount, onMounted, onUpdated } from 'vue';
import { RouterLink, RouterView } from "vue-router";

export default {
  name: "NavbarView",
  components: { RouterLink },
  mounted() {
    const childDropdownMenu: any = document.getElementById('childDropdownMenu')
    const navbarDropdown2: any = document.getElementById('navbarDropdown2')

    navbarDropdown2.addEventListener('click', (event: any) => {
      childDropdownMenu.classList.contains('d-none') ? childDropdownMenu.classList.remove('d-none') : childDropdownMenu.classList.add('d-none')
      event.stopPropagation()
    })
  },
}
</script>