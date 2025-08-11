<template>
  <div class="space-y-2">
    <p class="text-[18px]">{{ title }}</p>
    <label
      v-for="option in options"
      :key="option.value"
      class="base-radio-label"
    >
      <input
        type="checkbox"
        :value="option.value"
        v-model="internalValue"
        class="radio-input"
      />
      <span class="radio-option">{{ option.label }}</span>
    </label>
  </div>
</template>

<script setup>
const props = defineProps({
  options: {
    type: Array,
    required: true,
    default: () => []
  },
  modelValue: {
    type: Array,
    default: () => []
  },
  title: {
    type: String,
    default: 'Title'
  }
})

const emit = defineEmits(['update:modelValue'])

const internalValue = computed({
  get: () => props.modelValue,
  set: (val) => emit('update:modelValue', val)
})
</script>
