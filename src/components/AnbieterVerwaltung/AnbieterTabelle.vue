<script setup>
    defineProps(['alleAnbieter']);
    const emit = defineEmits(['show'])

</script>

<template>
    <div v-for="anbieter in alleAnbieter">
        <a href="" v-on:click.prevent="emit('show', anbieter.pnr)">
            {{anbieter.pnr + ' - ' + anbieter.name1 + ' ' + anbieter.name2}}
        </a> 
    </div>
    <a href="" v-on:click.prevent="emit('show', 0)">
        Clear
    </a> 
</template>

<style>
    
</style>