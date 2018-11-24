<template>
	<div>
      <span>我是A组件的数据->{{a}}</span>
      <input type="button" value="把1数据传给C" @click = "send">
    </div>
</template>

<script>
	import Vue from 'vue'
    export default new Vue()

</script>

<style>
</style>