<template>
  <div class="container">
    <ul>
      <li>
        <label>身長</label>
        <input type="nubmer" v-model="tall" />
        <span>({{tall}})cm</span>
      </li>
      <li>
        <label>体重</label>
        <input type="nubmer" v-model="weight" />
        <span>({{weight}})kg</span>
      </li>
      <li>BMI(Body Mass Index) = {{format(bmi)}}</li>
      <li>適正体重 = {{format(standard_weight)}} kg</li>
      <li>適正体重との差 = {{format(weight - standard_weight)}} kg</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tall: null,
      weight: null
    };
  },
  computed: {
    tall_m() {
      return this.tall / 100;
    },
    bmi() {
      return this.weight / (this.tall_m * this.tall_m);
    },
    standard_weight() {
      return this.tall_m * this.tall_m * 22;
    }
  },
  methods: {
    format(value) {
      return Math.round(value * 100) / 100;
    }
  }
};
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  > ul {
    list-style-type: none;
    > li {
      margin: 1em;
    }
  }
}
</style>
