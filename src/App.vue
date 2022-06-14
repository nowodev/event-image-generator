<script setup>
import Background from './Layout/Background.vue';
import Home from "./Pages/Home.vue";
import Preview from './Pages/Preview.vue';
import Controls from './Pages/Controls.vue';
</script>

<template>
    <div class="bg-slate-900">
        <Background>
            <!-- <Home /> -->
            <!-- <Preview /> -->
            <Controls />
        </Background>
    </div>
</template>

<style>
#app {
    /*font-family: Avenir, Helvetica, Arial, sans-serif;*/
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /* text-align: center; */
    /*color: #2c3e50;*/
    /* margin-top: 60px; */
}
</style>
