<template>
  <div>
    <div class="container">
    <app-header></app-header>
      <Nuxt />
    </div>
  </div>
</template>
<script>
import AppHeader from "@/components/AppHeader";

export default {
  name: "layout",
  components: {
    AppHeader,
  },
};
</script>
<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body{
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height:1.6;
  background: #f4f4f4;
}
.container {
  margin: 0 auto;
  justify-content: center;
  padding:1rem 2rem;
  max-width:1000px;
  overflow:hidden;
  background:#fff;
}
ul{
  list-style:none;
}

</style>
