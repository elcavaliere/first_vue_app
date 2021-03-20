<template>
  <div class="backdrop">
    <div class="modal">
      <h1>{{ title }}</h1>
      <p>{{ content }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: ['title','content']
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
</style>