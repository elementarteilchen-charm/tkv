<script setup>
	defineProps(['color'])
</script>

<template>
    <div class="d-flex py-2">
      <button :class="'btn btn-sm btn-' + color"> <slot></slot> </button>
      <input type="text">
    </div>
</template>

<style>
	
</style>