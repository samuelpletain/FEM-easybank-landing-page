<script setup>
import Button from './Button.vue'
import Background from '@/assets/bg-intro-mobile.svg'
</script>

<template>
  <section class="hero">
    <Background alt="Easybank colors" class="hero__img"></Background>
    <h1 class="hero__title">Next generation digital banking</h1>
    <p class="hero__subtitle">Take your financial life online. Your Easybank account will be a one-stop-shop for spending, saving, budgeting, investing, and much more.</p>
    <Button class="hero__button" msg="Request Invite"></Button>
  </section>
</template>

<style lang="scss" scope>
  .hero {
    padding-bottom: 1.5rem;
    text-align: center;
    font-size: .9rem;
    background: $neutral-100;
    position: relative;
    &__img {
      position: relative;
      width: 100%;
      top: -4rem;
      margin-bottom: -6.5rem;
    }
    &__title {
      font-size: 2.5rem;
      line-height: 2.8rem;
      font-weight: $font-weight-light;
      padding: 0 1.5rem;
      margin-bottom: 1rem;
    }
    &__subtitle { 
      padding: 0 1.5rem;
      margin-bottom: 2rem;
      color: $neutral-500;
    }
    &__button {
      margin-bottom: 3rem;
    }
  }
</style>