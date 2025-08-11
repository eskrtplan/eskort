<template>
<NuxtLink :to="to">
  <button
    :type="type"
    :class="[
      variant === 'Red' ? 'text-link' : '',
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
  to: {
    type: String,
    required: true
  },
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
    default: 'primary',
  },
  disabled: {
    type: Boolean,
    default: false,
  }
})
</script>
