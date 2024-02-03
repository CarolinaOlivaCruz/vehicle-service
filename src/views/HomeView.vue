<template>
  <div class="home">
    <Button
      width="100%"
      clickType=""
      :onclick="handleClick"
      text="Cadastrar novo cliente"
    />
    <Fieldset :isInput="true" placeholder="Buscar..." type="text" label="" />
    <ul>
      <li>Fulano</li>
    </ul>
  </div>
  <RegisterCustomer v-if="showRegisterCustomer" />
</template>

<script>
import RegisterCustomer from "../../src/components/RegisterCustomer.vue";
import Fieldset from "@/components/Fieldset.vue";
import Button from "@/components/Button.vue";

export default {
  components: {
    Button,
    RegisterCustomer,
    Fieldset,
  },
  data() {
    return {
      showRegisterCustomer: false,
    };
  },
  methods: {
    handleClick() {
      this.showRegisterCustomer = true;
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
