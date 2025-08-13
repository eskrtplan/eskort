<template>
  <div class="welcome-wrapper w-12/12">
    <RegistrationTxt/>

    <section class="sign-in-sec ivory-smoke-bg">
    <h1 class="code-header">We’ve send a 5 digit code to your number 0810 9** ****</h1>
    <div>
    <label for="code" class="text-[18px] text-left mb-[4px]">Enter Code</label>
        <div class="flex space-x-3">
          <input @submit="submitCode"
            v-for="(digit, index) in code"
            :key="index"
            type="text"
            maxlength="1"
            v-model="code[index]"
            @input="focusNext(index, $event)"
            class="code-input"
          />
        </div>
        
        <div class="mt-[20px] text-right">
            <p class="new-here">
              <i v-if="isCounting == false">Didn't get it - </i> 
              <i v-if="isCounting == true">{{ remaining }}s - </i> 
              <!-- <NuxtLink to="/Registration"> -->
                <button @click="startCountdown" :disabled="isCounting" class="register">
                  <b>{{ isCounting ? `Resend code` : 'Resend Code' }}</b>
                </button>
              <!-- </NuxtLink> -->
            </p>
        </div>
    </div>

    <div class="flex flex-col items-center mt-[110px]">
       <TextLink
       label="Go Back"
       variant="Red"
       to="/RegistrationPage"
       />

        <BaseBtn
        label="Continue"
        variant="primary"
        class="mt-[18px]"
        to="/RegistrationPage/Capturing"
        />
    </div>
    </section>
  </div>
</template>

<script setup>
import BaseBtn from '~/components/buttons/BaseBtn.vue';
import TextLink from '~/components/buttons/TextLink.vue';
import RegistrationTxt from './RegistrationTxt.vue';
import { ref } from 'vue'


const remaining = ref(30)
const isCounting = ref(false)
let intervalId = null

const startCountdown = () => {
  isCounting.value = true
  remaining.value = 59

  intervalId = setInterval(() => {
    if (remaining.value > 0) {
      remaining.value--
    } else {
      clearInterval(intervalId)
      isCounting.value = false
    }
  }, 1000)
}


const code = ref(['', '', '', '', ''])

const focusNext = (index, event) => {
  const input = event.target
  if (input.value.length === 1 && index < code.value.length - 1) {
    input.nextElementSibling?.focus()
  }
}

const submitCode = () => {
  const joined = code.value.join('')
  if (joined.length === 5 && /^\d{5}$/.test(joined)) {
    alert(`Code entered: ${joined}`)
    // You can now send this to an API or perform a check
  } else {
    alert('Please enter all 5 digits.')
  }
}
</script>

<style scoped>
input::-webkit-inner-spin-button,
input::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
input[type='text'] {
  font-family: monospace;
}
</style>
