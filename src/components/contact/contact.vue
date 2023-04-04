<template>
  <div class="section contact-section row justify-content-between">
    <div class="d-flex justify-content-lg-end contact-title-field">
      <div class="col-lg-6 contact-title-container">
        <h2 class="contact-title">Get In Touch With Us</h2>
      </div>
    </div>
    <div class="col-lg-4">
      <strong class="contact-us">Contact Us</strong>
      <div class="divider"></div>
      <p class="contact-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
        labore
        et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat.</p>
      <div class="button-group d-flex">
        <div v-for="button in props.contactButton" :key="button.id">
          <a href="" class="btn contact-btn"><i :class="button.buttonName"></i></a>
          <div class="contact-detail">{{ button.buttonDetail }}</div>
        </div>
      </div>
    </div>
    <div class="col-lg-6 contact-form">
      <form action="">
        <div class="form-input-group">
          <label for="" class="form-label">Name</label>
          <input type="text" class="form-control contact-form-input">
        </div>
        <div class="form-input-group">
          <label for="" class="form-label">Phone Number</label>
          <input type="text" class="form-control contact-form-input">
        </div>
        <div class="form-input-group">
          <label for="" class="form-label">Email</label>
          <input type="email" class="form-control contact-form-input">
        </div>
        <div class="form-input-group">
          <label for="" class="form-label">Message</label>
          <textarea name="" id="" cols="30" rows="5" class="form-control contact-form-input"></textarea>
        </div>
        <div class="text-end">
          <button class="contact-form-btn main-btn">Send</button>
        </div>
      </form>
    </div>
  </div>
</template>
<style scoped lang="scss" src="./contact.scss"></style>
<script lang="ts">
export default {
  name: "ContactView",
  props: {
    contactButton: Array
  },
  setup(props: any) {
    return {
      props
    }
  }
}
</script>k