<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld>
      vaya vaya perro
    </HelloWorld> -->
    <Modal>
      <template slot="title">Titulo para el modal</template>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sunt, animi.
      <template slot="footer">
        <ModalButton>my botnnnnn</ModalButton>
      </template>
    </Modal>

    <ProgressView inline-template>
      <div>
        <h1>Mi progreso de seguir el tutorial es de: {{ progress }}</h1>
        <p>
          <button @click="progress += 10">Aumentar el progreso</button>
        </p>
      </div>
    </ProgressView>

  </div>
</template>

<script>
import Modal from './components/Modal.vue'

import Vue from 'vue/dist/vue';

const ModalButton = Vue.component('ModalButton', {
  name: 'ModalButton',
  template: `
  <a href="#" class="button is-primary"><slot></slot></a>
  `
});

const ProgressView = Vue.component('ProgressView', {
  data() {
    return {
      progress: 0
    }
  },
})

export default {
  name: 'App',
  components: {
    Modal,
    ModalButton,
    ProgressView
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
