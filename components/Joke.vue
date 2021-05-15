<template>
  <div>
    <nuxt-link :to="'jokes/' + this.id">
      <div id="Joke" class="joke">
        <p>{{ joke }}</p>
        <small>{{this.id}}</small>
      </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"],
};
</script>

<style>
.joke {
  padding: 1rem;
  border: solid 1px #ccc;
  margin: 1rem 0;
}

a{
  text-decoration: none;
}
</style>
