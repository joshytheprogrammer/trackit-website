<template>
  <footer>
    <div class="address">
      <h3>Address</h3>
      <p>40, Oyekan Street Off Ogunlana Drive Surulere, Lagos.</p>
      <p>Suite 11b, DBM plaza Wuse Zone1, Abuja.</p>
    </div>
    <div class="contacts">
      <h3>Contacts</h3>
      <p>+234 802 317 8729</p>
      <p>+234 813 117 7733</p>
      <p><a href="mailto:info@trackit.com.ng">info@trackit.com.ng</a></p>
    </div>
    <div class="attribution">
      <h3>Track IT Limited</h3>
      <p>This website was created by <a href="https://www.joshytheprogrammer.com">joshytheprogrammer</a></p>
      <p>© 2022 TRACK I.T. Limited. All Rights Reserved.</p>
    </div>
    
  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
footer {
  padding: 1rem;
  width: 100%;
  max-height: fit-content;
  
  margin-top: 2rem;

  text-align: center;

  display: grid;
  grid-template-columns: repeat(3, 1fr);

  @media screen and (max-width: 900px) {
    grid-template-columns: repeat(2,1fr);
  }

  @media screen and (max-width: 728px) {
    text-align: left;
    grid-template-columns: repeat(1,1fr);
  }

  div {
    @media screen and (max-width: 728px) {
      padding: 1rem 0;
    }
  }

  h3 {
    font-size: 24px;
    font-weight: 500;
  }

  p {
    font-size: 14px;
    font-weight: 400;
    padding: 5px 0;
  }

  a {
    color: $dark;
    font-weight: 500;
  }
}
</style>