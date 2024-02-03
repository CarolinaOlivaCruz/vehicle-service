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
      <router-link to="/customer">
        <li>Fulano</li>
      </router-link>
    </ul>
  </div>
  <Modal :showModal="isModalVisible" @close-modal="closeModal">
    <RegisterCustomer />
  </Modal>
</template>

<script>
import RegisterCustomer from "../../src/components/RegisterCustomer.vue";
import Fieldset from "@/components/Fieldset.vue";
import Button from "@/components/Button.vue";
import Modal from "@/components/Modal.vue";

export default {
  components: {
    Button,
    RegisterCustomer,
    Fieldset,
    Modal,
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
