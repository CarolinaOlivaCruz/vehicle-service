<template>
  <div class="home">
    <Button
      width="100%"
      @click.prevent="handleClick"
      text="Cadastrar novo cliente"
      color=""
    />
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
import FormCustomer from "../../src/components/FormCustomer.vue";
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
#home {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
