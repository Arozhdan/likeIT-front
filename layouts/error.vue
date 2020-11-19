<template>
  <div class="err">
    <header class="err-header">
      <Nav />
      <div class="err-header-inner container">
        <img src="../assets/img/err.png" alt="" />
        <h1 class="err-header-title">
          К сожалению, такая страница не найдена :(
        </h1>
        <h3 class="err-header-suptitle">
          Возможно, она была удалена или была перемещена
        </h3>
        <div class="btn-wrapper">
          <button class="btn">На главную</button>
        </div>
      </div>
    </header>
    <Footer/>
  </div>
</template>
<script>
import Footer from '../components/Footer'
export default {
  components:{
    Footer
  }

  
}
</script>