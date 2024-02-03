<template>
  <header id="header">
    <h2>VEHICLE SERVICE</h2>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style>
#header {
  text-align: center;
  background-color: #ffff;
  border-bottom: 1px solid #f5f5f5;
  padding: 30px 0;
}

#header a {
  color: #000;
  text-decoration: none;
  transition: 0.5s;
  font-weight: bold;
}

#header a:hover {
  color: #fff;
}
</style>
