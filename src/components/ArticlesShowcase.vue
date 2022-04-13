<script setup>
  import { ref } from 'vue'
  import Article from './Article.vue'

  const articles = ref([
    {
      author: 'Claire Robinson',
      title: 'Receive money in any currency with no fees',
      subtitle: 'The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …',
      img: 'currency'
    },
    {
      author: 'Wilson Hutton',
      title: 'Treat yourself without worrying about money',
      subtitle: 'Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …',
      img: 'restaurant'
    },
    {
      author: 'Wilson Hutton',
      title: 'Take your Easybank card wherever you go',
      subtitle: 'We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …',
      img: 'plane'
    },
    {
      author: 'Claire Robinson',
      title: 'Our invite-only Beta accounts are now live!',
      subtitle: 'After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site …',
      img: 'confetti'
    }
  ])
</script>

<template>
  <div class="articles-showcase">
    <h2 class="articles-showcase__title">Latest Articles</h2>
    <Article v-for="item in articles" :article="item" class="articles-showcase__article"></Article>
  </div>
</template>

<style lang="scss" scoped>
  .articles-showcase {
    position: relative;
    top:-1px;
    margin-bottom: 1px;
    padding: 5rem 1.6rem;
    background: $neutral-200;
    &__title {
      margin-bottom: 2rem;
      text-align: center;
      font-weight: $font-weight-regular;
      font-size: 1.9rem;
    }
    &__article:not(:last-child) {
      margin-bottom: 1.5rem;
    }
  }
</style>