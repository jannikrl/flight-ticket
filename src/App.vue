<template>
  <div id="app">
    <flight-ticket></flight-ticket>
  </div>
</template>

<script>
import FlightTicket from './components/flight-ticket/FlightTicket'

export default {
  components: { 
    FlightTicket
  }
}
</script>

<style lang="scss">
  // Libraries
  $fa-font-path: '../node_modules/font-awesome/fonts/';
  @import 'node_modules/font-awesome/scss/font-awesome';

  // Global imports
  @import 'src/assets/scss/_normalize.scss';
  @import 'src/assets/scss/_base';
  @import 'src/assets/scss/_helpers';
  
  // Center flight ticket
  #app {
    display: flex;
    justify-content: center;
    align-items: center;

    height: 100vh;
    width: 100%;
  }
</style>
