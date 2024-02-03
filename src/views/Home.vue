<template>
  <div class="home">
    <div class="container-button">
      <Button
        width="100%"
        @click.prevent="handleClick"
        text="Cadastrar novo cliente"
        color=""
      />
    </div>
    <Fieldset :isInput="true" placeholder="Buscar..." type="text" label="" />
    <ul>
      <CardCustomer />
      <CardCustomer />
      <CardCustomer />
      <CardCustomer />
    </ul>
  </div>
  <Modal :showModal="isModalVisible" @close-modal="closeModal">
    <FormCustomer />
  </Modal>
</template>

<script>
import FormCustomer from "@/components/FormCustomer.vue";
import Fieldset from "@/components/Fieldset.vue";
import Button from "@/components/Button.vue";
import Modal from "@/components/Modal.vue";
import CardCustomer from "@/components/CardCustomer.vue";

export default {
  components: {
    Button,
    FormCustomer,
    Fieldset,
    Modal,
    CardCustomer,
  },
  data() {
    return {
      isModalVisible: false,
    };
  },
  methods: {
    handleClick() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    },
  },
};
</script>

<style>
.container-button {
  margin: 30px auto;
}

.home ul {
  margin: 15px 0;
  border: 1px solid #f5f5f5;
  padding: 10px;
  border-radius: 8px;
}

@media (min-width: 750px) {
  .container-button {
    max-width: 200px;
    margin: 30px auto;
  }
}
</style>
