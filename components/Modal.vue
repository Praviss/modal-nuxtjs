<template>
  <div class="b-modal__parent">
      <div class="b-modal">

          <Header :title="title"/>
          
          <Message :message="message"/>
          
          <div 
          class="b-modal__action"
          >
            <div 
            class="b-modal__action__button1"
            >
                <button @click="close" id="button1_id">
                    {{button1}}
                </button>
            </div>
            <div
            class="b-modal__action__button2"
            >
                <button @click="close" id="button2_id">
                    {{button2}}
                </button>
            </div>
          </div>
      </div>
  </div>
</template>

<script>
import Header from '~/components/ModalHeader.vue'
import Message from '~/components/ModalMessage.vue'
export default {
    data(){
        return{
            
        }
    },
    props : ['title', 'message', 'button1', 'button2'],
    methods : {
        close(){
            this.$emit('close');
        }
    },
    components : {
        Header,
        Message,
    }
}
</script>

<style>
.b-modal__parent{
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(43,61,81,.81);
    display: flex;
    justify-content: center;
    align-items: center;
}
.b-modal{
    background: #FFFFFF;
    box-shadow: 2px 2px 20px 1px;
    overflow-x: auto;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
    padding: 56px;
}
.b-modal__title{
    font-size: 21px;
    text-align: center;
    color: #3f5166;
}
.b-modal__body{
    font-size: 14px;
    text-align: justify;
    color: #707780;
    margin-top: 18px;
}
.b-modal__title,
.b-modal__body,
.b-modal__action__button1,
.b-modal__action__button2{
    padding : 15px;
    display: flex;
}
.b-modal__action{
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
}
#button2_id{
    font-weight: 500;
    font-size: 14px;
    color: #fff;
    margin: 0;
    padding: 0;
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
#button1_id{
    font-weight: 500;
    font-size: 14px;
    color: #35495e;
    margin: 0;
    padding: 0;
    min-width: 70px;
    padding-left: 25px;
    padding-right: 25px;
    box-sizing: border-box;
    border: 1px solid #35495e;
    border-radius: 20px;
    box-shadow: 2px 4px 7px 0 #0000001a;
    background-color: #fff;
    line-height: 3em;
    height: 3em;
}
button{
    -webkit-appearance: button;
    cursor: pointer;
    outline: none;
}
</style>