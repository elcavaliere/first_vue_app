<template>
  <div class="backdrop" @click.self="hideModal">
    <div class="modal" :class="{ dark: theme === 'dark'}">
      <slot></slot>
      <div class="actions">
        <slot name="actions"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: ['theme'],
  methods: {
    hideModal() {
      this.$emit('hideModal')
    }
  }
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

  .modal .actions{
    color: #fff;
    padding: 20px 0;
  }

  .modal .actions a{
    color: #333;
    padding: 8px;
    border: 1px solid #eee;
    border-radius: 4px;
    text-decoration: none;
    margin: 10px;
  }
  .modal.dark .actions a{
    color: #fff;
  }
</style>