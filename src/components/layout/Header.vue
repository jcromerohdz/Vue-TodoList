<template >
  <header class="header">
    <h1>Todo List</h1>
    <div>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Heder"
}
</script>

<style scoped>
  .header {
    background: #333;
    color: #ffff;
    text-align: center;
    padding: 10px;
  }

  .header a {
    color: #ffff;
    padding-right: 5px;
    text-decoration: none;
  }


</style>