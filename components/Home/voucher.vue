<template>
  <div class="vouchers" id="vouchers">
    <h2>Our Vouchers</h2>
    <div class="voucher">
      <div class="card" v-for="item in offerings" :key="item.id">
        <div class="_image">
          <img :src="item.imgLink" :alt="'image of voucher '+item.name">
        </div>
        <div class="_details">
          <span class="name"> {{item.name}} </span>
          <NuxtLink :to="item.link">Book Now</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      vouchers: [
        {
          id: 0,
          imgLink: '',
          name: '',
          to: '#'
        },
        {
          id: 1,
          imgLink: '',
          name: '',
          to: '#'
        },
        {
          id: 3,
          imgLink: '',
          name: '',
          to: '#'
        },
        
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

</style>