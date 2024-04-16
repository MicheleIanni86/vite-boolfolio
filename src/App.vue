<script>
import axios from 'axios';
export default {
  data() {
    return {
      title: "Projects",
      projects: [],

    };
  },

  created() {
    axios.get('http://127.0.0.1:8000/api/projects').then((response) => {
      this.projects = response.data.data;
    });
  }
}

</script>

<template>
  <div class="container mt-5">
    <h1>{{ title }}</h1>

    <div v-for="project in projects">
      <ul>
        <li><strong>ID: </strong>{{ project.id }}</li>
        <li><strong>Titolo: </strong>{{ project.title }}</li>
        <li><strong>Contenuto: </strong>{{ project.content }}</li>
        <li><strong>Immagine: </strong>{{ project.image }}</li>
      </ul>
      <hr>
    </div>

  </div>
</template>

<style lang="scss">
@use './src/scss/general.scss' as *;
</style>
