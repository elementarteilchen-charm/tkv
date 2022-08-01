<script setup>
    import Anbieter from './Anbieter.vue'
    const items = [1,2,3,4,5,6,7,8,9,10,11,12,13]
</script>

<template>
    <div class="py-3">

        <Anbieter name="Shell" :tankkarten="{aktiv: 2, gesperrt: 1, endgueltig: 0}" />
        <Anbieter name="LogPay" :tankkarten="{aktiv: 2, gesperrt: 1, endgueltig: 0}" />
        <Anbieter name="IDS" :tankkarten="{aktiv: 2, gesperrt: 1, endgueltig: 0}" />
        <Anbieter name="INAK" :tankkarten="{aktiv: 2, gesperrt: 1, endgueltig: 0}" />
        
    </div>
</template>

<style>
   
</style>