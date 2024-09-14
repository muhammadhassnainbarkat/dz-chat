<script setup lang="ts">
import { GoogleLogin } from 'vue3-google-login'
import type {
  CredentialPopupResponse,
  GoogleAuthButtonConfiguration
} from '@/module/auth/types/auth.types'
const googleLoginCallBack = (response: CredentialPopupResponse) => {
  console.log(response)
}

const buttonConfiguration: GoogleAuthButtonConfiguration = {
  theme: 'outline',
  text: 'continue_with',
  shape: 'circle',
  locale: 'en-us',
  logo_alignment: 'left'
}
</script>

<template>
  <GoogleLogin :callback="googleLoginCallBack" :button-config="buttonConfiguration" />
</template>

<style scoped></style>
