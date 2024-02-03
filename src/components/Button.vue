<template>
  <button
    id="button"
    :style="{ width: width, background: color, border: color }"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    width: {
      type: String,
      default: "auto",
    },
    text: {
      type: String,
      default: "Clique aqui",
    },
    color: {
      type: String,
      default: "",
    },
  },
};
</script>

<style>
#button {
  padding: 10px 0;
  border: 1px solid #f5f5f5;
  border-radius: 8px;
  background: #f5f5f5;
  margin: 0 auto;
}
</style>
