<template>
  <div class="flex flex-col items-center">
    <div class="flex justify-between">
      <!--      <div class="w-1/3" id="heading">-->
      <!--        <h3 class="text-white font-bold text-lg capitalize">{{ heading }}</h3>-->
      <!--      </div>-->

      <div class="bg-white mx-4 p-4 lg:mx-0 lg:p-16 shadow-lg shadow-cyan-500/50 rounded-2xl" id="image">
        <input
            type="file"
            class="accent-slate-500 p-1.5 lg:p-6 border w-full font-bold border-cyan-500/50 rounded-lg transition ease-in-out"
        />
      </div>

      <!--      <div class="" id="date">-->
      <!--        <h3 class="text-white font-bold text-lg capitalize">{{ date }}</h3>-->
      <!--      </div>-->
    </div>

    <div class="pt-6 flex flex-col items-center space-y-3">
      <input type="date" class="rounded-lg px-5 py-2 w-full font-semibold" v-model="date" />

      <input type="text" class="rounded-lg font-semibold px-5 py-2 placeholder-slate-700 w-full"
             placeholder="Insert Heading" v-model="heading" />

      <textarea rows="4" class="rounded-lg font-thin px-5 py-2 placeholder-slate-700 w-full"
                placeholder="Insert Description"></textarea>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    'heading',
    'date',
    'description',
  ],
}
</script>