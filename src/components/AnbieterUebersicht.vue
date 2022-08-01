<script setup>
    import Anbieter from './Anbieter.vue'
    const items = [1,2,3,4,5,6,7,8,9,10,11,12,13]
</script>

<template>
    <div class="py-3">
        <div v-for="(item, index) in items">
            <div class="d-flex align-items-center border p-3 mb-3" style="height: 3rem;">
                Some info about Anbieter {{item}}
            </div>
        </div>
        <!-- <Anbieter name="Shell"/>
        <Anbieter name="LogPay"/>
        <Anbieter name="IDS"/>
        <Anbieter name="Saudi Oil"/> -->
    </div>
</template>

<style>
   
</style>