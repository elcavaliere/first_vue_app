<template>
  <div class="backdrop">
    <div class="modal" :class="{ dark: theme === 'dark'}">
      <h1>{{ header }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: ['header','text','theme']
}
</script>

<style scoped>
  .modal{
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background-color: #fff;
    border-radius: 10px;
  }
  .backdrop{
    top: 0;
    position: fixed;
    background: rgba(0,0,0,0.5);
    width: 100%;
    height: 100%;
  }
  h1{
    color: #03cfb4;
    border: none;
    padding: 0;
  }
  .modal.dark{
    background-color: #2c3e50;
    color: #ffffff;
  }
  .modal.dark h1{
    color: #fff;
  }
</style>