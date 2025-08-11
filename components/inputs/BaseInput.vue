<template>
    <div>
        <label v-if="label" for="" class="input-label">
            <slot>{{ label }}</slot>
        </label>
        <div class="input-wrapper">
           <input
           :type="type"
           :placeholder="placeholder"
           class="base-input"
           >
           <Icon :name="icon" v-if="icon" 
           :class="[
            variant === 'red icon' ? 'input-red-icon' : 'input-icon'
           ]"
           />
        </div>
        
    </div>
</template>

<script setup>
defineProps({
    label: String,
    modelValue: String,
    placeholder: String,
    icon: String,
    variant: String,
    type: {
        type: String,
        default: 'text',
    }
})
</script>