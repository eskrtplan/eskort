<template>
  <NuxtLink :to="to">
    <button
    :type="type"
    :class="[
      variant === 'primary' ? 'baseBtn' : '',
      fullWidth ? 'w-full' : '',
    ]"
    :disabled="disabled"
  >
    <slot>{{ label }}</slot>
  </button>
  </NuxtLink>
</template>

<script setup>
defineProps({
  to: String,
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
  fullWidth: {
    type: Boolean,
    default: false,
  },
  disabled: {
    type: Boolean,
    default: false,
  }
})
</script>
