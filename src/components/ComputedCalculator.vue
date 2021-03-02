<template>
  <div class="method_calc computed_calc">
    <h3 class="topic">
      Calculator with Computed property ...
    </h3>
    <input type="text" v-model="firstNum">
    <div class="select_box">
      <select id="select_inner" v-model="selected">
        <option v-for="(operator, index) in operators" :key="operator + index">
          {{ operator }}
        </option>
      </select>
    </div>
    <input type="text" v-model="secondNum">
    <p class="result">
      Result is:
      <span class="color">
        {{ result }}
      </span>
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstNum: 0,
      secondNum: 0,
      operators: ["+", "-", "*", "/"],
      selected: "+"
    }
  },
  computed: {
    result() {
      switch(this.selected) {
        case "+":
          return +this.firstNum + +this.secondNum;
        case "-":
          return this.firstNum - this.secondNum;
        case "*":
          return this.firstNum * this.secondNum;
        case "/":
          return this.firstNum / this.secondNum;
        default:
          return 0;
      }
    }
  }
}
</script>

<style>
  .computed_calc {
    margin: 32px 0;
  }
</style>
