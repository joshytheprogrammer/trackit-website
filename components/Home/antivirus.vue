<template>
  <div class="all-antivirus" id="antivirus">
    <h2>Antivirus</h2>
    <div class="virus">
      <div class="card" v-for="item in antivirus" :key="item.id">
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
      antivirus: [
        {
          id: 0,
          imgLink: '',
          name: '',
          link: ''
        },
        {
          id: 1,
          imgLink: '',
          name: '',
          link: ''
        },
        {
          id: 2,
          imgLink: '',
          name: '',
          link: ''
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.all-antivirus  {
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
  
  .virus {
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
    .virus {
      grid-template-columns: repeat(2, 1fr);
      margin: 1rem 0;
    }
  }

  @media screen and (max-width: 728px) {
    padding: 1rem;
    display: block;

    .virus {
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