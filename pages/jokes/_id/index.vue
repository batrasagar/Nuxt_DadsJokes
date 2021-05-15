
<template>
  <div>
        <nuxt-link to="/jokes">Back to Jokes</nuxt-link>

    <h3>{{ joke }}</h3>
    <small>Joke id : {{ $route.params.id }}</small>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data(){
    return{
      joke:{
      }
    }
  },
  head() {
    return {
      title: this.joke,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "my School best School etc",
        },
      ],
    };
  },
  async created() {
    try {
      const config = {
        headers: {
          Accept: "application/json",
        },
      };

      const res = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`, config);
      this.joke   = res.data.joke;
      console.log(res.data.joke);
    } catch (error) {
      console.log(error);
    }
  },
};
</script>

<style>
</style>
