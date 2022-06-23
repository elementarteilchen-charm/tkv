<script setup>
    // import Kommentar from './Kommentar.vue'
</script>

<template>
    <div class="partnerinfo-box border px-2 py-1">
        <div class="bg-secondary">
            Name
        </div>
        <div class="bg-info">
            Postadresse
        </div>
        
    </div>
</template>

<style>
    div.partnerinfo-box {
        display:  grid;
        grid-column-gap: 0.5rem;
        grid-template-columns: 50% 50%;
        overflow:  hidden;
        font-size: small;
    }
</style>