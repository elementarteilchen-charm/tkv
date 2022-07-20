<script setup>
    import Anbieter from './Anbieter.vue'
</script>

<template>
    <div class="anbieter-uebersicht">
        <Anbieter name="Shell" :tankkarten="{'aktiv': 1, 'gesperrt': 0, 'endgueltig': 0}" />
        <Anbieter name="LogPay" :tankkarten="{'aktiv': 2, 'gesperrt': 0, 'endgueltig': 1}" />
        <Anbieter name="IDS" :tankkarten="{'aktiv': 3, 'gesperrt': 1, 'endgueltig': 0}" />
        
    </div>
</template>

<style>
    div.anbieter-uebersicht {
        display:  grid;
        grid-row-gap: 1.5rem;
        grid-template-rows: 1fr;
        
    }
</style>