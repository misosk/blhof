<template>
  <div id="layout">
    <b-container>
      <MainMenu/>

      <nuxt />
    </b-container>
  </div>
</template>
<script setup>
import MainMenu from '~/components/MainMenu.vue'
</script>
