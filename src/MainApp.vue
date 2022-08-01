<script setup>
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
      
      <nav :class="menuExpanded ? 'menu-expanded' : '' ">
        <button @click="menuExpanded = !menuExpanded">
          Toggl
        </button> 
        <br> side menu (foldable)
      </nav>

      <div> <!-- Main content area -->

        <section class="info-bereich">
          <PartnerInfoBox />  <KommentarBox />
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
  
  main {
    height: calc(100vh - 12rem - 6rem); /* 12rem == höhe des info-bereichs, 3rem == header, 3rem == footer */
    overflow: hidden; 
    overflow-y: scroll;
  }

  div.app-content > nav {
    width: 4rem;
    background-color: #ebebeb;
    font-size: 90%;
  }

  div.app-content > nav.menu-expanded {
    width: 12rem;
  }

  div.brand-header {
    height: 3rem;
    padding-left: 1rem;
  }

  footer.app-footer {
    height: 3rem;
    padding-left: 1rem;
  }

  .info-bereich {
    height: 12rem;
    display:  grid;
    grid-template-columns: 2fr 5fr;
    background-color: antiquewhite;
  }

  #app {
     font-family: system-ui, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  } 


</style>