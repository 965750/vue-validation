<template>
  <main>
    <app-form></app-form>
  </main>
</template>

<script>

import Form from './components/Form.vue'

export default {
  components: {
    "app-form": Form
  },
  name: 'app',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<style lang="scss">

@import url('https://fonts.googleapis.com/css?family=Lato:400,700&amp;subset=latin-ext');

body{
  margin: 0px;
  padding: 0px;
  font-family: 'Lato', sans-serif;
}
</style>
