<template>
  <div>
    <div class="text-h4" id="project-title">{{ title }}</div>
    <div v-for="project in projects" :key="project.name">
      <ProjectCard :project="project" />
      <br />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    projects: Array,
    title: {
      default: "Projects"
    }
  }
};
</script>

<style scoped>
#project-title {
  margin-bottom: 20px;
}
</style>
