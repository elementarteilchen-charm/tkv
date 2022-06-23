<script setup>
  import KommentarBox from './components/KommentarBox.vue'
  import PartnerInfoBox from './components/PartnerInfoBox.vue'
</script>

<template>
  <div class="container-fluid">
    <div class="row pr-2">
      <header class="info-bereich">
        <PartnerInfoBox />
        <KommentarBox />
      </header>
    </div>
  </div>
</template>

<style>
  header.info-bereich {
    background-color: #efefef;
    display:  grid;
    grid-template-columns: 2fr 5fr;
  }

  #app {
    font-family: system-ui, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
</style>
