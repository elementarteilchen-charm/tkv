<script setup>
  import TKVButton from './components/TKVButton.vue'
  import TKVSuche from './components/TKVSuche.vue'
  import PartnerAktionen from './components/PartnerAktionen.vue'
  import KommentarBox from './components/KommentarBox.vue'
  import PartnerInfoBox from './components/PartnerInfoBox.vue'
  import AnbieterUebersicht from './components/AnbieterUebersicht.vue'
  import { ref } from 'vue'

  const menuExpanded = ref(false)

</script>

<template>
  <div id="mainapp">

    <div class="brand-header d-flex align-items-center bg-primary text-light">
      brand header
    </div>
    
    <div class="app-content">
      
      <nav 
        :class="menuExpanded ? 'menu-expanded' : '' ">
        <button @click="menuExpanded = !menuExpanded">
          Toggl
        </button> 
        <br> side menu (foldable)
      </nav>

      <div> <!-- Main content area -->

        <header class="app-header-suche">
          <div>
            <span class="app-pageName">1232450 Kitlik Trans GmbH</span>
          </div>

          <div class="d-flex justify-content-end">
            <TKVSuche color="primary">Risikoliste</TKVSuche>
            <TKVSuche color="success">Verwaltung</TKVSuche>
          </div>
        </header>

        <section class="partner-info-bereich">
          <PartnerInfoBox />  

          <div>
            <PartnerAktionen />
            <KommentarBox style="background-color: lightgreen;"/>
          </div>
        </section>

        <main>
            <AnbieterUebersicht/>
        </main>
      
      </div>

    </div>
    
    
    <footer class="app-footer py-2 bg-dark text-light">
      app footer (fixed)
    </footer>
    
  </div>
</template>

<style>
  :root {
    --action-bar-height: 3rem;
  }

  #mainapp {
    display: grid;
    grid-template-rows: auto 1fr auto;
    height: 100vh; 
  }
  
  div.app-content {
    display: grid;
    grid-template-columns: auto 1fr;
    grid-column-gap: 1rem;
  }
  
  div.brand-header {
    height: var(--action-bar-height);
    padding-left: 1rem;
  }

  .app-header-suche {
    height: var(--action-bar-height);
    display: grid;
    grid-template-columns: 1fr 1fr;
    border-bottom:  1px solid #ccc;
  }

  .partner-info-bereich {
    height: 13rem;
    display:  grid;
    grid-template-columns: 2fr 5fr;
    grid-column-gap: 0.5rem;  
  }

  main {
    /* 13rem == höhe des partner-info-bereichs, 3rem == header 3rem == app-header, 3rem == footer */
    height: calc(100vh - 13rem - var(--action-bar-height) - var(--action-bar-height) - 3rem); 
    overflow: hidden; 
    overflow-y: scroll;
    padding-top: 1rem;
    background-color: azure;
  }


  div.app-content > nav {
    width: 4rem;
    background-color: #ebebeb;
    font-size: 90%;
  }

  div.app-content > nav.menu-expanded {
    width: 12rem;
  }


  footer.app-footer {
    height: 3rem;
    padding-left: 1rem;
  }



  #app {
     font-family: system-ui, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  } 


</style>