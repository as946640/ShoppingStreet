<template>
  <div id="app">
    <!-- 使用keep-alive，表示我们main-tab-bar所有的组件，子组件都会被保存
        然后我们现在Details组件不希望它被保存，而是重复创建，所以用
        exclude把该组件排除在外
     -->
    <keep-alive exclude="Details">
      <router-view></router-view>
    </keep-alive>
    
    <Main-tab-bar></Main-tab-bar>
    
    
  </div>
</template>

<script>
  import MainTabBar from 'components/content/MaintabBar'


export default {
  name: 'App',
  components: {
    MainTabBar,
    
  }
}
</script>

<style>
  @import url('~assets/css/base.css');
  
</style>
