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
      type="select"
      label="Gênero"
      :options="selectGender"
      :multiple="False"
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
    <div id="container-form-vehicle">
      <Fieldset
        :isInput="true"
        placeholder="Tipo do veículo"
        type="text"
        label="Tipo do veículo"
      />
      <Fieldset :isInput="true" placeholder="Placa" type="text" label="Placa" />
      <Fieldset :isInput="true" placeholder="Marca" type="text" label="Marca" />
      <Fieldset
        :isInput="true"
        placeholder="Modelo"
        type="text"
        label="Modelo"
      />
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
      <Fieldset
        :isInput="false"
        placeholder=""
        type="checkbox"
        label="Serviço a ser realizado"
        :options="selectedServices"
        :multiple="true"
      />
    </div>
    <div id="container-button">
      <Button
        width="100%"
        clickType=""
        :onclick="handleClick"
        text="Adicionar outro veículo"
        color=""
      />
      <Button
        width="100%"
        clickType=""
        :onclick="handleSaveClick"
        text="Salvar"
        color="#a7a3a3"
      />
    </div>
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
      selectedServices: [
        { value: "Troca de Óleo", label: "Troca de Óleo", concluded: false },
        { value: "Troca de Pneu", label: "Troca de Pneu", concluded: false },
      ],
      selectGender: [
        { value: "Masculino", label: "Masculino" },
        { value: "Feminino", label: "Feminino" },
        { value: "Prefiro não dizer", label: "Prefiro não dizer" },
      ],
    };
  },
  methods: {
    handleSaveClick() {
      console.log("Form saved!");

      console.log(this.selectedServices);
    },
    
  },
};
</script>

<style>
#container-form-vehicle {
  margin: 15px 0;
  border: 1px solid #a7a3a3;
  border-radius: 8px;
  padding: 5px;
}

#container-button {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
</style>
