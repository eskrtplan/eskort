<template>
    <div>
        <NuxtLink :to="to">
            <button class="nav-link-wrapper relative">
                <div class="nav-sec-1">
                    <span>
                        <Icon class="nav-icon" :name="icon" v-if="icon"/>
                    </span>
        
                    <label class="nav-text">
                        <slot>{{ title }}</slot>
                    </label>
                </div>

                <div v-if="countmssg" class="nav-sec-2">
                    <span class="count">
                        <slot>{{ count }}</slot>
                    </span>
                </div>
            </button>
        </NuxtLink>
    </div>
</template>

<script setup>
defineProps({
    title: String,
    icon: String,
    to: String,
    count: {
        type: Number,
        default: 0,
    },
    countmssg: {
        type: Boolean,
        default: false,
    }
})
</script>