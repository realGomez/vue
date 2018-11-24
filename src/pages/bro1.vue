<template>
	<div>
      <span>我是A组件的数据->{{a}}</span>
      <input type="button" value="把1数据传给C" @click = "send">
    </div>
</template>

<script>
	import vmson from "./commEmpty"
	export default {   
	   methods: {
              send () {
                  vmson.$emit("a-msg", this.a);
              }
          },
          data () {
              return {
                  a: "我是1组件中数据"
              }
         }
	 
	 }
</script>

<style>
</style>