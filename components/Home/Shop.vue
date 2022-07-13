<template>
  <div class="shop" id="shop">
    <h2>Quick Shop</h2>
    <div class="products">
      <div class="card" v-for="item in products" :key="item.id">
        <div class="_image">
          <img :src="item.imgLink" :alt="item.alt">
        </div>
        <div class="_details">
          <span class="name">{{item.name}}</span>
          <a href="tel:+2348023178729" class="cta">Call to Order</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      products: [
        {
          id: 0, 
          imgLink: 'https://res.cloudinary.com/dsgvwxygr/image/upload/v1657045225/trackit/picture_of_pc_trackit_g19cu0.jpg',
          alt: 'image_of_pc_trackit',
          name: 'HP - 15.6" Touch-Screen Laptop - Intel Core i7 - 16GB Memory - 512GB SSD - Natural Silver'
        },
        {
          id: 1, 
          imgLink: 'https://res.cloudinary.com/dsgvwxygr/image/upload/v1657046227/trackit/hard_drive_images_trackit_bczqkj.jpg',
          alt: 'image_of_harddrive_trackit',
          name: 'Seagate - Expansion 100GB - 2TB External USB 3.0 Portable Hard Drive with Rescue Data Recovery Services - Black'
        },
        {
          id: 2, 
          imgLink: 'https://res.cloudinary.com/dsgvwxygr/image/upload/v1657046428/trackit/micorsoft_office_365_trackit_jdqyfg.jpg',
          alt: 'image_of_microsoft office 365',
          name: 'Microsoft 365 Business Standard (1 Person) (12-Month Subscription) - Android, Apple iOS, Chrome, Mac OS, Windows [Digital]'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.shop {
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

  .products {
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
        .cta {
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