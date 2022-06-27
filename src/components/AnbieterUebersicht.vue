<script setup>
    import Anbieter from './Anbieter.vue'
</script>

<template>
    <div class="anbieter-uebersicht">
        <Anbieter name="Shell"/>
        <Anbieter name="LogPay"/>
        <Anbieter name="IDS"/>
        <Anbieter name="Saudi Oil"/>
    </div>
</template>

<style>
    div.anbieter-uebersicht {
        display:  grid;
        grid-row-gap: 1.5rem;
        grid-template-rows: 1fr;

        overflow:  hidden;
        overflow-y:  scroll;
        
    }
</style>