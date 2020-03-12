<template>
  <div class="b-modal__body">
      {{ message }}
  </div>
</template>

<script>
export default {
    props : ['message'],
}
</script>

<style>
    .b-modal__body{
        font-size: 14px;
        text-align: justify;
        color: #707780;
        margin-top: 18px;
        padding: 15px;
        display: flex;
    }
</style>