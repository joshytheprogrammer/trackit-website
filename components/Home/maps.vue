<template>
  <div class="maps" id="maps" :class="{'wide' : !mobile}">
    <div class="_header">
      <h2>Our Offices</h2>
    </div>
    <div class="content">
      <div class="card">
        <div class="map">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3964.142733117981!2d3.349837015003017!3d6.503609225197974!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x103b8d8b74245bed%3A0x98cda859077b56f4!2sTrack%20IT!5e0!3m2!1sen!2sng!4v1654336974311!5m2!1sen!2sng" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
        <div class="info">
          <h4>Address</h4>
          <p>40, Oyekan Street Off Ogunlana Drive Surulere, Lagos.</p>
          <h4>Hours</h4>
          <p>Monday - Friday</p>
          <p>8am - 5pm</p>
          <h4>Contacts</h4>
          <p><a href="tel:+234 901 563 0453">+234 901 563 0453</a></p>
          <p><a href="mailto:info@trackit.com.ng">info@trackit.com.ng</a></p>
        </div>
      </div>
      <div class="card">
        <div class="map">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15759.903889839848!2d7.455027980789247!3d9.06595313563224!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x104e0b146aaaaaab%3A0x1f731775230620f7!2sTrack%20IT%20Limited!5e0!3m2!1sen!2sng!4v1654354352329!5m2!1sen!2sng" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
        <div class="info">
          <h4>Address</h4>
          <p>Suite 11b, DBM plaza Wuse Zone1, Abuja.</p>
          <h4>Hours</h4>
          <p>Monday - Friday</p>
          <p>8am - 5pm</p>
          <h4>Contacts</h4>
          <p><a href="tel:+234 802 317 8729">+234 802 317 8729</a></p>
          <p><a href="mailto:info@trackit.com.ng">info@trackit.com.ng</a></p>
        </div>
      </div>
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

  ._header {
    margin: 2rem 0;
    
    h2 {
      font-weight: 400;
      font-size: 36px;
    }
  }

  .content {
    .card {
      margin: 1rem 0;
    }
  }

  &.wide {
    .content {
      .card {
        margin: 2rem 0;
        display: grid;
        grid-template-columns: 1fr 1fr;

        @media screen and (max-width: 900px) {
          display: block;
        }
      }
    }
  }

  .map {
    width: 100%;
  }

  .info {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 1rem;

    h6 {
      padding: 0.9rem 0;
    }

    p {
      padding: 0.5rem 0;

      a {
        color: $dark;
      }
    }
  }
}
</style>