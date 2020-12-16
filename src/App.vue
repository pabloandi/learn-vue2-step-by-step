<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld>
      vaya vaya perro
    </HelloWorld> -->
    <Modal>
      <template slot="title">Titulo para el modal</template>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sunt, animi.
      
    </Modal>
  </div>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Modal
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
</style>
