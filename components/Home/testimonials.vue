<template>
  <div class="testimonials" :class="{'wide' : !mobile}" id="testimonials">
    <div class="_header">
      <h2>Here's what our clients say</h2>
    </div>
    <div class="content">
      <div class="card">
        <p class="testimony">"Track IT is one of the most professional IT firms in Nigeria. It was a pleasure working with them."</p>
        <p class="testifier">-F.Nadah</p>
      </div>
      <div class="card">
        <p class="testimony">"Track IT is a very innovative company with a great vision for future of Nigeria."</p>
        <p class="testifier">-Ikenna Isiadinso</p>
      </div>
      <div class="card">
        <p class="testimony">"Track IT is the best software licensing company to work with and also the best company to get technology skills and certifications that will promote your tech career. The best place to learn is at Track IT."</p>
        <p class="testifier">-Oluwatosin Ajayi</p>
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
  margin: 72px 1rem;

  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;

  h2 {
    font-size: 36px;
    font-weight: 400;
    padding: 2rem 0;
  }

  .content {
    display: grid;
    gap: 1rem;
    grid-template-columns: repeat(3, 1fr);

    .card {
      margin: 2rem 0;

      .testimony {
        font-size: 16px;
        line-height: 1.85;
      }

      .testifier{
        font-size: 14px;
        font-weight: 500;
        padding: 1rem 0;
      }
    }
  }

  @media screen and (max-width: 900px) {
    .content {
      grid-template-columns: repeat(2, 1fr);
      margin: 1rem 0;
    }
  }

  @media screen and (max-width: 728px) {
    .content {
      display: block;
    } 
  }
}
</style>