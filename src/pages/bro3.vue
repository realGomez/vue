<template>
	<div>
      <h3>我是C组件</h3>
         <span>接收过来A的数据为: {{a}}</span>
          <br>
          <span>接收过来B的数据为: {{b}}</span>
	</div>
</template>

<script>
	import vmson from "./commEmpty"
	
	export default {   
	     mounted () {
             //接收A组件的数据
            vmson.$on("a-msg", function (a) {
                  this.a = a;
            }.bind(this));
  
             //接收B组件的数据
             vmson.$on("b-msg", function (a) {
                  this.b = a;
             }.bind(this));
         },
          data () {
              return {
                  a:"",
                  b:""
              }
         }
	 
	 }
</script>

<style>
</style>