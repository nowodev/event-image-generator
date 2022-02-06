<template>
  <div id="controls">
    <div class="flex flex-col items-center">
      <div class="p-4 mx-4 bg-white rounded-2xl shadow-lg lg:mx-0 lg:p-16 shadow-cyan-500/50" id="image">
        <input
            type="file"
            class="accent-slate-500 p-1.5 lg:p-6 border w-full font-bold border-cyan-500/50 rounded-lg transition ease-in-out"
        />
      </div>

      <div class="flex flex-col items-center pt-6 space-y-3">
        <label for="date" class="mr-auto font-semibold text-white">Date:</label>
        <input type="date" id="date" class="px-5 py-2 w-full font-medium rounded-lg" v-model="date" />

        <label for="heading" class="mr-auto font-semibold text-white">Heading:</label>
        <input type="text" id="heading" class="px-5 py-2 w-full font-medium rounded-lg placeholder-slate-700"
               placeholder="Insert Heading" v-model="heading" />

        <label for="name" class="mr-auto font-semibold text-white">Name:</label>
        <input type="text" id="name" class="px-5 py-2 w-full font-medium rounded-lg placeholder-slate-700"
               placeholder="Insert Name" v-model="name" />

        <label for="description" class="mr-auto font-semibold text-white">Description:</label>
        <textarea rows="4" id="description" class="px-5 py-2 w-full font-medium rounded-lg placeholder-slate-700"
                  placeholder="Insert Description" v-model="description"></textarea>
      </div>
    </div>

    <div class="grid grid-cols-3 grid-flow-row gap-4 justify-items-center pt-12 lg:flex lg:justify-between">
      <button class="w-10 h-10 bg-red-500 rounded-full"></button>
      <button class="w-10 h-10 bg-blue-500 rounded-full"></button>
      <button class="w-10 h-10 bg-indigo-500 rounded-full"></button>
      <button class="w-10 h-10 bg-gray-500 rounded-full"></button>
      <button class="w-10 h-10 bg-green-500 rounded-full"></button>
      <button class="w-10 h-10 bg-white rounded-full"></button>
      <button class="w-10 h-10 bg-black rounded-full"></button>
      <button class="w-10 h-10 bg-cyan-500 rounded-full"></button>
      <button class="w-10 h-10 bg-orange-500 rounded-full"></button>
    </div>

    <div class="text-center py-12">
      <Button @click="generate" title="generate" />
    </div>
  </div>

  <div class="text-center py-12 hidden" id="show-button">
    <Button @click="back" title="Back" />
  </div>
</template>

<script>
import Button from "../components/Button.vue";

export default {
  name: "Controls.vue",
  components: {
    Button
  },
  props: [
    'date',
    'heading',
    'name',
    'description',
  ],
  methods: {
    generate() {
      this.toggle('controls')
      this.toggle('home')
      this.toggle('show-button')
      this.$emit('preview', [this.date, this.heading, this.name, this.description])
    },

    back() {
      this.toggle('home')
      this.toggle('controls')
      this.toggle('show-button')
    },

    toggle(id) {
      const value = document.getElementById(id);
      // value.classList.toggle("block");
      value.classList.toggle("hidden");
    },
  },
}
</script>

<style scoped>

</style>