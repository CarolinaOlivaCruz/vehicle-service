<template>
  <div id="container-modal">
    <div class="modal-content">
        <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
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
  padding-top: 450px;
}

.modal-content {
  margin: 40px 0;
  background: #ffff;
  padding: 20px;
  width: 90%;
  max-width: 600px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  overflow-y: auto;
}

.modal-content::-webkit-scrollbar {
  width: 10px;
}

.modal-content::-webkit-scrollbar-thumb {
  background-color: #888;
}

.modal-content::-webkit-scrollbar-track {
  background-color: #f1f1f1;
}

</style>