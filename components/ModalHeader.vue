<template>
  <div class="b-modal__title">
      {{title}}
  </div>
</template>

<script>
export default {
    
    props : ['title'],
}
</script>

<style>
    .b-modal__title{
        font-size: 21px;
        text-align: center;
        color: #3f5166;
        padding: 15px;
        display: flex;
    }
</style>