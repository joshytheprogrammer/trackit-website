<template>
  <div class="quote-form">
    <h1>GET QUOTATION</h1>
    <p>Fill the form below. The quotation will be sent by mail or sms.</p>
    <form @submit.prevent="validateForm">
      <div class="form-group">
        <label>BUSINESS NAME *</label>
        <input type="text" class="form-control" required>
      </div>
      <div class="form-group">
        <label>BUSINESS EMAIL *</label>
        <input type="text" class="form-control" v-model="data.email" required>
        <p class="error" v-if="error.email">{{error.email}}</p>
      </div>
      <div class="form-group">
        <label>BUSINESS TELEPHONE *</label>
        <input type="text" class="form-control" v-model="data.phone" required>
        <p class="error" v-if="error.phone">{{error.phone}}</p>
      </div>
      <div class="form-group">
        <label>BUSINESS LOCATION *</label>
        <input type="text" class="form-control" required>
      </div>
      <div class="form-group">
        <label>WHAT AREA ARE YOU MOST INTERESTED IN? *</label>
        <select class="form-control" required>
          <option value="" disabled hidden selected>How can we help you?</option>
          <option value="isb" :selected="params === 'isb'">Interactive Smart Board</option>
          <option value="mce" :selected="params === 'mce'">Microsoft Certified Educator</option>
          <option value="ict-l" :selected="params === 'ict-l'">ICT Lab</option>
          <option value="mia" :selected="params === 'mia'">Microsoft Imagine Academy</option>
          <option value="s-t" :selected="params === 's-t'">Student Training</option>
        </select>
      </div>
      <div class="form-group">
        <label>TELL US MORE *</label>
        <textarea class="form-control lg" placeholder="This should include a rough estimate of the amount/quantity of the product you might need." required></textarea>
      </div>
      <div class="form-group QWDED">
        <input class="btn" type="submit" value="Submit" :disabled="loading">
        <div class="loader" v-if="loading"></div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loading: false,
      params: this.$route.query.interest,
      data: {
        email: ''
      },
      error: {
        email: null,
        phone: null,
      }
    }
  },
  methods: {
    async submit() {
     this.loading = false
     console.log('success')
    },
    validateForm() {
      this.loading = true
      let emailPattern = /(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:(2(5[0-5]|[0-4][0-9])|1[0-9][0-9]|[1-9]?[0-9]))\.){3}(?:(2(5[0-5]|[0-4][0-9])|1[0-9][0-9]|[1-9]?[0-9])|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])/;

      let telPattern = /^^(?:(?:(?:\+?234(?:\h1)?|01)\h*)?(?:\(\d{3}\)|\d{3})|\d{4})(?:\W*\d{3})?\W*\d{4}$/;

      // Test email
      if(!this.data.email.match(emailPattern)){
        this.error.email="Email is improperly formatted"
      }else{
        this.error.email = null
      }

      if(!this.data.phone.match(telPattern)){
        this.error.phone="The Phone Number is improperly formatted"
      }else{
        this.error.phone = null
      }

      // Check if no errors exist

      // if(this.error.email.length === 0 || this.error.phone.length === 0){
      //   this.submit()
        
      //   return
      // }else {
      //   this.loading = false
      //   return
      // }

      this.loading = false
    }
  }
}
</script>

<style lang="scss" scoped>
.quote-form {
  padding: 1rem;
  
  h1 {
    font-weight: 500;
    font-size: 36px;
  }

  p {
    font-weight: 400;
    font-size: 16px;
    padding: 1rem 0;
  }

  form {
    .form-group {
      display: flex;
      flex-direction: column;

      label {
        text-transform: uppercase;
        font-weight: 500;
        font-size: 12px;
        padding: 0.2rem 0 0.2rem 0;
      }

      .form-control {
        height: 48px;
        background: $grey;
        color: $dark;
        border: none;
        outline: 1px solid $dark;
        border-radius: 4px;
        padding: 0 0 0 0.2rem;
        margin-bottom: 1rem;
        transition: background .2s linear, outline .1s ease-in-out;
        
        font-size: 16px;
        font-weight: 400;

        &.lg {
          height: 10rem; // 160px;
          padding: 0.2rem;
        }

        &:focus {
          outline: 2px solid $dark;
          background: $light;
        }
      }

      p.error {
        text-transform: uppercase;
        font-weight: 500;
        font-size: 12px;
        padding: 0.2rem;
        margin: 0.2rem 0;
        background: $red;
        color: $light;
        width: fit-content;
        border-radius: 4px;
        transition: .2s ease-in-out;
      }

      &.QWDED {
        display: flex;
        justify-content: space-between;
        flex-direction: row;
        align-items: center;

        .btn {
          background: $primary;
          color: $light;
          border: none;
          font-size: 16px;
          font-weight: 400;
          border-radius: 4px;
          height: fit-content;
          width: fit-content;
          padding: 8px 12px;
          margin: 1rem 0;
          cursor: pointer;
          transition: box-shadow .2s ease-in-out, padding .2s linear;

          &:hover {
            box-shadow: 0px 8px 8px $dark;
            padding: 9px 16px;
          }

          &:disabled {
            cursor: not-allowed;
            opacity: .6;
          }
        }

        .loader {
          border: 5px solid $light; /* Light grey */
          border-top: 5px solid $dark; /* Blue */
          border-radius: 50%;
          width: 20px;
          height: 20px;
          animation: spin .9s linear infinite;
        }

        @keyframes spin {
          0% { transform: rotate(0deg); }
          100% { transform: rotate(360deg); }
        }
      }
    }
  }
}
</style>