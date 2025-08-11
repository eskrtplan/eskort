<template>
<NuxtLink :to="to">
  <button
    :type="type"
    :class="[
      variant === 'small rounded button' ? ['rd-btn', 'small-rd'] : '',
      variant === 'large rounded button' ? ['rd-btn', 'large-rd'] : '',
      fullWidth ? 'w-full' : '',
    ]"
    :disabled="disabled"
  >
    <Icon :name="icon" v-if="icon" 
    class="rd-icon"
    />
    <div v-if="notification" class="not-dot"></div>
  </button>
</NuxtLink>

</template>

<script setup>
defineProps({
  to: {
    type: String,
    required: true
  },
  type: {
    type: String,
    default: 'button',
  },
  variant: {
    type: String,
    default: 'small rounded button',
  },
  disabled: {
    type: Boolean,
    default: false,
  },

  icon: String,

  notification: {
    type: Boolean,
    default: false,
  }
})
</script>
