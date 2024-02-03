<template>
  <header id="header">
    <router-link to="/">logo</router-link>
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style>
#header {
  margin: 0 auto;
  background-color: #ffff;
  border-bottom: 1px solid #f5f5f5;
  padding: 15px 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

#header a {
  color: #000;
  text-decoration: none;
  margin: 12px;
  transition: 0.5s;
}

#header a:hover {
  color: #fff;
}
</style>
