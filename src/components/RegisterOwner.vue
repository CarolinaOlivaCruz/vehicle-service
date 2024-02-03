<template>
  <div id="container-register">
    <form>
      <Fieldset
        :isInput="true"
        placeholder="Nome Exemplo"
        type="name"
        label="Nome Completo"
      />
      <Fieldset
        :isInput="true"
        placeholder="email@email.com"
        type="email"
        label="Email"
      />
      <Fieldset
        :isInput="true"
        placeholder="81 992547202"
        type="phone"
        label="Telefone"
      />
      <Fieldset
        :isInput="false"
        placeholder="Selecione"
        type=""
        label="Sexo"
        :options="selectOptions"
      />
      <Button
      width="100%"
      clickType=""
      :onclick="handleClick"
      text="Salvar"
    />
    </form>
  </div>
</template>

<script>
import Fieldset from "./Fieldset.vue";
import Button from "./Button.vue";

export default {
  name: "RegisterOwner",
  components: {
    Fieldset,
    Button,
  },
  data() {
    return {
      selectOptions: [
        { value: "Masculino", label: "Masculino" },
        { value: "Feminino", label: "Feminino" },
        { value: "Nenhum", label: "Nenhum" },
      ],
    };
  },
};
</script>
