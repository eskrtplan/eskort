<template>
    <div class="profile-success-wrapper">
        <div class="p-s-sec1">
            <svg width="61" height="60" viewBox="0 0 61 60" fill="none" xmlns="http://www.w3.org/2000/svg">
               <circle cx="30.5" cy="30" r="30" fill="#2D1E2F"/>
               <g clip-path="url(#clip0_44_75)">
               <path d="M26.2492 38.6626C25.5679 38.6629 24.9146 38.3921 24.4332 37.91L18.9431 32.4219C18.3523 31.8309 18.3523 30.873 18.9431 30.2821C19.534 29.6913 20.4919 29.6913 21.0828 30.2821L26.2492 35.4484L39.9172 21.7805C40.5081 21.1897 41.466 21.1897 42.0569 21.7805C42.6477 22.3714 42.6477 23.3293 42.0569 23.9202L28.0651 37.91C27.5838 38.3921 26.9305 38.6629 26.2492 38.6626Z" fill="#F4F4F9"/>
               </g>
               <defs>
               <clipPath id="clip0_44_75">
               <rect width="24" height="24" fill="white" transform="translate(18.5 18)"/>
               </clipPath>
               </defs>
            </svg>

            <p class="font-semibold text-[18px] mt-[20px]">Your profile has been created successfully</p>
        </div>
        
        <BaseBtn
        label="Continue"
        variant="primary"
        class="mt-[18px]"
        to="/"
        />
    </div>
</template>

<script setup>
import BaseBtn from '~/components/buttons/BaseBtn.vue';
</script>