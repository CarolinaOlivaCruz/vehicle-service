<template>
  <li>
    <div id="card">
      <router-link to="/customer">
        <p>Nome Sobrenome</p>
        <p>12/12/06</p>
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
  margin: 30px 0;
  border-bottom: 1px solid #f5f5f5;
}

#card a {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 10px;
}
</style>
