<template>
  <div class="flex flex-col items-center">
    <div class="bg-white p-16 shadow-lg shadow-cyan-500/50 rounded-full">
      <input
        type="file"
        class="accent-slate-500 p-6 border w-full font-bold border-cyan-500/50 rounded-lg transition ease-in-out"
      />
    </div>

    <div class="pt-6 flex flex-col items-center space-y-3">
      <input type="text" class="rounded-lg px-5 py-2" placeholder="Insert Heading" />
      <textarea cols="30" rows="4" class="rounded-lg px-5 py-2" placeholder="Insert Description"></textarea>
    </div>
  </div>
</template>