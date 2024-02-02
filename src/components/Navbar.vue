<template>
  <div id="nav">
    <router-link to="/">logo</router-link>
    <div>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
#nav {
  margin: 0 auto;
  background-color: #ffff;
  border-bottom: 1px solid #f5f5f5;
  padding: 15px 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

#nav a {
  color: #000;
  text-decoration: none;
  margin: 12px;
  transition: 0.5s;
}

#nav a:hover {
  color: #fff;
}
</style>
