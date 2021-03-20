<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <div v-if="showModal" >
      <Modal theme="dark" @hideModal="toggleModal">
        <h1>Ninja Giveaway</h1>
        <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Blanditiis cum dignissimos ea fugit ipsam magni,
          modi molestias officiis placeat porro quo quos repudiandae voluptate. Amet deserunt numquam officia optio
          suscipit.
        </div>
        <div>Adipisci alias consequatur consequuntur deleniti dicta dignissimos dolorem ducimus expedita fugit illum
          ipsum laudantium maiores modi mollitia, nam nisi pariatur porro quam quas quasi quo recusandae rem sit unde
          voluptates.
        </div>
        <template v-slot:actions>
          <a href="#">Sign Up</a>
          <a href="#">More Info</a>
        </template>
      </Modal>
    </div>
    <button @click="toggleModal">
      Toggle Modal
    </button>
    <button @click="toggleModal2">
      Toggle Modal 2
    </button>
    <div v-if="showModal2">
      <Modal @hideModal="toggleModal2">
        <h1>Sign Up to the newsletter</h1>
        <form action="">
          <p>
            <label for="email">Email : </label>
            <input type="email" id="email">
          </p>
          <p>
            <label for="password">Password : </label>
            <input type="text" id="password">
          </p>
          <button>Sign Up</button>
        </form>
      </Modal>
    </div>
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
      text: 'Grab your ninja swag for half price !',
      showModal: false,
      showModal2: false
    }
  },
  components: {
    Modal,
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModal2() {
      this.showModal2 = !this.showModal2
    }
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
