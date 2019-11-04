<template>
  <TabBar>
<!--    activeColor -->
    <TabBarItem path="/home">
      <template #item-icon>
        <i class="iconfont iconyemian"></i>
      </template>
      <template v-slot:item-text>
        <div>首页</div>
      </template>
    </TabBarItem>
    <TabBarItem path="/category">
      <template #item-icon>
        <i class="iconfont iconicon_type"></i>
      </template>
      <template #item-text>
        <div>分类</div>
      </template>
    </TabBarItem>
    <TabBarItem path="/shoppingcart">
      <template #item-icon>
        <i class="iconfont iconqicheqianlian-"></i>
      </template>
      <template #item-text>
        <div>购物车</div>
      </template>
    </TabBarItem>
    <TabBarItem path="/profile">
      <template #item-icon>
        <i class="iconfont iconyonghu"></i>
      </template>
      <template #item-text>
        <div>我的</div>
      </template>
    </TabBarItem>
  </TabBar>
</template>

<script>
import TabBar from '../common/tabbar/TabBar'
import TabBarItem from '../common/tabbar/TabBarItem'
export default {
  name: 'MainTabBar',
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style scoped lang="scss">

</style>
