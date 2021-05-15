<template>
  <div>
    <h1>Jokes</h1>
    <p>All jokes</p>
    <SearchJokes v-on:search-text="SearchText" />
    <Joke
      v-for="joke in jokes"
      :key="joke.id"
      :joke="joke.joke"
      :id="joke.id"
    />
  </div>
</template>

<script>
import axios from "axios";
import Joke from '@/components/Joke';
import SearchJokes from '@/components/SearchJokes';

export default {
  name: "jokes",
  components:{
    Joke,SearchJokes,
  },
  data() {
    return {
      jokes: [],
    };
  },
  methods:{
    async SearchText(prm1){
       try {
      const config = {
        headers: {
          Accept: "application/json",
        },
      };

      const res = await axios.get(`https://icanhazdadjoke.com/search?term=${prm1}`, config);
      this.jokes   = res.data.results;
      console.log(res.data);
    } catch (error) {
      console.log(error);
    }
    }
  },
  async created() {
    try {
      const config = {
        headers: {
          Accept: "application/json",
        },
      };

      const res = await axios.get("https://icanhazdadjoke.com/search", config);
      this.jokes   = res.data.results;
      console.log(res.data);
    } catch (error) {
      console.log(error);
    }
  },
  head() {
    return {
      title: "Jokes",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "my School best School etc",
        },
      ],
    };
  },
};
</script>

<style>
</style>
