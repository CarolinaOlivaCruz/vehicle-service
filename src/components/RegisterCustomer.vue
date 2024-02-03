<template>
  <div id="register-customer">
    <div class="modal-content">
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
        <Fieldset
          :isInput="true"
          placeholder="Placa"
          type="text"
          label="Placa"
        />
        <Fieldset
          :isInput="true"
          placeholder="Marca"
          type="text"
          label="Marca"
        />
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

        <Button
          width="100%"
          clickType=""
          :onclick="handleClick"
          text="Salvar"
        />
      </form>
    </div>
  </div>
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
#register-customer {
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 5;
  overflow-y: auto;
  padding-top: 450px;
}

.modal-content {
  margin: 20px 0;
  background: #ffff;
  padding: 20px;
  width: 90%;
  max-width: 600px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  overflow-y: auto;
}

.modal-content::-webkit-scrollbar {
  width: 10px;
}

.modal-content::-webkit-scrollbar-thumb {
  background-color: #888;
}

.modal-content::-webkit-scrollbar-track {
  background-color: #f1f1f1;
}

.modal-content form {
  margin: 0;
  padding: 0;
}
</style>
