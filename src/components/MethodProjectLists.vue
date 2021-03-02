<template>
  <div class="method_calc">
    <h3 class="topic">
      Project lists with Method ...
    </h3>
    <ul class="project_list">
      <li v-for="project in result" :key="project.id">
        <span class="color">
          {{ project.projectName }}
        </span>
        developer is:
        <span class="color">
          {{ project.developer }}
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
      result: []
    }
  },
  methods: {
    showProjects(developer) {
      this.result = this.projects.filter(project => project.developer === developer);
    }
  },
  mounted(){
    this.showProjects("ehsan");
  }
}
</script>

<style>
  .project_list {
    list-style-type: none;
    border: 1px solid #ddd;
    padding: 16px;
    margin-bottom: 0;
  }
  .project_list li {
    padding: 16px 0;
    border-bottom: 1px solid #ddd;
  }
  .project_list li:first-child {
    padding-top: 0;
  }
  .project_list li:last-child {
    padding-bottom: 0;
    border-bottom: none;
  }
  .color {
    display: inline-block;
    color: #cf000f;
    font-weight: bold;
  }
</style>
