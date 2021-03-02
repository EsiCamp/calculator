<template>
  <div class="method_calc">
    <h3 class="topic">
      Project lists with Query ...
    </h3>
    <input type="text" placeholder="Search ..." v-model="getDeveloper">
    <ul class="project_list">
      <li v-for="project in showProjects" :key="project.id">
        <span class="color">
          {{ project.developer }}
        </span>
        has
        <span class="color">
          {{ project.projectName }}
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name:'Query',
  data() {
    return {
      projects: [
        {
          projectName: "donya-e-eqtesad",
          developer: "ehsan",
          yearStart: 1390,
          id: 1
        },
        {
          projectName: "jamaran",
          developer: "ehsan",
          yearStart: 1390,
          id: 2,
        },
        {
          projectName: "eghtesadonline",
          developer: "fatemeh",
          yearStart: 1391,
          id: 3,
        },
        {
          projectName: "borna",
          developer: "fatemeh",
          yearStart: 1391,
          id: 4,
        },
        {
          projectName: "eghtesadnews",
          developer: "sara",
          yearStart: 1392,
          id: 5,
        }
      ],
      getDeveloper: ""
    }
  },
  computed: {
    showProjects() {
      return this.projects.filter(project => project.developer === this.getDeveloper);
    },
  },
}
</script>

<style>

</style>