<template>
  <div class="welcome-wrapper w-12/12">
    <RegistrationTxt/>

    <section class="sign-in-sec py-[60px]">
    <div>
         <header class="flex items-center gap-[12px]">
            <Icon class="w-[24px] h-[24px]" name="material-symbols:shopping-cart"/>
            <h4 class="reg-header">Act Of Services</h4>
        </header>

        <div class="setup-options">
            <BaseCheckbox
            name="profile type"
            v-model="selectedRole"
            :options="availability"
            title="Profile Type"
            />

            <BaseCheckbox
            name="general experience"
            v-model="selectedRole"
            :options="generalExperience"
            title="General Experience"
            />

            <BaseCheckbox
            name="oral services"
            v-model="selectedRole"
            :options="oralServices"
            title="Oral Services"
            />

            <BaseCheckbox
            name="numbers & extras"
            v-model="selectedRole"
            :options="numbersExtras"
            title="Numbers & Extras"
            />
        </div>
    </div>

    <div class="base-btn-wrap">
       <TextLink
       label="Go Back"
       variant="Red"
       to="/RegistrationPage/Setup"
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
import BaseCheckbox from '../inputs/BaseCheckbox.vue';

const availability = [
  { label: 'Daytime', value: 'daytime' },
  { label: 'Evenings', value: 'evenings' },
  { label: 'Overnight', value: 'overnight' },
  { label: 'Weekneds', value: 'weekends' },
  { label: 'Travel Ready', value: 'travel_ready' },
]

const generalExperience = [
  { label: 'GFE', value: 'gfe' },
  { label: 'Fetish-Friendly / Kinky Play', value: 'fetish_friendly' },
  { label: 'Cuddling & Affection', value: 'cuddling_affection' },
  { label: 'Roleplay & fantasy', value: 'roleplay_fantasy' },
  { label: 'BDSM (Soft)', value: 'bdsm_soft' },
  { label: 'BDSM (Hard)', value: 'bdsm_hard' },
  { label: 'Raw', value: 'raw' },
]

const oralServices = [
  { label: 'Oral (Giving - With Protection)', value: 'oral_giving' },
  { label: 'Oral (receiving - With Protection)', value: 'oral_receiving' },
  { label: 'CIM (Cum In Mouth)', value: 'cim' },
  { label: 'COF (Cum On Face)', value: 'cof' },
  { label: '69', value: '69' },
  { label: 'Rimming', value: 'Rimming' },
]

const numbersExtras = [
  { label: 'Threesome', value: 'threesome' },
  { label: 'Twosome', value: 'twosome' },
  { label: 'Blowjob', value: 'bowjob' },
  { label: 'Group of 10', value: 'group_of_10' },
  { label: 'House Party', value: 'house_party' },

]
</script>
