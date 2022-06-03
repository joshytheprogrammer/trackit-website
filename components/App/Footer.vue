<template>
  <footer>
    <div class="address">
      <h3>Address</h3>
      <p>1 Joseph Street, Lagos Island 102273</p>
    </div>
    <div class="contacts">
      <h3>Contacts</h3>
      <p>08088985577</p>
      <p><a href="mailto:kingsleyn24@yahoo.com">kingsleyn24@yahoo.com</a></p>
    </div>
    <div class="attribution">
      <h3>Track IT Nigeria Limited</h3>
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
  width: 100%;
  max-height: fit-content;
  
  box-shadow: 0px -2px 2px -2px;
  margin-top: 1rem;

  padding: 8px 0 0 0;
  text-align: center;

  font-size: 12px;
  font-weight: 400;

  position: relative;

  display: grid;
  grid-template-columns: repeat(3, 1fr);

  @media screen and (max-width: 900px) {
    grid-template-columns: repeat(2,1fr);
  }

  @media screen and (max-width: 728px) {
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
    font-size: 16px;
    font-weight: 400;
    padding: 5px 0;
  }

  a {
    color: $dark;
    font-weight: 500;
  }
}
</style>