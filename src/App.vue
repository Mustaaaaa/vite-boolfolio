<template>
  <div>
    {{ msg }}
    <AppMain />
  </div>

</template>

<script>
import AppMain from './components/AppMain.vue';

export default {
  data() {
    return {
      msg: 'Welcome to Vue.js + Vite App'
    }
  },
  components: {
    AppMain,

  }
}
</script>


<style></style>
