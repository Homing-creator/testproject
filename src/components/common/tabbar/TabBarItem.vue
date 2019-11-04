<template>
<!--  :class="{ 'tab-bar-item-active': isActive }"-->
    <div class="tab-bar-item"
         @click="itemClick"
         :style="activeStyle">
      <slot name="item-icon"></slot>
      <slot name="item-text"></slot>
    </div>
</template>

<script>
// import fontcolor from '../../assets/style/globalconst.scss'
export default {
  name: 'TabBarItem',
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'deeppink'
    }
  },
  data () {
    return {
      // isActive: false
      // fontcolor
    }
  },
  computed: {
    isActive: {
      get () {
        return this.$route.path === this.path
      },
      set () {

      }
    },
    activeStyle: {
      get () {
        return this.isActive ? { color: this.activeColor } : {}
      },
      set () {
      }
    }
  },
  methods: {
    itemClick () {
      this.isActive = !this.isActive
      if (this.$route.path !== this.path) {
        this.$router.replace(this.path)
      }
    }
  },
  mounted () {
  }
}
</script>

<style scoped lang="scss">
/*@import "../../assets/style/global";*/
  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
    color: #222222;
    display: block;
    cursor: pointer;
    i{
      display: block;
      margin-top: 3px;
      font-size: 24px;
    }
    &:hover{
      color: $tabbar-color;
    }
    &.tab-bar-item-active{
      color: $tabbar-color;
    }
  }
</style>
