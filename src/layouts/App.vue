<template>
  <div id="app">
    <!-- this代表app，root代表根实例 -->
    <Loading v-show="this.$root.bLoading"/>
    <Header v-show="this.$root.bNav"/>
    <router-view></router-view>
    <Footer v-show="this.$root.bFoot"/>
  </div>
</template>
<script>
 import Home from '../pages/home.vue'
 import Header from './header.vue'
 import Footer from '@/layouts/footer.vue'
 import Loading from '@/components/loading.vue'
  export default{
	  name:'App',
    components:{
      Home,Header,Footer,Loading
    },
    watch: {
      $route:{
        handler(nextValue,prevValue){
          // console.log("path的变化",nextValue.path);
          let path=nextValue.path

          if(/login|reg|detail/.test(path)){
            this.$root.bNav=this.$root.bFoot=false
          }
          if(/home|follow|column/.test(path)){
            this.$root.bNav=this.$root.bFoot=true
          }
          if(path.includes('user')){
            this.$root.bNav=false
            this.$root.bFoot=true
          }
        }
      },
      immediate: true
    }
  }
</script>
<style>
  
</style>
