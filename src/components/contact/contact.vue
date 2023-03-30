<template>
  <div class="section contact-section row justify-content-between">
    <div class="d-flex justify-content-end">
      <div class="col-6 contact-title-container">
        <h2 class="contact-title">Get In Touch With Us</h2>
      </div>
    </div>
    <div class="col-4">
      <strong>Lorem ipsum dolor</strong>
      <div class="divider"></div>
      <p class="contact-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
        et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat.</p>
      <div class="button-group">
        <button class="btn contact-btn"><i class="fa-solid fa-location-dot"></i></button>
        <button class="btn contact-btn"><i class="fa-brands fa-whatsapp"></i></button>
        <button class="btn contact-btn"><i class="fa-brands fa-instagram"></i></button>
        <button class="btn contact-btn"><i class="fa-regular fa-envelope"></i></button>
      </div>
    </div>
    <div class="col-6">
      <form action="">
        <div class="form-input-group">
          <label for="" class="form-label">Name</label>
          <input type="text" class="form-control">
        </div>
        <div class="form-input-group">
          <label for="" class="form-label">Phone Number</label>
          <input type="text" class="form-control">
        </div>
        <div class="form-input-group">
          <label for="" class="form-label">Email</label>
          <input type="email" class="form-control">
        </div>
        <div class="form-input-group">
          <label for="" class="form-label">Message</label>
          <textarea name="" id="" cols="30" rows="10" class="form-control"></textarea>
        </div>
        <div class="text-end">
          <button class="btn contact-form-btn">Send</button>
        </div>
      </form>
    </div>
  </div>
</template>
<style scoped lang="scss" src="./contact.scss"></style>
<script lang="ts">
export default {
  name: "ContactView",
}
</script>