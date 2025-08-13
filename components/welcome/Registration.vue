<template>
    <div class="welcome-wrapper w-12/12">
        <RegistrationTxt/>

        <section class="sign-in-sec ivory-smoke-bg">
            <div class="md:hidden p-[42px]">
                <h4 class="registration-header">Registration</h4>
                <p class="registration-text">
                    All personal information you provide is protected with advanced security technologies like end-to-end encryption, secure storage, and regular audits. We never sell your data, and we never access your personal content without your permission.
                    <br>
                    <br>
                    You're in full control of your data. You can view, update, download, or delete your personal information at any time from your account settings. Transparency is key—we’ll always let you know why we’re asking for certain details and how they’re used.
                </p>
            </div>
            <div>

                <!-- REGISTER -->
                <form action="" class="pb-[67px] md:py-[67px]">
                    <div class="flex flex-col gap-[8px]">
                        <BaseInput
                        label="Personal information"
                        placeholder="Firstname"
                        icon="uil:user"
                        variant="red icon"
                        />

                        <BaseInput
                        placeholder="Lastname"
                        icon="uil:user"
                        variant="red icon"
                        />

                        <BaseInput
                        placeholder="State of Origin"
                        icon="ic:baseline-edit-road"
                        variant="red icon"
                        />

                        <BaseInput
                        placeholder="Current Residence"
                        icon="ic:sharp-house"
                        variant="red icon"
                        />

                        <BaseInput
                        type="number"
                        placeholder="NIN/BVN"
                        icon="ic:outline-password"
                        variant="red icon"
                        />

                        <BaseInput
                        placeholder="Phone"
                        icon="ic:baseline-phone-in-talk"
                        variant="red icon"
                        />
                    </div>

                    <div class="flex flex-col gap-[8px] mt-[20px]">
                        <BaseInput
                        label="Access information"
                        type="email"
                        placeholder="Email"
                        icon="ic:baseline-alternate-email"
                        variant="red icon"
                        />

                        <BaseInput
                        placeholder="Username"
                        icon="uil:user"
                        variant="red icon"
                        />

                        <BaseInput
                        placeholder="Password"
                        type="password"
                        icon="ic:baseline-password"
                        variant="red icon"
                        />

                        <BaseInput
                        placeholder="Confirm Password"
                        type="password"
                        icon="ic:baseline-password"
                        variant="red icon"
                        />
                    </div>

                    <div class="flex flex-col items-center mt-[110px]">
                        <TextLink
                        label="Go Back"
                        variant="Red"
                        to="/WelcomePage"
                        />

                        <BaseBtn
                        label="Continue"
                        variant="primary"
                        class="mt-[18px]"
                        to="/RegistrationPage/Code"
                        />
                    </div>
                </form>
            </div>
        </section>
    </div>
</template>

<script setup>
import BaseBtn from '~/components/buttons/BaseBtn.vue';
import TextLink from '~/components/buttons/TextLink.vue';
import BaseInput from '~/components/inputs/BaseInput.vue';
import RegistrationTxt from './RegistrationTxt.vue';
</script>