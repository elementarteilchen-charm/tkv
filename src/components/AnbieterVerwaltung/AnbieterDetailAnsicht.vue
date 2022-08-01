<script setup>
    import { reactive, ref, nextTick} from 'vue'
    defineProps(['anbieter', 'zeigeAnbieter'])

</script>

<template>
    Hier wird etwas zum Anbieter angezeigt
    <transition>
        <div v-if="anbieter">
            {{anbieter}}    
        </div>
    </transition>
</template>

<style>
    .v-enter-active,
    .v-leave-active {
        transition: opacity .75s ease;
    }

    .v-enter-from,
    .v-leave-to {
        opacity: 0;
        transition: opacity .25s ease;
    }
</style>