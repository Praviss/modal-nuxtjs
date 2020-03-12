<template>
  <div class="container">
    <div>
      
      <h2 class="title">
        Sample Nuxtjs Modal Project
      </h2>
      <button @click="showModal" id="b-modal-btn">Show Modal</button>
      
      <Modal 
      v-if="isModal" 
      :title="modalContent.title"
      :message="modalContent.message"
      :button1="modalContent.button1"
      :button2="modalContent.button2"
      @close="closeModal"
      />
    
    </div>
  </div>
</template>

<script>
import Modal from '~/components/Modal.vue'
import Logo from '~/components/Logo.vue'

export default {
  data(){
    return{
      isModal : false,
      modalContent : {
        title : 'This is the default title',
        message : 'This is the default message',
        button1 : 'CANCEL',
        button2 : 'CONTINUE',
      },
      
    }
  },
  components: {
    Logo,
    Modal
  },
  methods : {
    showModal(){
      this.isModal = true;
    },
    closeModal(){
      this.isModal = false;
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
#b-modal-btn{
    font-weight: 500;
    font-size: 14px;
    color: #fff;
    margin: 0;
    padding: 0;
    margin-top: 24px;
    min-width: 70px;
    padding-left: 25px;
    padding-right: 25px;
    box-sizing: border-box;
    border: none;
    border-radius: 20px;
    box-shadow: 2px 4px 7px 0 #0000001a;
    background-color: #35495e;
    line-height: 3em;
    height: 3em;
}
</style>
