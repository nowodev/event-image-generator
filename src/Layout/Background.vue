<template>
    <!-- <div class="min-h-screen w-full bg-slate-900 items-center"> -->
    <div
        class="min-h-screen h-screen w-full lg:w-3/5 xl:w-2/5 bg-slate-900 items-center container mx-auto py-12">
        <Button class="hidden">Print</Button>

        <slot />
    </div>
</template>


<script>
import Button from '../components/Button.vue';
export default {
    name: "Controls",
    components: { Button }
}
</script>