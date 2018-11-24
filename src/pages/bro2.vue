<template>
	<div>
         <span>我是B组件的数据->{{a}}</span>
         <input type="button" value="把2数据传给C" @click = "send">
    </div>
</template>

<script>
	import vmson from "./commEmpty"
	
	export default {   
	  methods: {
             send () {
                  vmson.$emit("b-msg", this.a);
              }
          },
          data () {
              return {
                  a: "我是2组件中数据"
              }
          }
	 }
</script>

<style>
</style>