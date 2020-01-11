<template>
  <div class="nav">
    <ul>
		<router-link tag="li" active-class="active" to="/home"><a href="#" >首页</a></router-link>
		<router-link tag="li" active-class="active" to="/follow"><a href="#" >论坛</a></router-link>
		<router-link tag="li" active-class="active" to="/column"><a href="#" >关注</a></router-link>
    </ul>
  </div>
</template>

<script>
  export default {
    data(){return {}},
    components:{},
    mounted(){},
    updated(){},
    methods:{}
  }
</script>

<style  scoped>
  .nav{width:100%; position:fixed; top:0;left:0; z-index:2; background:#5477b2;}
  .nav ul{width:4.38rem;height:0.6rem; margin:0 auto;}
  .nav ul li{width:1.46rem;height:0.6rem; float:left;}
  .nav ul li a{ display:block;width:1.46rem;height:0.6rem; line-height:0.6rem; text-align:center; font-size:0.3rem; color:#9e9a95;}
  .nav ul li.active a{height:0.5rem; border-bottom:0.1rem solid #fff; color:#333;}
</style>
