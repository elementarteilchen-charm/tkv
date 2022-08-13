<script setup>
  import TKVButton from './components/TKVButton.vue'
  import TKVModal from './components/TKVModal.vue'
  import TKVSuche from './components/TKVSuche.vue'
  import PartnerAktionen from './components/PartnerAktionen.vue'
  import KommentarBox from './components/KommentarBox.vue'
  import PartnerInfoBox from './components/PartnerInfoBox.vue'
  import AnbieterUebersicht from './components/AnbieterUebersicht.vue'
  import { ref } from 'vue'

  const menuExpanded = ref(false)
  const showModal = ref(false)

</script>

<template>
  <div id="testapp">
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

      <div style="position: relative;"> <!-- Main content area -->

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
            <button @click="showModal = true">Neue Karte</button>
            <KommentarBox style="background-color: lightgreen;"/>
          </div>
        </section>

        <main>
            <AnbieterUebersicht/>
        </main>
        
        <div class="floating-bar d-flex align-items-center justify-content-between">
          <div>
            Floating Bar Message
          </div>
          <div>
            <button class="btn btn-danger btn-sm">Do something</button>
          </div>
        </div>
      
      </div>

    </div>
    
    
    <TKVModal :show="showModal"/>
    
    <footer class="app-footer py-2 bg-dark text-light">
      app footer (fixed)
    </footer>

    
</div>

</template>

<style>
 :root {
    --action-bar-height: 3rem;
  }

  .floating-bar {
    position: absolute;
    top:  80%; 
    width:  80%;
    height:  5rem;
    margin-left:  10%;
    padding:  1rem;
    display:  flex;
    background-color: white;
    border:  1px solid #ddd;
    border-radius:  3px;
    box-shadow: 0 6px 8px -1px rgb(0 0 0/0.1),0 2px 4px -2px rgb(0 0 0/0.1)
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
    height: 1rem;
    padding-left: 1rem;
    font-size: 0.75rem;
  }



  #app {
     font-family: system-ui, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  } 


</style>