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
          imgLink: 'https://imgs.search.brave.com/g0tnrYlMOjJffhs_zi0UoRyPgoTpuuZZxR_x0kTtRDM/rs:fit:542:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5r/M01zREJaamZxVllY/WkVvYko4NTRRSGFH/ZSZwaWQ9QXBp',
          name: 'Interactive Smart Board',
          link: '/services/#isb'
        },
        {
          id: 1,
          imgLink: 'https://imgs.search.brave.com/IMNk4aJFLgIiHmeIog4r-ZavgpP7pKCKyKfDNR7iwCs/rs:fit:1200:1200:1/g:ce/aHR0cHM6Ly9pMi53/cC5jb20vdGVjaG1v/cmFuLmNvbS93cC1j/b250ZW50L3VwbG9h/ZHMvMjAxMy8xMS9D/b21wdXRlci1MYWIu/anBnP2ZpdD0zODcy/JTJDMjU5MiZzc2w9/MQ',
          name: 'ICT Lab',
          link: '/services/#ict-lab'
        },
        {
          id: 2,
          imgLink: 'https://forrit-cms-msedu-web-consumables.azureedge.net/media/8806824e-543b-48ba-8567-aeaef11f67dc/1920-Panel1-FeatureHeader-Academy.jpg',
          name: 'Microsoft Imagine Academy',
          link: '/services/#mia'
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
    .offer {
      grid-template-columns: repeat(2, 1fr);
      margin: 1rem 0;
    }
  }

  @media screen and (max-width: 728px) {
    padding: 1rem;
    display: block;

    .offer {
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