<template>
  <div class="method_calc">
    <h3 class="topic">
      Calculator with Method ...
    </h3>
    <input type="text" v-model="firstNum">
    <div class="select_box">
      <select id="select_inner" v-model="selected">
        <option v-for="operator in operators" :key="operator">
          {{ operator }}
        </option>
      </select>
    </div>
    <input type="text" v-model="secondNum">
    <span class="btn_wrapper">
      <button class="btn_calc" @click="calculate">
        Calculate
      </button>
    </span>
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
      result: 0,
      operators: ["+", "-", "*", "/"],
      selected: "+"
    }
  },
  methods: {
    calculate() {
      if (this.selected === "+") {
        this.result = +this.firstNum + +this.secondNum;
      } else if (this.selected === "-") {
        this.result = this.firstNum - this.secondNum;
      } else if (this.selected === "*") {
        this.result = this.firstNum * this.secondNum;
      } else if (this.selected === "/") {
        this.result = this.firstNum / this.secondNum;
      }
    }
  }
}
</script>

<style>
  .method_calc {
    box-shadow: 0 0 7px 0 rgba(0, 0, 0, 0.26);
    background-color: #fff;
    padding: 16px;
  }
  .topic {
    margin-top: 0;
  }
  .select_box {
    display: inline-block;
    padding: 0 16px;
  }
  .btn_wrapper {
    padding-left: 16px;
  }
  .btn_calc {
    cursor: pointer;
    border: 1px solid #ddd;
    border-radius: 4px;
    padding: 8px 16px;
    background-color: #4caf50;
    color: #fff;
    transition: .3s;
    box-shadow: none;
  }
  .btn_calc:hover {
    background-color: #46a049;
  }
  #select_inner {
    padding: 3px 6px;
    cursor: pointer;
  }
  .result {
    margin-bottom: 0;
  }
</style>
