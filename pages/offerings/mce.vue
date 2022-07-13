<template>
  <div class="mce">
    <div class="header">
      <h1>The Microsoft Certified Educator Program</h1>
      <img src="../../assets/img/microsoft-logo.png" alt="microsoft logo on mce page">
    </div>
    <div class="details">
      <p>The Microsoft Certified Educator Program is a professional development program that bridges the gap between technology skills and innovative teaching. Educators holding a Microsoft Certified Educator certification can prove they have the skills needed to provide rich, customized learning experiences for their students that incorporate critical 21st century skills using Microsoft tools.</p>
      
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.mce {
  width: 80%;
  margin: 2rem auto;
  border-radius: 12px;
  box-shadow: 2px 2px 2px 2px $dark;

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
    border-bottom: 1px solid $dark;

    h1 {
      font-size: 32px;
      font-weight: 400;
    }

    h1, img {
      margin: 0 1rem;
    }
  }
}
</style>