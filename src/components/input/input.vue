<template>
  <div class="form-input-group">
    <div class="TextInput" :class="{ 'has-error': !!errorMessage, success: meta.valid }">
      <label :for="name" class="form-label">{{ label }} *</label>
      <input type="text" :id="name" :name="name" :value="inputValue" @input="handleChange" @blur="handleBlur"
        :class="{ 'form-control': true, 'contact-form-input': true, 'is-invalid': isInvalid }">
    </div>
    <span>{{ errorMessage }}</span>
  </div>
</template>
<script lang="ts">
import { useField } from 'vee-validate'
export default {
  name: "Input",
  props: {
    label: {
      type: String
    },
    name: {
      type: String,
      required: true
    },
    isInvalid: {
      type: Boolean
    },
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
  },
}
</script>