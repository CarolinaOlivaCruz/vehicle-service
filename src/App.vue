import Header from './components/Navbar.vue';
<template>
  <Header />
  <main id="main">
    <router-view></router-view>
  </main>
</template>

<script>
import Header from "./components/Header";

export default {
  data: function () {
    return {
      app_name: "Vehicle Service",
    };
  },
  components: {
    Header,
  },
};
</script>

<style>
* {
  font-family: Helvetica;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  width: 100%;
}

a {
  text-decoration: none;
}

button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  text-align: center;
}

input,
select,
fieldset {
  border: none;
  outline: none;
}

ul {
  list-style-type: none;
}

#main {
  width: 80%;
  margin: 0 auto;
  margin-top: 15px;
}
</style>
