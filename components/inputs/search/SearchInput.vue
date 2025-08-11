<template>
    <div>
        <label v-if="label" for="" class="input-label">
            <slot>{{ label }}</slot>
        </label>
        <div class="search-wrapper">
           <input
           :type="type"
           :placeholder="placeholder"
           class="search-input"
           >
           <NuxtLink :to="to">
            <Icon :name="icon" v-if="icon"
            :class="[
             variant === 'red icon' ? 'input-red-icon' : 'input-icon'
            ]"
            />
           </NuxtLink>
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
    to: String,
    type: {
        type: String,
        default: 'text',
    }
})
</script>