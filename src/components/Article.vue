<script setup>
import { ref } from 'vue'

defineProps({
  article: {
    title: String,
    subtitle: String,
    img: String,
    author: String
  }
})
</script>

<template>
  <article class="article">
    <img :src="'./src/assets/image-' + article.img + '.jpg'" alt="" class="article__img">
    <div class="article__content content">
      <p class="content__author">By {{ article.author }}</p>
      <h3 class="content__title">{{ article.title }}</h3>
      <p class="content__subtitle">{{ article.subtitle }}</p>
    </div>
  </article>
</template>

<style lang="scss" scoped>
  .article {
    background: $neutral-100;
    font-size: .9rem;
    &__img {
      object-fit: cover;
      width: 100%;
      border-top-left-radius: 5px;
      border-top-right-radius: 5px;
      aspect-ratio: 1.5;
    }
  }

  .content {
    padding: 1.8rem;
    color: $neutral-500;
    &__author {
      font-size: .7rem;
      margin-bottom: .5rem;
    }
    &__title {
      font-weight: $font-weight-regular;
      color: $neutral-900;
      line-height: 1.2rem;
      margin-bottom: .5rem;
      &:hover {
        color: $primary;
        cursor: pointer;
      }
    }
    &__subtitle {
      margin-bottom: .5rem;
      font-size: .8rem;
    }
  }
</style>