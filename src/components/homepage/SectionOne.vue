<template>
  <div class="page">
    <div class="page-content">
      <div class="left-content">
        <h1>
          Frontend <br />
          Developer.
        </h1>
        <p>
          I like to build solid frontend products with great user experience
          without giving up on the design.
        </p>

        <img
          class="pattern-1"
          alt="pattern-2"
          src="../../assets/img/pattern-2.png"
        />
        <img
          class="pattern-2"
          alt="pattern-1"
          src="../../assets/img/pattern-1.png"
        />
      </div>
      <div class="right-content">
        <img alt="picture" src="../../assets/img/hero-img.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionOne",
};
</script>

<style scoped lang="scss">
.page {
  background: linear-gradient(rgba(255, 253, 42, 0.9), rgba(255, 253, 42, 0.9)),
    url("../../assets/Logo.svg");
  background-color: #fffd2a;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 80%;
}
.page-content {
  .left-content,
  .right-content {
    width: 50%;
    color: #262626;
  }
  .left-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    position: relative;
    height: 100%;
    p {
      margin-bottom: 12.5rem;
    }
    .pattern-1 {
      position: absolute;
      bottom: 10%;
    }
    .pattern-2 {
      position: absolute;
      bottom: 15%;
      right: -10%;
    }
  }
  .right-content {
    align-self: center;
    margin-left: 12%;
  }
}
</style>
