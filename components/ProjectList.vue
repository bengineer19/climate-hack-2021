<template>
  <div>
    <div class="text-h4" id="project-title">Active projects</div>
    <div v-for="project in projects" :key="project.name">
      <ProjectCard :project="project" />
    </div>
  </div>
</template>

<script>
export default {
  props: ["projects"]
};
</script>

<style scoped>
#project-title {
  margin-bottom: 20px;
}
</style>
