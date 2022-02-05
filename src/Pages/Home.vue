<template>
  <div class="flex hidden flex-col items-center" id="home">
    <div class="px-3 ml-auto border-2 rotate-12">
      <h3 class="float-right text-2xl font-bold text-white">03 FEB</h3>
    </div>

    <div class="font-sans text-center">
      <h1 class="text-6xl font-bold text-white capitalize">{{ heading }}</h1>
    </div>

    <div class="p-12 mt-6 rounded-2xl border-4 border-white">
      <img src="../assets/logo.png" alt="">
    </div>

    <div class="mt-6">
      <h1 class="font-sans text-7xl font-extrabold text-white uppercase">John Doe</h1>
      <Button title="LCVP, MAC" />
    </div>
  </div>

  <Controls @showHeading="showHeading" />
</template>

<script>
import Button from "../components/Button.vue";
import Controls from "./Controls.vue";

export default {
  name: "Home",
  components: {
    Controls,
    Button
  },
  data() {
    return {
      heading: 'Dead'
    }
  },
  methods: {
    showHeading(heading) {
      console.log('It works')
      this.heading = heading;
    },
  }
}
</script>