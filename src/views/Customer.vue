<template>
  <div class="customer">
    <div>
      <h1>Fulano</h1>
      <Button width="50px" clickType="" :onclick="handleClick" text="Editar" />
    </div>
    <div>
      <article>
        name: string, email: string, phone: number, gender: string, birth: date,
        cpf: number, address: string,
      </article>
      <Button
        width="100%"
        clickType=""
        :onclick="handleClick"
        text="Adicionar veículo"
      />
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
