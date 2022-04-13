<script setup>
import { ref } from 'vue'

const data = [
  {
    img: 'online',
    title: 'Online Banking',
    content: 'Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.' 
  },
  {
    img: 'budgeting',
    title: 'Simple Budgeting',
    content: 'See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits.' 
  },
  {
    img: 'onboarding',
    title: 'Fast Onboarding',
    content: 'We don’t do branches. Open your account in minutes online and start taking control of your finances right away.' 
  },
  {
    img: 'api',
    title: 'Open API',
    content: 'Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.' 
  },
  ]
</script>

<template>
  <section class="showcase">
    <h2 class="showcase__title">Why choose Easybank?</h2>
    <p class="showcase__subtitle">We leverage Open Banking to turn your bank account into your financial hub. Control your finances like never before.</p>
    <div class="showcase__category category" v-for="item in data">
      <img :src="'./src/assets/icon-' + item.img + '.svg'" :alt="item.title + ' icon'" class="category__img">
      <h3 class="category__title">{{ item.title }}</h3>
      <p class="category__content">{{ item.content }}</p>
    </div>
  </section>
</template>

<style lang="scss">
  .showcase {
    position: relative;
    top: -1px;
    background-color: $neutral-300;
    color: $neutral-900;
    text-align: center;
    padding: 4rem 1.6rem;
    font-size: .9rem;
    &__title {
      font-size: 2rem;
      font-weight: $font-weight-regular;
      line-height: 2.3rem;
      margin-bottom: 1rem;
    }
    &__subtitle {
      color: $neutral-500;
      padding-bottom: 3rem;
    }
  }
  
  .category {
    &__img {
      margin: 0 auto 1.5rem;
    }
    &__title {
      font-size: 1.2rem;
      font-weight: $font-weight-light;
      margin-bottom: 1rem;
    }
    &__content {
      color: $neutral-500;      
    }
    &:not(:last-child) {
      margin-bottom: 2rem;
    }
  }
</style>