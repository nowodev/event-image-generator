<template>
    <div class="grid content-between h-full">
        <div class="flex flex-col gap-y-4">
            <Input type="file" name="" id="" />

            <Input type="date" />

            <Input placeholder="Description" />
            <Input placeholder="Name" />

            <textarea
                class="border-gray-300 focus:border-indigo-300 focus:ring focus:ring-indigo-200 focus:ring-opacity-50 rounded-md shadow-sm border px-3 py-1"
                cols="30" rows="10"></textarea>

            <div
                class="grid grid-cols-3 grid-flow-row gap-4 justify-items-center pt-12 lg:flex lg:justify-between">
                <button class="w-10 h-10 bg-red-500 rounded-full"></button>
                <button class="w-10 h-10 bg-blue-500 rounded-full"></button>
                <button class="w-10 h-10 bg-indigo-500 rounded-full"></button>
                <button class="w-10 h-10 bg-gray-500 rounded-full"></button>
                <button class="w-10 h-10 bg-green-500 rounded-full"></button>
                <button class="w-10 h-10 bg-sky-500 rounded-full"></button>
                <button class="w-10 h-10 bg-black rounded-full"></button>
                <button class="w-10 h-10 bg-cyan-500 rounded-full"></button>
                <button class="w-10 h-10 bg-orange-500 rounded-full"></button>
            </div>
        </div>

        <div class="flex justify-center">
            <Button>Preview</Button>
        </div>
    </div>
</template>

<script>
import Input from '../components/Input.vue';
import Button from '../components/Button.vue';
export default {
    name: "Controls",
    components: { Input, Button }
}
</script>