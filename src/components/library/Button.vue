<template>
  <button class="button">
    <div class="content">
      {{ text }}
      <img src="../../assets/img/arrow.svg" />
    </div>
  </button>
</template>

<script>
export default {
  name: "AlamButton",
  props: ["text"],
};
</script>

<style scoped lang="scss">
.button {
  width: 100%;
  max-width: 500px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  text-transform: uppercase;
  background-color: transparent;
  padding: 20px 0px;
  border: 2px solid #000;
  font-size: 1.25rem;
  font-family: Montserrat;
  font-weight: 600;
  -webkit-transition: ease-out 0.4s;
  -moz-transition: ease-out 0.4s;
  transition: ease-out 0.4s;
  &:hover {
    box-shadow: inset 500px 0 0 0 #000;
    color: #fff;
    img {
      transition: ease-out 0.5s;

      filter: invert(100%);
    }
  }
  .content {
    display: flex;
    align-items: center;
    img {
      margin-left: 10px;
    }
  }
}
</style>
