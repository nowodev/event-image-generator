<template>
  <div class="flex flex-col items-center">
    <div class="bg-white mx-4 p-4 lg:mx-0 lg:p-16 shadow-lg shadow-cyan-500/50 rounded-2xl">
      <input
          type="file"
          class="accent-slate-500 p-1.5 lg:p-6 border w-full font-bold border-cyan-500/50 rounded-lg transition ease-in-out"
      />
    </div>

    <div class="pt-6 flex flex-col items-center space-y-3">
      <input type="text" class="rounded-lg font-semibold px-5 py-2 placeholder-slate-700 w-full"
             placeholder="Insert Heading" />
      <textarea rows="4" class="rounded-lg font-thin px-5 py-2 placeholder-slate-700 w-full"
                placeholder="Insert Description"></textarea>
    </div>
  </div>
</template>