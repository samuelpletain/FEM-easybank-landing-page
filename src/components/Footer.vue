<script setup>
import Button from './Button.vue'
import Logo from '@/assets/logo.svg'
import Facebook from '@/assets/icon-facebook.svg'
import Youtube from '@/assets/icon-youtube.svg'
import Twitter from '@/assets/icon-twitter.svg'
import Pinterest from '@/assets/icon-pinterest.svg'
import Instragram from '@/assets/icon-instagram.svg'

const links = [
  'About us',
  'Contact',
  'Blog',
  'Careers',
  'Support',
  'Privacy Policy'
]
const socials = [
  'Facebook',
  'YouTube',
  'Twitter',
  'Pinterest',
  'Instagram'
]
</script>

<template>
  <footer class="footer">
    <Logo alt="Easybank logo" class="footer__logo"></Logo>
    <div class="footer__socials socials">
      <Facebook class="socials__icon"></Facebook>
      <Youtube class="socials__icon"></Youtube>
      <Twitter class="socials__icon"></Twitter>
      <Pinterest class="socials__icon"></Pinterest>
      <Instragram class="socials__icon"></Instragram>
    </div>
    <ul class="footer__menu menu" role="list">
      <li class="menu__item item" v-for="item in links" :ref="item">
        <a :href="'./' + item.toLowerCase() + '.html'" class="item__link"> {{ item }}</a>
      </li>
    </ul>
    <Button msg="Request invite" class="footer__button button"></Button>
    <p class="footer__credits">@Easybank. All Rights Reserved</p>
  </footer>
</template>

<style lang="scss">
  .footer{
    color: $neutral-100;
    padding: 1.5rem;
    display: flex;
    align-items: center;
    flex-direction: column;
    font-size: .9rem;
    &__logo {
      margin-bottom: 2rem;
      & [fill-rule="nonzero"] {
        fill: #fff;
      }
    }
    &__socials {
      display: flex;
      gap: 1rem;
      margin-bottom: 2rem;      
    }
    &__menu {
      margin-bottom: 2rem;
    }
    &__button {
      margin-bottom: 2rem;
    }
    &__credits {
      color: $neutral-500;
    }
  }

  .menu {
    text-align: center;
    align-items: center;
    &__item:not(:last-child){
      margin-bottom: 1rem;
    }
  }

  .item__link, .item__link:visited {
    color: $neutral-100;
    text-decoration: none;
  }

  .item__link:hover {
    color: $primary;
  }

  .socials__icon:hover path {
    fill: $primary;
    cursor: pointer;
  }
</style>