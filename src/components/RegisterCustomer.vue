<template>
  <form id="form">
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
      placeholder="Digite apenas números"
      type="phone"
      label="Telefone"
    />
    <Fieldset
      :isInput="false"
      placeholder=""
      type="text"
      label="Gênero"
      :options="selectOptions"
    />
    <Fieldset
      :isInput="true"
      placeholder="dia/mês/ano"
      type="date"
      label="Data de nascimento"
    />
    <Fieldset
      :isInput="true"
      placeholder="Digite apenas números"
      type="number"
      label="CPF"
    />
    <Fieldset
      :isInput="true"
      placeholder="Tipo do veículo"
      type="text"
      label="Tipo do veículo"
    />
    <Fieldset :isInput="true" placeholder="Placa" type="text" label="Placa" />
    <Fieldset :isInput="true" placeholder="Marca" type="text" label="Marca" />
    <Fieldset :isInput="true" placeholder="Modelo" type="text" label="Modelo" />
    <Fieldset
      :isInput="true"
      placeholder="Digite apenas número"
      type="number"
      label="Ano de fabricação"
    />
    <Fieldset
      :isInput="true"
      placeholder="dia/mês/ano"
      type="date"
      label="Data da última revisão"
    />
    <Button width="100%" clickType="" :onclick="handleClick" text="Salvar" />
  </form>
</template>

<script>
import Fieldset from "./Fieldset.vue";
import Button from "./Button.vue";

export default {
  name: "RegisterCustomer",
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

<style>
</style>
