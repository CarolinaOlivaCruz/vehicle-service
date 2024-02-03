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
    <div
      v-for="(vehicle, index) in vehicles"
      :key="index"
      id="container-form-vehicle"
    >
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
      <fieldset class="container-checkbox">
        <legend>Serviços a serem realizados</legend>
        <div v-for="(service, index) in listServices" :key="index">
          <label>
            <input type="checkbox" v-model="vehicle.services[serviceIndex]" />
            {{ service.label }}
          </label>
        </div>
      </fieldset>
      <Button
        width="100%"
        @click.prevent="removeVehicle"
        text="Remover veículo"
        color=""
      />
    </div>
    <div id="container-button">
      <Button
        width="100%"
        @click.prevent="addVehicle"
        text="Adicionar veículo"
        color=""
      />
      <Button
        width="100%"
        @click="handleSaveClick"
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
      listServices: [
        { value: "Troca de Óleo", label: "Troca de Óleo" },
        { value: "Troca de Pneu", label: "Troca de Pneu" },
        { value: "Pintura", label: "Pintura" },
        {
          value: "Instalação de alarme",
          label: "Instalação de alarme",
        },
        {
          value: "Instalação de som",
          label: "Instalação de som",
        },
      ],
      selectGender: [
        { value: "", label: "Selecione" },
        { value: "Masculino", label: "Masculino" },
        { value: "Feminino", label: "Feminino" },
        { value: "Prefiro não dizer", label: "Prefiro não dizer" },
      ],
      showVehicleFields: false,
      vehicles: [],
    };
  },
  methods: {
    handleSaveClick() {
      console.log("Form saved!");

      console.log(this.listServices);
    },
    addVehicle() {
      this.vehicles.push({
        type: "",
        plate: "",

        services: this.listServices.map((service) => ({
          ...service,
          concluded: false,
        })),
      });
    },
    removeVehicle() {
      this.vehicles.pop();
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

.container-checkbox {
  width: 100%;
  margin: 15px 0;
  border: 1px solid #f5f5f5;
  padding: 10px 5px;
  border-radius: 8px;
}

.container-checkbox legend {
  padding: 0 5px;
}
</style>
