<script setup>
  import { ref } from 'vue'
  import Logo from '@/assets/logo.svg'

  const open = ref(false)
  const links = [
    'Home',
    'About',
    'Contact',
    'Blog',
    'Careers'
  ]
  
  function toggleOpen() {
    open.value = !open.value
  }
</script>

<template>
  <nav class="nav">
    <Logo alt="Easybank logo" class="nav__logo"></Logo>
    <img :src="open ? './src/assets/icon-close.svg' : './src/assets/icon-hamburger.svg'" alt="Menu icon" class="nav__hamburger" @click="toggleOpen">
    <ul v-if="open" class="nav__menu menu" role="list">
      <li class="menu__item item" v-for="item in links" :ref="item">
        <a :href="'./' + item.toLowerCase() + '.html'" class="item__link"> {{ item }}</a>
      </li>
    </ul>
  </nav>
  <div v-if="open" class="gradiant"></div>
  <img v-if="!open" src="@/assets/image-mockups.png" alt="" class="mockups">
</template>

<style lang="scss" scoped>
  .nav {
    padding: 1.5rem;
    background: $neutral-100;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    z-index: 3;
    position: relative;
    &__menu {
      position: absolute;
      top: 5.5rem;
    }
  }

  .mockups {
    position: absolute;
    transform: translate(-50%, -29%);
    margin-left: 50%;
    z-index: 2;
    object-fit: contain;
    max-height: 420px;
  }

  .menu {
    background-color: $neutral-100;
    text-align: center;
    width: min(100% - 3rem);
    padding: 1.5rem;
    border-radius: 5px;
    align-items: center;
    &__item:not(:last-child){
      margin-bottom: 1rem;
    }
  }

  .item__link, .item__link:visited {
    text-decoration: none;
    color: $neutral-900;
  }

  .gradiant {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: linear-gradient(to bottom, $neutral-900, transparent);
    z-index: 2;
  }
</style>