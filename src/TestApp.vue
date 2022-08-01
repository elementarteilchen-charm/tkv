<script setup>
  import KommentarBox from './components/KommentarBox.vue'
  import PartnerInfoBox from './components/PartnerInfoBox.vue'
  import AnbieterUebersicht from './components/AnbieterUebersicht.vue'
  import { ref } from 'vue'

  const showSidebar = ref(true);

</script>

<template>
  <div style="
        display: grid; 
        grid-template-rows: 1fr;
        grid-template-columns: auto 1fr; 
        height: 100vh;
  ">

    <div :class=" showSidebar ? 'sidebar-open' : 'sidebar-closed'" class="p-2 bg-light text-dark">
      <button @click="showSidebar = !showSidebar">Menu</button>
    </div>
    
    <div class="testapp-layout">

      <div class="p-2 bg-secondary" style="width: 100%;">
        <header class="bg-primary text-light p-2" style="">
          row 1 TANKARTENVERWALTUNG
        </header>

        <section class="partnerinfo-bereich p-2">  
            <PartnerInfoBox />
            <KommentarBox />        
        </section>

        <main class="datenbereich p-2" >
          <AnbieterUebersicht />
        </main>
        
        <footer class="bg-dark text-light p-2">
          row 3 Das ist der fixe Footer 
        </footer>
      </div>
    </div>    

  </div> 


</template>

<style>
  .sidebar-open {
    width: 12rem;
  }
  .sidebar-closed {
    width: 2rem;
  }

  .partnerinfo-bereich {
    display:  grid;
    background-color: aliceblue;
    grid-template-columns: 3fr 5fr;
  }

  .datenbereich {
    overflow-y: scroll;
    background-color: antiquewhite;
  }

  .testapp-layout {
    display: grid;
    grid-template-rows: auto 1fr auto;
    grid-row-gap: 0.5rem;
    overflow-y: scroll;
  }

  #testapp {
     font-family: system-ui, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  } 

</style>