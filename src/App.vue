<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './components/HelloWorld.vue'
import Background from './Layout/Background.vue';
import Form from './components/Form.vue';
import CustomColors from './components/CustomColors.vue';
import Download from './components/Download.vue';
</script>

<template>
  <Background>
    <Form />
    <CustomColors />
    <Download />
  </Background>
  <!-- <img alt="Vue logo" class="mr-auto ml-auto" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 + Vite" />-->
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
