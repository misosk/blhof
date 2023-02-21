<template>
  <div id="layout" style='background-image: url("https://mdbootstrap.com/img/Photos/Others/images/76.jpg"); height: 100vh;'>
    <b-container>
      <MainMenu/>

      <nuxt />
    </b-container>
  </div>
</template>
<script setup>
import MainMenu from '~/components/MainMenu.vue'
</script>
