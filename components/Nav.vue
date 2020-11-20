
<template>
  <nav class="nav">
    <div class="container">
      <div class="row justify-content-between nav-wrapper">
        <nuxt-link class="logo col-md-2" to="/" tag="div">
          <img src="../assets/img/logo.svg" alt="" />
        </nuxt-link>
        <div class="nav-links col-md-9 row justify-content-between">
          <nuxt-link tag="a" to="/" class="nav-link"> Главная</nuxt-link>
          <nuxt-link tag="a" to="/#about" class="nav-link" >О Нас</nuxt-link>
          <nuxt-link tag="a" to="/#programs" class="nav-link" >Программы</nuxt-link>
          <nuxt-link tag="a" to="/#pricing" class="nav-link" >Тарифы</nuxt-link>
          <nuxt-link tag="a" to="/#testimonials" class="nav-link" >Отзывы</nuxt-link>
          <nuxt-link tag="a" to="/#contacts" class="nav-link" >Контакты</nuxt-link>
          <nuxt-link tag="a" to="/#faq" class="nav-link" >FAQ</nuxt-link>
          <a :href="'tel:'+links[0].phone" class="btn btn__nav">{{links[0].phone}}</a>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
import linksQuery from "../apollo/queries/link/links.gql";
export default {
  data() {
    return {
      links: {},
    };
  },
  apollo: {
    links: {
      prefetch: true,
      query: linksQuery,
    },
  },
}
</script>