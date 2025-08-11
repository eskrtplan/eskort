<template>
    <div class="welcome-wrapper w-12/12">
        <RegistrationTxt/>

        <section class="sign-in-sec">
            <div class="grid place-items-center">
                <div class="text-center">
                    <h4 class="reg-header">Face Capturing</h4>
                    <p>Verification</p>
                </div>
        
                <div class="capture-circle">
                    <Icon class="capture-icon" name="material-symbols:imagesmode"/>
                </div>

                <div>
                    <form action="">
                        <BaseInput
                        label="National ID Card/Passport"
                        placeholder="upload"
                        type="file"
                        variant="red icon"
                        icon="material-symbols:add-a-photo-rounded"
                        class="mb-[20px]"
                        />

                        <BaseInput
                        label="Confirm password"
                        placeholder="Password"
                        type="password"
                        variant="red icon"
                        icon="ic:outline-password"
                        />

                        <div class="flex flex-col items-center mt-[110px]">
                        <TextLink
                        label="Go Back"
                        variant="Red"
                        to="/RegistrationPage/Code"
                        />

                        <BaseBtn
                        label="Continue"
                        variant="primary"
                        class="mt-[18px]"
                        to="/RegistrationPage/Setup"
                        />
                    </div>
                    </form>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
import BaseInput from '../inputs/BaseInput.vue';
import RegistrationTxt from './RegistrationTxt.vue';
import BaseBtn from '~/components/buttons/BaseBtn.vue';
import TextLink from '~/components/buttons/TextLink.vue';
</script>