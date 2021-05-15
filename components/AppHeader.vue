<template>
  <div class="header">
    <h1 class="header-title">Jet66</h1>
    <ul>
      <li>
        <nuxt-link class="nav-item" to="/">Home</nuxt-link>
        <nuxt-link class="nav-item" to="/about">About</nuxt-link>
        <nuxt-link class="nav-item" to="/jokes">Jokes</nuxt-link>
        <nuxt-link class="nav-item" to="/contact">Contact</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>
<style>
.header {
  padding: 20px;
  display: flex;
  justify-content: space-between;
  margin-bottom: 1rem;
  padding-bottom: 1rem;
  border-bottom: 1px dotted #ccc;
}
.header-title {
  color: red;
  font-size: 3rem;
}
.header ul{
  display:flex;
}
.header a{
  display: inline-block;
  background:#333333;
  color:#fff;
  padding:0.5rem 2rem;
  margin-right:0.5 rem;
  text-decoration: none;
}
</style>
