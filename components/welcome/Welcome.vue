<template>
    <div class="welcome-wrapper w-12/12">
        <section class="welcome-sec hidden md:grid">
            <div class="flex flex-col items-center">
                <img class="welcome-img" alt="eskort-logo">
                <h2 class="welcome-text">Welcome</h2>
            </div>
        </section>

        <section class="sign-in-sec">
            <div>
                <!-- LOGIN -->
                <form action="">
                    <div>
                        <BaseInput
                        placeholder="Username"
                        icon="uil:user"
                        class="mb-[20px]"
                        />

                        <BaseInput
                        type="password"
                        placeholder="Password"
                        icon="ic:outline-password"
                        class="mb-[40px]"
                        />

                        <BaseBtn
                        label="Login"
                        variant="primary"
                        />

                        <div class="mt-[20px] text-right">
                            <p class="new-here">New here? <NuxtLink to="/RegistrationPage" class="register"><b>Register</b></NuxtLink></p>
                        </div>
                    </div>
                </form>

                <div class="continue-with">
                    <b class="font-extrabold text-[14px]">Or Continue With</b>
                    <NuxtLink to="">
                        <img src="" alt="" class="svg-img-icon">
                    </NuxtLink>
                    <NuxtLink to="">
                        <img src="" alt="" class="svg-img-icon">
                    </NuxtLink>
                    <NuxtLink to=""></NuxtLink>
                    <div class="terms">
                        <NuxtLink to=""><p>Terms & Conditions</p></NuxtLink>
                        <NuxtLink to=""><p>Privacy Policy</p></NuxtLink>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
import BaseBtn from '~/components/buttons/BaseBtn.vue';
import BaseInput from '~/components/inputs/BaseInput.vue';
</script>