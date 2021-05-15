<template>
<form @submit.prevent="OnSubmit">
  <input type="text" v-model="text" placeholder="Search Jokes.."></input>
  <button type="submit">SEARCH</button>
</form>
</template>

<script>
export default {
name:'SearchJokes',
data(){
  return{
    text:''
  }
},
methods:{
  OnSubmit(){
    this.$emit('search-text',this.text);
    this.text="";
  }
}
}
</script>

<style>
input{
  padding:5px;
  border:solid 1px #ccc;
  border-radius:5px;
  margin-right:10px;
}
button{
  padding:5px 10px;
}
</style>
