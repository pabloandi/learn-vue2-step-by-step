<template>
  <div :class="modalClass">
      <div class="modal-background"></div>
      <div class="modal-card">
          <header class="modal-card-head">
              <p class="modal-card-title">
                  <slot name="title"></slot>
              </p>
              <button class="delete" @click="closeModal"></button>
          </header>
          <section class="modal-card-body">
              <slot>
                  Default content here
              </slot>
          </section>
          <footer class="modal-card-foot">
              <slot name="footer">
                  <a href="#" class="button is-primary">Save changes</a>    
                  <a href="#" class="button" @click="closeModal">Cancel</a>
              </slot>
          </footer>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Modal',
    data() {
        return {
            close: false
        }
    },
    methods: {
        closeModal(){
            this.close = true;
        }
    },
    computed: {
        modalClass(){
            return (this.close) ? 'modal' : 'modal is-active'
        }
    },
}
</script>

<style scoped>
    @import url('https://cdn.jsdelivr.net/npm/bulma@0.9.1/css/bulma.min.css');
</style>
