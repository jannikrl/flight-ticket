<template>
  <div class="flight-ticket">
    <section>
      <flight-route></flight-route>

      <flight-route></flight-route>

      <footer>
        <footer-actions :rating="rating"></footer-actions>
        <footer-details></footer-details>
      </footer>
    </section>
    
    <aside>
      <side :rating="rating"></side>
    </aside>
  </div>
</template>

<!-- The "scoped" attribute limits CSS to this component only -->
<style lang="scss" scoped>
  @import 'src/assets/scss/_variables';

  .flight-ticket {
  	background-color: #fff;
  	width: 100%;
  	max-width: 710px;
    border-radius: $box-border-radius;
    overflow: hidden;

    aside {
      display: none;
    }

    .footer-details {
      display: none;
    }
  }

  @media only screen and (min-width: $screen-sm-min) {
    .flight-ticket {
      display: flex;

      section {
        flex: 1;
      }

      aside {
        display: block;
        flex: 0 0 170px;
        background-color: #e8f0f3;
      }

      .footer-actions {
        display: none;
      }

      .footer-details {
        display: block;
      }
    }
  }
</style>

<script>
import FlightRoute from './subcomponents/FlightRoute'
import FooterActions from './subcomponents/FooterActions'
import FooterDetails from './subcomponents/FooterDetails'
import Side from './subcomponents/Side'

export default {
  // Fetch data from API
  data() {
    return {
      rating: 9.3,
    }
  },

  components: {
    FlightRoute,
    FooterActions,
    FooterDetails,
    Side,
  }
}
</script>