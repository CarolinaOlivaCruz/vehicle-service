<template>
  <div class="home">
    <Button
      width="100%"
      clickType=""
      :onclick="handleClick"
      text="Registrar novo proprietário"
    />
    <Fieldset :isInput="true" placeholder="Buscar..." type="text" label="" />
    <ul>
      <li>Fulano</li>
    </ul>
  </div>
  <RegisterOwner v-if="showRegisterOwner" />
</template>

<script>
import RegisterOwner from "../../src/components/RegisterOwner.vue";
import Fieldset from "@/components/Fieldset.vue";
import Button from "@/components/Button.vue";

export default {
  components: {
    Button,
    RegisterOwner,
    Fieldset,
  },
  data() {
    return {
      showRegisterOwner: false,
    };
  },
  methods: {
    handleClick() {
      this.showRegisterOwner = true;
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
