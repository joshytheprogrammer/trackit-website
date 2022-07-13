<template>
  <div class="mce">
    <div class="header">
      <h1>Microsoft Certified Educator Program</h1>
      <img src="../../assets/img/microsoft-logo.png" alt="microsoft logo on mce page">
    </div>
    <div class="details">
      <p>The Microsoft Certified Educator Program is a professional development program that bridges the gap between technology skills and innovative teaching. Educators holding a Microsoft Certified Educator certification can prove they have the skills needed to provide rich, customized learning experiences for their students that incorporate critical 21st century skills using Microsoft tools.</p>
      <p>
        Microsoft offers a comprehensive e-learning curriculum, 21CLD, to help educators prepare for this rigorous exam.
      </p>
      <p><b>Note:</b> The Microsoft Certified Educator exam assesses whether educators understand how to apply technology tools in the six different content domains, not whether they are proficient in using specific technology tools.</p>
      <p>
        <b>Skills measured</b>
        <ul>
          <li>Facilitate student collaboration</li>
          <li>Facilitate skilled communication</li>
          <li>Facilitate self-regulation</li>
          <li>Facilitate real-world problem solving and innovation</li>
          <li>Facilitate student use of Information and Communication Tools (ICT)</li>
          <li>Use ICT to be an effective educator</li>
        </ul>
      </p>
      <p>Job role: Developer</p>
      <p>Required exams: 62-193</p>
      <p>
        You write. <b>Technology Literacy for Educators.</b>
        You earn. <b>Microsoft Certified Educator Certificate.</b>
      </p>
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
  box-shadow: -1px -1px 2px 0px $dark;

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid $dark;

    h1 {
      font-size: 32px;
      font-weight: 400;
    }

    h1, img {
      margin: 0 1rem;
    }
  }

  .details {
    padding: 1rem;
    height: 500px;
    overflow-y: auto;

    p {
      font-size: 1.1rem;
      padding: 1.5rem 0;

      ul {
        padding: 0.5rem 1.5rem;
      }

      b {
        font-weight: 500;
      }
    }
  }

  @media screen and (max-width: 728px) {
    width: 90%;
    margin: 1rem auto;
    display: block;
    box-shadow: none;
    border: 1px solid $dark;

    .header {
      display: block;

      img {
        display: none;
      }
      
      h1 {
        font-size: 24px;
      }
    }
  }
}
</style>