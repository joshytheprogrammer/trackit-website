<template>
  <div class="quote-form">
    <h1>GET QUOTATION</h1>
    <p>Fill the form below. The quotation will be sent by mail or sms.</p>
    <form>
      <div class="form-group">
        <label>BUSINESS EMAIL *</label>
        <input type="text" class="form-control">
      </div>
      <div class="form-group">
        <label>BUSINESS TELEPHONE *</label>
        <input type="text" class="form-control">
      </div>
      <div class="form-group">
        <label>WHAT AREA ARE YOU MOST INTERESTED IN? *</label>
        <select class="form-control">
          <option value="" disabled selected hidden>How can we help you?</option>
          <option value="">Interactive Smart Board</option>
          <option value="">Microsoft Certified Educator</option>
          <option value="">ICT Lab</option>
          <option value="">Microsoft Imagine Academy</option>
          <option value="">Student Training</option>
        </select>
      </div>
      <div class="form-group">
        <label>TELL US MORE *</label>
        <textarea class="form-control lg"></textarea>
      </div>
      <div class="form-group">
        <input class="btn" type="button" value="Submit">
      </div>
    </form>
  </div>
</template>

<script>
export default {

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

      .btn {
        background: $dark;
        color: $light;
        border: none;
        font-size: 16px;
        font-weight: 400;
        border-radius: 4px;
        height: fit-content;
        width: fit-content;
        padding: 8px 12px;
        cursor: pointer;
        transition: box-shadow .2s ease-in-out, padding .2s linear;

        &:hover {
          box-shadow: 0px 8px 8px $primary;
          padding: 12px 16px;
        }
      }
    }
  }
}
</style>