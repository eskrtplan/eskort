<template>
  <div class="welcome-wrapper w-12/12">
    <RegistrationTxt/>

    <section class="sign-in-sec ivory-smoke-bg">
    <div>
         <header class="flex items-center gap-[12px]">
            <Icon class="w-[24px] h-[24px]" name="solar:user-heart-rounded-line-duotone"/>
            <h4 class="reg-header">Set Up Your Profile</h4>
        </header>

        <div class="setup-options">
            <BaseRadio
            name="acct-type"
            v-model="selectedRole"
            :options="type"
            title="Profile Type"
            />

            <BaseRadio
            name="sex"
            v-model="selectedRole"
            :options="sex"
            title="Sex"
            />

            <BaseRadio
            name="age-range"
            v-model="selectedRole"
            :options="age"
            title="Age"
            />
        </div>
    </div>

    <div class="base-btn-wrap">
       <TextLink
       label="Go Back"
       variant="Red"
       to="/RegistrationPage/Capturing"
       />

        <BaseBtn
        label="Continue"
        variant="primary"
        class="mt-[18px]"
        to="/RegistrationPage/Services"
        />
    </div>
    </section>
  </div>
</template>

<script setup>
import BaseBtn from '~/components/buttons/BaseBtn.vue';
import TextLink from '~/components/buttons/TextLink.vue';
import RegistrationTxt from './RegistrationTxt.vue';
import BaseRadio from '../inputs/BaseRadio.vue';

const type = [
  { label: 'Escort', value: 'escort' },
  { label: 'Client', value: 'client' },
]

const sex = [
  { label: 'Female', value: 'female' },
  { label: 'Male', value: 'male' },
]

const age = [
  { label: '18-24', value: '18_24' },
  { label: '25-34', value: '25_34' },
  { label: '35&above', value: '35_and_above' },
]
</script>
