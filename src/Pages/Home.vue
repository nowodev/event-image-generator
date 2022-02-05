<template>
  <div class="flex hidden flex-col items-center" id="home">
    <div class="px-3 ml-auto border-2 rotate-12">
      <h3 class="float-right text-2xl font-bold text-white uppercase">{{ date }}</h3>
    </div>

    <div class="font-sans text-center">
      <h1 class="text-6xl font-bold text-white capitalize">{{ heading }}</h1>
    </div>

    <div class="p-12 mt-6 rounded-2xl border-4 border-white">
      <img src="../assets/logo.png" alt="">
    </div>

    <div class="mt-6 text-center">
      <h1 class="font-sans text-4xl font-extrabold text-white uppercase">{{ name }}</h1>
      <p class="mt-4 font-sans text-sm font-medium text-white capitalize">{{ description }}</p>
      <Button title="LCVP, MAC" />
    </div>
  </div>

  <Controls @preview="preview" />
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
      date: '',
      heading: '',
      name: '',
      description: '',
    }
  },
  methods: {
    preview(data) {
      this.date = new Date(data[0]).toDateString();
      this.heading = data[1];
      this.name = data[2];
      this.description = data[3];
    },
  }
}
</script>