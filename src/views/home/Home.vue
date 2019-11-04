<template>
  <div id="home">
    <NavBar>
      <template v-slot:center>
        <div class="home-nav">购物街</div>
      </template>
    </NavBar>
    <h2>首页</h2>
  </div>
</template>

<script>
import NavBar from '../../components/common/navbar/NavBar'
export default {
  name: 'Home',
  components: {
    NavBar
  }
}
</script>

<style scoped lang="scss">
  #home{
    .home-nav{
      background-color: #fff;
    }
  }
</style>
