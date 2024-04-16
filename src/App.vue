<script>
import axios from 'axios';
export default {
  data() {
    return {
      title: "Ciao Mondo"
    };
  },

  created() {
    axios.get('http://127.0.0.1:8000/api/projects').then((response) => { });
  }
}

</script>

<template>
  <div class="container mt-5">
    <h1>{{ title }}</h1>
  </div>
</template>

<style lang="scss">
@use './src/scss/general.scss' as *;
</style>
