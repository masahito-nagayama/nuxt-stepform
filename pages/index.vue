<template>
  <div class="container">
     <!-- //ここで子コンポーネントのpropsと連携している。 -->
    <StepLabel1 :hoge="userData.name"></StepLabel1>
    <StepLabel1 :hoge="userData.email"></StepLabel1>
    <StepLabel1 :hoge="userData.password"></StepLabel1>
    <div>
      <form @submit.prevent>
        <p>名前入力フォーム</p>
        <input type="text" v-model="userData.name">
        <button>next</button>
        <p>メール入力フォーム</p>
        <input type="email" v-model="userData.email">
        <button>next</button>
        <p>パスワード入力フォーム</p>
        <input type="password" v-model="userData.password">
        <button>next</button>
      </form>
      <pre>{{ $data }}</pre>
    </div>
  </div>
</template>

<script>
import StepLabel1 from '~/components/stepLabel1.vue'

export default {
  components: {
    StepLabel1,
  },
  data() {
    return {
      userData: {
        name: "",
        email: "",
        password: "",
      },
    }
  },
  methods: {
    // clickSubmit() {
    //   console.log(this.userData.name);
    // }
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
