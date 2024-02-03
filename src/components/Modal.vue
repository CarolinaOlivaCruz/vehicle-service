<template>
  <div v-if="showModal" id="container-modal">
    <div class="modal-content">
      <Button width="20px" @click.prevent="closeModal" text="X" color="#ffff" />
      <slot></slot>
    </div>
  </div>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Modal",
  components: {
    Button,
  },
  props: {
    showModal: {
      type: Boolean,
      default: "true",
    },
  },
  methods: {
    closeModal() {
      this.$emit("close-modal");
    },
  },
};
</script>

<style>
#container-modal {
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 5;
  overflow-y: auto;
}

.modal-content {
  height: 90%;
  background: #ffff;
  padding: 20px;
  width: 90%;
  max-width: 600px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  overflow-y: auto;
}

.modal-content::-webkit-scrollbar {
  width: 0;
}

.modal-content::-webkit-scrollbar-thumb {
  background-color: #888;
}

.modal-content::-webkit-scrollbar-track {
  background-color: #f1f1f1;
}
</style>
