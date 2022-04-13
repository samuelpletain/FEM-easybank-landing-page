<script setup>
  import { ref } from 'vue'
  
  defineProps({
    msg: String
  })
</script>

<template>
  <a class="button">{{ msg }}</a>
</template>

<style lang="scss">
  .button {
    padding: 1rem 2rem;
    border-radius: 50px;
    background: linear-gradient(to right, $primary, $secondary);
    color: $neutral-100;
    display: block;
    width: fit-content;
    margin: auto;
    line-height: 1rem;
    font-weight: $font-weight-bold;
    &:hover {
      background: linear-gradient(to right, lighten($primary, 10), lighten($secondary, 10));
      cursor: pointer;
    }
  }
</style>