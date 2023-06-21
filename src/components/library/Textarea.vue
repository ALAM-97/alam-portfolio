<template>
  <div class="input-container">
    <label for="textarea" class="label">{{ label }}</label>
    <textarea placeholder="Enter your message" />
    <div class="underline" />
  </div>
</template>

<script>
export default {
  name: "AlamTextarea",
  props: ["label"],
};
</script>

<style scoped lang="scss">
.input-container {
  position: relative;
  margin: 50px 0;
  width: 650px;
  textarea {
    font-size: 1.25rem;
    border: none;
    background-color: transparent;
    border-bottom: 2px solid #000;
    outline: none;
    width: 100%;
    font-family: Montserrat;
    height: 4rem;
    vertical-align: middle;
  }
  .label {
    position: absolute;
    top: -30px;
    left: 0;
    color: #585858;
    transition: all 0.3s ease;
    pointer-events: none;
  }
}
</style>
