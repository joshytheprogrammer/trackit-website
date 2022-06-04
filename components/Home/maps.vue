<template>
  <div class="maps" id="maps" :class="{'wide' : !mobile}">
    <div class="card">
      <div class="map">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3964.142733117981!2d3.349837015003017!3d6.503609225197974!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x103b8d8b74245bed%3A0x98cda859077b56f4!2sTrack%20IT!5e0!3m2!1sen!2sng!4v1654336974311!5m2!1sen!2sng" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
      <!-- <div class="info">
        <p>1 Joseph Street, Lagos Island 102273</p>
        <h4>Hours</h4>
        <p>Monday - Friday</p>
        <p> 9am - 6pm</p>
        <h4>Contacts</h4>
        <p>08088985577</p>
        <p><a href="">kingsleyn24@yahoo.com</a></p>
      </div> -->
    </div>
  </div>
</template>

<script>
import {mapGetters} from "vuex"
export default {
  computed: {
    ...mapGetters({
      mobile: 'mobile/mobile',
    })
  },
}
</script>

<style lang="scss" scoped>
.maps {
  padding: 1rem;

  &.wide {
    
    .map {
      width: 600px;
    }

    .card {
      display: grid;
      grid-template-columns: 1fr 2fr;
    }
  }

  .map {
    width: 100%;
  }
}
</style>