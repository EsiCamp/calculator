<template>
  <div class="method_calc computed_project">
    <h3 class="topic">
      Project lists with Computed property ...
    </h3>
    <ul class="project_list">
      <li v-for="project in showProjects" :key="project.id">
        <span class="color">
          {{ project.developer }}
        </span>
        get
        <span class="color">
          {{ project.projectName }}
        </span>
        since
        <span class="color">
          {{ project.yearStart }}
        </span>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
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
    }
  },
  computed: {
    showProjects() {
      return this.projects.filter(project => project.developer === "sara" && project.yearStart > 1391);
    }
  }
}
</script>

<style>
  .computed_project {
    margin: 32px 0;
  }
</style>
