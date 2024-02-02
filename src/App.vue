import Navbar from './components/Navbar.vue';
<template>
  <div>
    <Navbar />
    <div>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";

export default {
  data: function () {
    return {
      app_name: "Vehicle Service",
    };
  },
  components: {
    Navbar,
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
</style>
