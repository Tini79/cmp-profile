<template>
  <div class="form-input-group">
    <label for="message" class="form-label">{{ label }} *</label>
    <textarea :id="id" cols="30" rows="5" :value="inputValue" @input="handleChange" :name="name"
      :class="{ 'form-control': true, 'contact-form-input': true, 'is-invalid': isInvalid }"></textarea>
  </div>
  <span>{{ errorMessage }}</span>
</template>

<script lang="ts">
import { useField } from 'vee-validate'
export default {
  name: "Input",
  props: {
    label: {
      type: String
    },
    id: {
      type: String
    },
    name: {
      type: String
    },
    isInvalid: {
      type: Boolean
    }
  },
  setup(props: any) {
    const {
      value: inputValue,
      errorMessage,
      handleBlur,
      handleChange,
      meta,
    } = useField(props.name, value => !!value, {
      initialValue: props.modelValue,
    })

    return {
      inputValue,
      errorMessage,
      handleBlur,
      handleChange,
      meta,
    }
  }
}
</script>