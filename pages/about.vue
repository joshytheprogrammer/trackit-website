<template>
  <div class="about">
    <section>
      <h1>Who we are</h1>
      <p>Track IT Limited is a Microsoft Authorized Education Partner, an IT solution provider and a trail blazer in the Microsoft Education Arena. Track IT Limited having identifed the gap in IT education in Nigeria has partnered with Microsoft a Global Software Company to implement and deploy Microsoft Education Labs across the country. (Track IT have deployed in education the following: IT Labs, Language Labs, E-Library Labs, Computer based testing (CBT) Labs, E-learning Suite, Microsoft Imagine Academy, Cisco Academy, etc).</p>
    </section>
    <section>
      <h1>I.T. Solutions Company</h1>
      <p>We setup in schools world class ICT infrastructure with workstations, backup power, internet, e-library, learning management system and online training centre at highly reduced cost. We deliver IT training with the right curriculum, by certfied personnel to impact right IT skills to students to enable them obtain international certification for each specific skill. (NOTE: This is lacking even in modern computer schools). We also enable Primary, Secondary and Tertiary School Students obtain Microsoft Certfication and knowledge at highly discounted price within their school environment.</p>
    </section>

    <section>
      <button @click="$router.push('/quotation')">Get a Quote</button>
    </section>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.about {
  padding: 1rem;

  section {
    padding: 1rem;
    
    h1 {
      font-size: 24px;
      font-weight: 400;
    }

    p {
      font-size: 16px;
      font-weight: 300;
    }

    button {
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
    }
  }
}
</style>