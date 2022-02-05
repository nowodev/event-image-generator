<template>
  <div class="py-12 text-center">
    <button
        class="px-6 py-3 font-bold text-white capitalize bg-sky-600 rounded-lg shadow-md hover:bg-sky-900 focus:ring-2 hover:transition hover:delay-75 hover:scale-110 shadow-cyan-500/50"
    >
      {{ title }}
    </button>
  </div>
</template>

<script>
export default {
  props: {
    'title': {
      type: String,
      default: 'Button'
    }
  },
}
</script>