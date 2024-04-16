<script>

import ProjectList from './components/ProjectList.vue';
import AppHeader from './components/AppHeader.vue';
export default {
  data() {
    return {
      title: "PortFolio Projects",


    };
  },

  components: { AppHeader, ProjectList },

}

</script>

<template>
  <AppHeader :title="title"></AppHeader>
  <div class="container mt-5 pb-5">
    <ProjectList></ProjectList>
  </div>
</template>

<style lang="scss">
@use './src/scss/general.scss' as *;
</style>
