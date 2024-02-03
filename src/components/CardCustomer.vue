<template>
  <li>
    <div id="card">
      <router-link to="/customer">
        <h4>Nome Sobrenome</h4>
        <span>nº de veículos</span>
        <span>Ver</span>
      </router-link>
    </div>
  </li>
</template>

<script>
export default {
  name: "CardCustomer",
  // props: {

  // }
};
</script>

<style>
#card {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 15px 0;
  border: 1px solid #f5f5f5;
  padding: 10px;
  border-radius: 8px;
}

#card a {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
