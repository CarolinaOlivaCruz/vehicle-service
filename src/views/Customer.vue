<template>
  <div id="container-customer">
    <router-link to="/"> Voltar </router-link>
    <div class="customer-menu">
      <h2>Nome Sobrenome</h2>
      <button @click.prevent="handleClick">Editar</button>
    </div>
    <div class="container-data">
      <article>
        <p>email: string,</p>
        <p>phone: number,</p>
        <p>gender: string,</p>
        <p>birth: date,</p>
        <p>cpf: number,</p>
        <p>address: string,</p>
      </article>

      <article>
        <h4>Veículos:</h4>
        <ul>
          <li>
            <p>type: string,</p>
            <p>plate: string,</p>
            <p>model: string,</p>
            <p>brand: string,</p>
            <p>yearOfManufacture: number,</p>
          </li>
          <li>
            <p>type: string,</p>
            <p>plate: string,</p>
            <p>model: string,</p>
            <p>brand: string,</p>
            <p>yearOfManufacture: number,</p>
          </li>
          <li>
            <p>type: string,</p>
            <p>plate: string,</p>
            <p>model: string,</p>
            <p>brand: string,</p>
            <p>yearOfManufacture: number,</p>
          </li>
        </ul>
      </article>
    </div>
  </div>
  <Modal :showModal="isModalVisible" @close-modal="closeModal">
    <FormCustomer />
  </Modal>
</template>

<script>
import Modal from "@/components/Modal.vue";
import FormCustomer from "../../src/components/FormCustomer.vue";

export default {
  components: {
    Modal,
    FormCustomer,
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
#container-customer a {
  width: 100%;
  text-align: center;
  margin: 15px 0;
}

.customer-menu {
  width: 100%;
  display: flex;
  align-items: center;
  margin: 15px 0;
  justify-content: space-between;
}

.container-data {
  width: 100%;
  margin: 15px 0;
  border: 1px solid #f5f5f5;
  padding: 10px;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.container-data article h4 {
  margin: 15px 0;
}

.container-data article p {
  margin: 5px 0;
}

.container-data article ul{
  display: flex;
  flex-direction: column;
  gap: 20px;
}
</style>
