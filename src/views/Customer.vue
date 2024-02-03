<template>
  <div class="customer">
    <div>
      <router-link to="/"> Voltar </router-link>
      <h1>Fulano</h1>
      <Button width="50px" text="Editar" color="" />
    </div>
    <div>
      <article>
        name: string, email: string, phone: number, gender: string, birth: date,
        cpf: number, address: string,
      </article>
    </div>
  </div>
</template>

<script>
import Button from "@/components/Button.vue";

export default {
  components: {
    Button,
  },
};
</script>
