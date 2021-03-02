<template>
  <div id="app" class="main_wrapper">
    <MethodCalculator></MethodCalculator>
    <ComputedCalculator></ComputedCalculator>
    <MethodProjectLists></MethodProjectLists>
    <ComputedProjectLists></ComputedProjectLists>
    <Query></Query>
  </div>
</template>

<script>
import MethodCalculator from './components/MethodCalculator'
import ComputedCalculator from './components/ComputedCalculator'
import MethodProjectLists from './components/MethodProjectLists'
import ComputedProjectLists from './components/ComputedProjectLists'
import Query from './components/Query'

export default {
  name: 'App',
  components: {
    MethodCalculator,
    ComputedCalculator,
    MethodProjectLists,
    ComputedProjectLists,
    Query
  }
}
</script>

<style>
  body {
    background-color: #e2e1e5;
    padding: 0;
    margin: 0;
  }
  .main_wrapper {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 8px;
  }
</style>
