<script setup>
  import AnbieterTabelle from './components/AnbieterVerwaltung/AnbieterTabelle.vue'
  import AnbieterDetailAnsicht from './components/AnbieterVerwaltung/AnbieterDetailAnsicht.vue'
  import { reactive, ref, nextTick} from 'vue'

  let anbieter = [
    {
      pnr: 13,
      name1: "Shell",
      name2: "GmbH"
    },
    {
      pnr: 456,
      name1: "logpay",
      name2: "Ltd",
      details: {
        mautkarten: [1,2,3],
        tankkkarten:  [4,5,6]
      }
    }
  ]

  let ausgewaehlterAnbieter = ref()

  function show(e) {
    ausgewaehlterAnbieter.value = anbieter.find(item => item.pnr == e)
  }

</script>

<template>
  <div class="app-layout">

    <header class="">
      <h2 class="p-3 bg-light">
        Anbieterdetails
      </h2>

      <div class="anbieter-tabelle p-3">      
        <AnbieterTabelle :alleAnbieter="anbieter" @show="show"/>
      </div>

    </header>

    <main class="p-3" style="overflow-y: scroll;">
      <AnbieterDetailAnsicht :anbieter="ausgewaehlterAnbieter"/>
    </main>
    
    <footer class="bg-light" style="min-height: 2rem;">
      <div class="p-3">
        Footer
      </div>
    </footer>
  </div>
</template>

<style>
  .anbieter-tabelle {
    
  }

  #appanbieterdetails {
     font-family: system-ui, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  } 

  .app-layout {
    display: grid;
    grid-template-rows: auto 1fr auto;
    height: 100vh;
    
  }
</style>
