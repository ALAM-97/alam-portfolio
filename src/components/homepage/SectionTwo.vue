<template>
  <div class="page">
    <div class="page-content">
      <div class="left-content">
        <div class="title">
          <img src="../../assets/img/line.svg" />
          <h2>About me</h2>
          <img class="pattern-1" src="../../assets/img/pattern-21.png" />
        </div>
        <p>
          I am a sociable and determined person who loves his job and is looking
          for continuous stimuli to give his best. My career in the tech field
          started in 2021, when I decided to enroll in the full-time Boolean
          Careers course, since then I have always looked for a job that allows
          me to improve and grow professionally.
        </p>
      </div>
      <div class="right-content">
        <div class="title">
          <img src="../../assets/img/line.svg" />
          <h2>My strenghts</h2>
          <img class="pattern-2" src="../../assets/img/pattern-22.png" />
        </div>
        <p>
          I’m a creative and determinated person who will do everything to
          develop the website you need, without giving up at the graphic design
          and the usability of the application.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionTwo",
};
</script>

<style scoped lang="scss">
.page {
  background: linear-gradient(
      rgba(227, 227, 227, 0.9),
      rgba(227, 227, 227, 0.9)
    ),
    url("../../assets/Logo.svg");
  background-color: #e3e3e3;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 80%;
}
.page-content {
  align-items: center;
  .left-content,
  .right-content {
    width: 100%;
  }
  .left-content {
    margin-bottom: 10%;
    .title {
      position: relative;
      h2 {
        position: relative;
      }
      img {
        position: absolute;
        left: 0;
        top: 50%;
        width: 51%;
      }
      .pattern-1 {
        position: absolute;
        top: 450%;
        left: 80%;
        width: 20%;
      }
    }
  }
  .right-content {
    margin-top: 5%;
    margin-left: 15%;
    .title {
      position: relative;
      h2 {
        position: relative;
      }
      img {
        position: absolute;
        left: 0;
        top: 50%;
        width: 68%;
      }
      .pattern-2 {
        position: absolute;
        width: 35%;
        top: 350%;
        left: 50%;
      }
    }
  }
}
</style>
