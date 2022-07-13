<template>
  <div class="offerings" id="offerings">
    <h2>Our Offerings</h2>
    <div class="offer">
      <div class="card" v-for="item in offerings" :key="item.id">
        <div class="_image">
          <img :src="item.imgLink" :alt="'image of offerings '+item.name">
        </div>
        <div class="_details">
          <span class="name"> {{item.name}} </span>
          <NuxtLink :to="item.link">Learn More</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      offerings: [
        {
          id: 0,
          imgLink: '_nuxt/assets/img/SMART.jpg',
          name: 'Interactive Smart Board',
          link: '/offerings/smartboard'
        },
        {
          id: 1,
          imgLink: '_nuxt/assets/img/m-c-e.svg',
          name: 'Microsoft Certified Educator',
          link: '/offerings/mce'
        },
        {
          id: 2,
          imgLink: 'https://imgs.search.brave.com/TUTT8KbZa_De-o_IH1ZdN6T2w5Dco7WQCreTbOiA2is/rs:fit:1200:1200:1/g:ce/aHR0cHM6Ly9zdGF0/aWMuc2tpbGxzaGFy/ZS5jb20vdXBsb2Fk/cy92aWRlby90aHVt/Ym5haWxzLzhjNGFh/ZmIxYzQzNDk4NGU2/MjNkZTRhOTE3ZTY3/NmFiL29yaWdpbmFs',
          name: 'Programming Courses (coming soon)',
          link: '#'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.offerings {
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

  .offer {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;

    .card {
      ._image {
        img {
          width: 100%;
          height: 400px;
          object-fit: contain;
        }
      }

      ._details {

        span {
          display: block;
          padding: 1rem 0;
          font-size: 18px;
          font-weight: 400;
        }

        a {
          display: block;
          margin: auto;
          width: fit-content;
          padding: 12px 16px;
          background: $primary;
          text-decoration: none;
          color: $light;
          cursor: pointer;
          border: none;
          font-size: inherit;
          border-radius: 4px;

          &:hover {
            background-image: linear-gradient(rgba(255, 77, 0, 0.4) 0 0);
          }
        }
      }
    }
  }
  
  @media screen and (max-width: 900px) {
    .products {
      grid-template-columns: repeat(2, 1fr);
      margin: 1rem 0;
    }
  }

  @media screen and (max-width: 728px) {
    padding: 1rem;
    display: block;

    .products {
      display: block;
      
      .card {
        margin: 1rem 0;
      }
    }

    h2 {
      font-weight: 400;
      font-size: 36px;
      padding: 1rem 0;
    }

  }
}
</style>