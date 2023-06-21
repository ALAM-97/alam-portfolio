<template>
  <div class="input-container">
    <input type="text" id="input" required />
    <label for="input" class="label">{{ label }}</label>
    <div class="underline" />
  </div>
</template>

<script>
export default {
  name: "AlamInput",
  props: ["label"],
};
</script>

<style scoped>
.input-container {
  position: relative;
  margin: 50px 0;
  width: 300px;
}

.input-container input[type="text"] {
  font-size: 1.25rem;
  width: 100%;
  border: none;
  border-bottom: 2px solid #585858;
  padding: 0.3125rem 0;
  background-color: transparent;
  outline: none;
  font-family: Montserrat;
}

.input-container .label {
  position: absolute;
  top: 0;
  left: 0;
  color: #585858;
  transition: all 0.3s ease;
  pointer-events: none;
}

.input-container input[type="text"]:focus ~ .label,
.input-container input[type="text"]:valid ~ .label {
  top: -1.25rem;
  font-size: 1.25rem;
  color: #333;
}

.input-container .underline {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 2px;
  width: 100%;
  background-color: #333;
  transform: scaleX(0);
  transition: all 0.3s ease;
}

.input-container input[type="text"]:focus ~ .underline,
.input-container input[type="text"]:valid ~ .underline {
  transform: scaleX(1);
}
</style>
