<template>
    <input
        class="border-gray-300 focus:border-indigo-300 focus:ring focus:ring-indigo-200 focus:ring-opacity-50 rounded-md shadow-sm border px-3 py-1"
        :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" ref="input" />

    <!-- <input type="text" name="first-name" id="first-name" autocomplete="given-name" class="mt-1 focus:ring-indigo-500 focus:border-indigo-500 block w-full shadow-sm sm:text-sm border-gray-300 rounded-md border"> -->

</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
    name: "Input",

    props: ['modelValue'],

    emits: ['update:modelValue'],

    methods: {
        focus() {
            this.$refs.input.focus()
        }
    }
})
</script>
