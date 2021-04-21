<template>
  <div class="container">
    <StepLabel></StepLabel>
    <div>
      <form>
        <p>名前入力フォーム</p>
        <input type="text" v-model="userData.name">
        <button>next</button>
      </form>
    </div>
  </div>
</template>

<script>
import StepLabel from '~/components/stepLabel.vue'

export default {
  components: {
    StepLabel,
  },
  data() {
    return {
      userData: {
        name: "",
      },
    }
  },
}
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
