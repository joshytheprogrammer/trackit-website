<template>
  <div class="testimonials" :class="{'wide' : !mobile}" id="testimonials">
    <div class="_header">
      <h2>Here's what our clients say</h2>
    </div>
    <div class="content">
      <div class="card">
        <p class="testimony">"Every day, they strive to improve their service to the clients by developing the right blend of technology and creativity to make sure every job done is done as efficiently as possible."</p>
        <p class="testifier">-Claurice Turner</p>
      </div>
      <div class="card">
        <p class="testimony">"Every day, they strive to improve their service to the clients by developing the right blend of technology and creativity to make sure every job done is done as efficiently as possible."</p>
        <p class="testifier">-Claurice Turner</p>
      </div>
      <div class="card">
        <p class="testimony">"Every day, they strive to improve their service to the clients by developing the right blend of technology and creativity to make sure every job done is done as efficiently as possible."</p>
        <p class="testifier">-Claurice Turner</p>
      </div>
      <div class="card">
        <p class="testimony">"Every day, they strive to improve their service to the clients by developing the right blend of technology and creativity to make sure every job done is done as efficiently as possible."</p>
        <p class="testifier">-Claurice Turner</p>
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
.testimonials {
  margin: 2rem 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;

  &.wide {
    .content {
      display: grid;
      grid-template-columns: repeat(3, 1fr);

      .card {
        width: 400px;
        margin: 1rem 0;

      }
    }
  }

  ._header {
    margin: 2rem 0;
    
    h2 {
      font-weight: 400;
      font-size: 36px;
    }
  }

  .content {
    .card {
      margin: 2rem 0;

      .testimony {
        text-align: left;
        font-size: 16px;
        line-height: 2;
      }

      .testifier{
        padding: 1rem 0;
        font-weight: 500;
      }
    }
  }
}
</style>