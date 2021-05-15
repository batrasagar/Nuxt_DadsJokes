<template>
  <div>
<h1>Welcome</h1>
<p>All home content</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Home",
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


.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
