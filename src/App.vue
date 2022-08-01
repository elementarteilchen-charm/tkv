<script setup>
  import KommentarBox from './components/KommentarBox.vue'
  import PartnerInfoBox from './components/PartnerInfoBox.vue'
  import AnbieterUebersicht from './components/AnbieterUebersicht.vue'
</script>

<template>
  <div class="app-layout">
    <header class="">
      <div class="p-3 bg-light">
        Verwaltung
      </div>
      <div class="info-bereich p-3">      
        <PartnerInfoBox />
        <KommentarBox />
      </div>
    </header>

    <main class="p-3" style="overflow-y: scroll;">
      <AnbieterUebersicht />
    </main>


    <footer class="bg-dark text-light" style="min-height: 2rem;">
      <div class="p-3">
        Footer
      </div>
    </footer>

  </div> <!-- app-layout -->
</template>

<style>
  .info-bereich {
    display:  grid;
    background-color: aliceblue;
    grid-template-columns: 3fr 5fr;
  }

  .app-layout {
    display: grid;
    grid-template-rows: auto 1fr auto;
    height: 100vh; 
  }

  #app {
     font-family: system-ui, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  } 

</style>
