<script setup>
    import { reactive, ref, nextTick} from 'vue'
    defineProps(['anbieter'])

    function show(e) {
        alert("caught event")
    }
</script>

<template>
    
    <div @show="show">
        Hier wird etwas zum Anbieter angezeigt
        {{anbieter}}    
    </div>
</template>