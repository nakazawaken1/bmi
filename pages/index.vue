<template>
  <div class="container">
    <div>
      <MyButton />
      <MyButton back_color="#666666" />
      <MyButton back_color="#330000" fore_color="#ffeeee" />
      <MyButton left_arrow />
      <MyButton right_arrow />
      <MyButton left_arrow right_arrow />
      <MyButton>実行</MyButton>
    </div>
  </div>
</template>

<script>
import MyButton from "@/components/MyButton.vue";
export default {
  components: {
    MyButton
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
