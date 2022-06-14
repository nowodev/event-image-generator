<template>
    <div :class="gen ? 'hidden' : 'block'">
        <div class="flex flex-col items-center">
            <div id="image" class="p-4 mx-4 bg-white rounded-2xl shadow-lg lg:mx-0 lg:p-16 shadow-cyan-500/50">
                <input
                        class="accent-slate-500 p-1.5 lg:p-6 border w-full font-bold border-cyan-500/50 rounded-lg transition ease-in-out"
                        type="file"
                />
            </div>

            <div class="flex flex-col items-center pt-6 space-y-3">
                <label class="mr-auto font-semibold text-white" for="date">Date:</label>
                <input id="date" v-model="date" class="px-5 py-2 w-full font-medium rounded-lg" type="date" />

                <label class="mr-auto font-semibold text-white" for="heading">Heading:</label>
                <input id="heading" v-model="heading"
                       class="px-5 py-2 w-full font-medium rounded-lg placeholder-slate-700"
                       placeholder="Insert Heading" type="text" />

                <label class="mr-auto font-semibold text-white" for="name">Name:</label>
                <input id="name" v-model="name" class="px-5 py-2 w-full font-medium rounded-lg placeholder-slate-700"
                       placeholder="Insert Name" type="text" />

                <label class="mr-auto font-semibold text-white" for="description">Description:</label>
                <textarea id="description" v-model="description"
                          class="px-5 py-2 w-full font-medium rounded-lg placeholder-slate-700"
                          placeholder="Insert Description" rows="4"></textarea>
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

        <div class="py-12 text-center">
            <Button title="generate" @click="generate" />
        </div>
    </div>

    <div :class="hide ? 'hidden' : 'block'" class="py-12 text-center">
        <Button title="Back" @click="back" />
    </div>
</template>

<script>
    import Button from "../components/Button.vue";

    export default {
        name: "Controls",

        components: {
            Button
        },

        props: [
            'date',
            'heading',
            'name',
            'description',
        ],

        data() {
            return {
                'gen': false,
                'hide': true,
            }
        },

        methods: {
            generate: function () {
                this.gen = !this.gen
                this.hide = !this.hide
                this.$emit('preview', [this.gen, this.date, this.heading, this.name, this.description])
            },

            back: function () {
                this.hide = !this.hide
                this.gen = !this.gen
                this.$emit('preview', [this.gen])
            },
        },
    }
</script>

<style scoped>

</style>