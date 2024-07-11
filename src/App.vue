<template>
  <div id="app" class="container redondeado">
    <HomeWidget />
    <ReproductorWidget />
    <ContadorWidget />
    <MapaWidget />
    <ItinerarioWidget />
    <ListaRegalosWidget />    
    <GaleriaWidget />
    <VestimentaWidget/>
    <ConfirmacionWidget />
    <HashTagWidget/>
    <FooterWidget/>
  </div>
</template>

<script>
import HomeWidget from './components/HomeWidget.vue';
import MapaWidget from './components/MapaWidget.vue';
import ListaRegalosWidget from './components/ListaRegalosWidget.vue';
import GaleriaWidget from './components/GaleriaWidget.vue';
import ConfirmacionWidget from './components/ConfirmacionWidget.vue';
import ItinerarioWidget from './components/ItinerarioWidget.vue';
import ContadorWidget from './components/ContadorWidget.vue';
import ReproductorWidget from './components/ReproductorWidget.vue';
import HashTagWidget from './components/HashTagWidget.vue';
import VestimentaWidget from './components/VestimentaWidget';
import FooterWidget from './components/FooterWidget';

export default {
  components: {
    HomeWidget,
    MapaWidget,
    ListaRegalosWidget,
    GaleriaWidget,
    ConfirmacionWidget,
    ItinerarioWidget,
    ContadorWidget,
    ReproductorWidget,
    HashTagWidget,
    VestimentaWidget,
    FooterWidget,
  }
};
</script>

<style>

  :root {
    background-color: darkgray;
    padding: 15px;
  }

  h1, h2, h3, h4 {
    font-family: "Playwrite NZ", cursive;
    font-optical-sizing: auto;
    font-style: normal;
    padding: 10px 0;
  }

  
</style>