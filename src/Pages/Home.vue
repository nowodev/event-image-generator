<template>
  <div class="flex flex-col items-center">
    <div class="ml-auto border-2 px-3 rotate-12">
      <h3 class="text-white text-2xl font-bold float-right">03 FEB</h3>
    </div>

    <div class="text-center font-sans">
      <h1 class="text-white text-6xl font-bold">Happy</h1>
      <h1 class="text-white text-6xl font-bold">Birthday</h1>
    </div>

    <div class="p-12 border-4 border-white rounded-2xl mt-6">
      <img src="../assets/logo.png" alt="">
    </div>

    <div class="mt-6">
      <h1 class="uppercase text-white text-7xl font-extrabold font-sans">John Doe</h1>
      <Button title="LCVP, MAC" />
    </div>
  </div>
</template>

<script>
import Button from "../components/Button.vue";

export default {
  name: "Home",
  components: {Button}
}
</script>

<style scoped>

</style>