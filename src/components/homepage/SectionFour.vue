<template>
  <div class="page">
    <div class="page-content">
      <div class="left-content">
        <div class="text">
          <div class="title">
            <h2>My work</h2>
            <img src="../../assets/img/line.svg" />
          </div>
          <p>
            Check out the <br />
            projects I made.
          </p>
        </div>
        <Button text="See my work" />
        <img
          class="pattern"
          alt="pattern"
          src="../../assets/img/pattern-41.png"
        />
      </div>
      <div class="right-content">
        <div class="text">
          <div class="title">
            <h2>Contact me</h2>
            <img src="../../assets/img/line.svg" />
          </div>
          <p>
            Got a project to propose me? <br />
            Let’s connect!
          </p>
          <div class="form">
            <Input label="Your name" />
            <Input label="Your e-mail address" />
          </div>
          <Textarea label="Your message" />
        </div>
        <Button text="Send message" />
      </div>
    </div>
  </div>
</template>

<script>
import Button from "../library/Button.vue";
import Input from "../library/Input.vue";
import Textarea from "../library/Textarea.vue";

export default {
  name: "SectionFour",
  components: { Button, Input, Textarea },
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
  .page-content {
    align-items: center;
    padding: 6.25rem 0;
    .left-content,
    .right-content {
      padding: 5rem;
      height: 70%;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
    .left-content {
      position: relative;
      width: 45%;
      border-right: 5px solid #fffd2a;
      margin-right: 6.25rem;
      .title {
        position: relative;
        h2 {
          position: relative;
          z-index: 10;
        }
        img {
          position: absolute;
          left: 0;
          top: 50%;
          transform: translateY(-10%);
          width: 58%;
        }
      }
      .text {
        flex-grow: 1;
      }
      .pattern {
        position: absolute;
        bottom: 27%;
        right: 22%;
        width: 35%;
      }
    }
    .right-content {
      width: 55%;
      .title {
        position: relative;
        h2 {
          position: relative;
          z-index: 10;
        }
        img {
          position: absolute;
          left: 0;
          top: 50%;
          transform: translateY(-10%);
          width: 60%;
        }
      }
      .text {
        flex-grow: 1;
      }
      .form {
        display: flex;
        gap: 2.5rem;
      }
    }
  }
}
</style>
