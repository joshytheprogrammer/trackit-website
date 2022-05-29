<template>
  <div class="contact-form" :class="{'wide' : !mobile}">
    <h1>Contact Form</h1>
    <form>
      <div class="form-group">
        <label>BUSINESS NAME *</label>
        <input type="text" class="form-control" required>
      </div>
      <div class="form-group">
        <label>BUSINESS EMAIL *</label>
        <input type="text" class="form-control" required>
      </div>
      <div class="form-group">
        <label>MESSAGE *</label>
        <textarea class="form-control lg" required></textarea>
      </div>
      <div class="form-group QWDED">
        <input class="btn" type="submit" value="Submit">
      </div>
    </form>
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
.contact-form {
  padding: 2rem 1rem;
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