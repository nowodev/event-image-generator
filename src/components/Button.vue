<template>
    <button
            class="px-6 py-3 font-bold text-white capitalize rounded-lg shadow-md focus:ring-2 hover:transition hover:delay-75 hover:scale-110 shadow-cyan-500/50"
            :class="classes"
    >
        {{ title }}
    </button>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: 'Button'
        },
        color: {
            type: String,
            default: 'bg-sky-600 hover:bg-sky-900'
        },
    },
    computed: {
        classes() {
            return this.color
        }
    }
}
</script>