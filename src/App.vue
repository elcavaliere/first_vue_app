<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Modal :header="header" :text="text" theme="dark" />
  </div>
</template>

<script>

import Modal from './components/Modal'

export default {
  name: 'App',
  data() {
    return {
      title: 'My first Vue App :)',
      header: 'Sign up for the Giveaway',
      text: 'Grab your ninja swag for half price !'
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
