<template>
  <button
    :type="type"
    :class="[
      variant === 'white' ? ['secondary-btn', 'sec-white'] : '',
      variant === 'gold' ? ['secondary-btn', 'sec-gold'] : '',
      variant === 'green' ? ['secondary-btn', 'sec-green'] : '',
      fullWidth ? 'w-full' : '',
    ]"
    :disabled="disabled"
  >
    <slot>{{ label }}</slot>
  </button>
</template>

<script setup>
defineProps({
  label: {
    type: String,
    default: 'Click me',
  },
  type: {
    type: String,
    default: 'button',
  },
  variant: {
    type: String,
    default: 'primary', // 'primary' | 'secondary' | 'danger'
  },
  disabled: {
    type: Boolean,
    default: false,
  }
})
</script>
