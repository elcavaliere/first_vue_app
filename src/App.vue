<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Modal title="My Modal" content="Modal content"/>
  </div>
</template>

<script>

import Modal from './components/Modal'

export default {
  name: 'App',
  data() {
    return {
      title: 'My first Vue App :)'
    }
  },
  components: {
    Modal,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{

}
</style>
