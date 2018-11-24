<template>
	<div>
		<p>--- props --子-- </p>
		<h4>父传子</h4>
		<p>{{mesFather}}</p>
		
		
		<a href="https://www.baidu.com/">百度</a>
		<h4>子传父</h4>
		<!-- 添加一个input输入框 添加keypress事件-->
    <input type="text" v-model="inputValue" @keyup="keypress"/>
    <button @click="keypress">butto</button>
    <div>{{inputValue}}</div>
	<p>	--- props--子-</p>
    
	</div>
</template>

<script>
	export default {   
	  props:['mesFather'],
	  
	  // 添加data, 用户输入绑定到inputValue变量，从而获取用户输入
	  data: function () {
	    return {
	      inputValue: ''  
	    }
	  },
	  methods:{
	     keypress:function(){
	     	console.log("keypress son");
	     	this.$emit("valueUp", this.inputValue)
	     }
	  },
	  events: {
		'onAddnew': function(items){
		   console.log(items)
	     }

	   }
	 }
</script>

<style>
</style>