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
      <p class="contact-text">Tell us more about your problem or service that you need to enhance your business.</p>
      <div class="button-group d-flex">
        <div v-for="button in contactButton" :key="button.id">
          <a href="" class="btn contact-btn"><i :class="button.buttonName"></i></a>
          <div class="contact-detail">{{ button.buttonDetail }}</div>
        </div>
      </div>
    </div>
    <div class="col-lg-6 contact-form">
      <Form @submit.prevent="onValidation" :validation-schema="schema" @invalid-submit="onInvalidSubmit">
        <c-input label="Name" name="name" v-model="form.name"></c-input>
        <c-input label="Phone Number" name="phone_number" v-model="form.phone_number"></c-input>
        <c-input label="Email" name="email" v-model="form.email"></c-input>
        <c-textarea label="Message" id="message" name="message" v-model="form.message"></c-textarea>
        <div class="text-end">
          <button type="submit" @click="onSubmit" class="contact-form-btn main-btn">Send</button>
        </div>
      </Form>
    </div>
  </div>
</template>
<style scoped lang="scss" src="./contact.scss"></style>
<script setup lang="ts">
import { reactive, ref } from 'vue'
import * as Yup from 'yup'
import {Form} from 'vee-validate'
import CInput from '../input/input.vue'
import CTextarea from '../textarea/textarea.vue'

const props: any = defineProps({
  contactButton: Array
})
const form: any = reactive({
  name: '',
  phone_number: '',
  email: '',
  message: ''
})
let isInvalid: any = ref(false)
const formValidation: any = ref()
// TODO : MAKE THE VALIDATION WORK!!!
function onValidation(values: any) {
  // alert(JSON.stringify(values, null, 2));
}

function onSubmit() {
  // formValidation.$el.requestSubmit()
}

function onInvalidSubmit(values: any) {
  // make red input border
}

const schema = Yup.object().shape({
  name: Yup.string().required(),
  phone_number: Yup.string().matches(/^[0-9]+$/, 'phone number must be only digits').required().min(12, 'phone number can\'t be less than 12 digits').max(13, 'phone number can\'t be more than 13 digits'),
  email: Yup.string().email().required(),
  message: Yup.string().required()
})

</script>