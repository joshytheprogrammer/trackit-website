<template>
  <div class="vouchers" id="vouchers">
    <h2>Exam Vouchers</h2>
    <div class="voucher">
      <div class="card" v-for="item in vouchers" :key="item.id">
        <div class="_image">
          <img :src="item.imgLink" :alt="'image of voucher '+item.name">
        </div>
        <div class="_details">
          <span class="name"> {{item.name}} </span>
          <a :href="item.to">Book Now</a>
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
          imgLink: 'https://docs.microsoft.com/en-us/media/learn/certification/badges/certification-exam.svg',
          name: 'Exam MS-900: Microsoft 365 Fundamentals',
          to: "https://api.whatsapp.com/send?phone=2348023178729&text=Hi+there.+I'm+interested+in+your+one+of+your+vouchers"
        },
        {
          id: 1,
          imgLink: 'https://docs.microsoft.com/en-us/media/learn/certification/badges/microsoft-certified-expert-badge.svg',
          name: 'Microsoft Certified Educator',
          to: "https://api.whatsapp.com/send?phone=2348023178729&text=Hi+there.+I'm+interested+in+your+one+of+your+vouchers"
        },
        {
          id: 2,
          imgLink: 'https://docs.microsoft.com/en-us/media/learn/certification/badges/microsoft-certified-fundamentals-badge.svg',
          name: 'Microsoft Certified: Power Platform Fundamentals',
          to: "https://api.whatsapp.com/send?phone=2348023178729&text=Hi+there.+I'm+interested+in+your+one+of+your+vouchers"
        },
        
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.vouchers  {
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
  
  .voucher {
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
    .voucher {
      grid-template-columns: repeat(2, 1fr);
      margin: 1rem 0;
    }
  }

  @media screen and (max-width: 728px) {
    padding: 1rem;
    display: block;

    .voucher {
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