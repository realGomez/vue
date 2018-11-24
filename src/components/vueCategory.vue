<template>
	<div>
		
		<h3>vue 入门</h3>
		<div>
			<p>脚手架、脚手架目录、组件</p>
			<a href="https://www.jianshu.com/p/1626b8643676" target="_blank">脚手架</a>		
		</div>
	
	
	  <div>
	  	<h3>父子传参</h3>
	  	
	  	<input v-model="newItem" />
	  	<div>{{newItem}}</div>
	  		  	
	  	
	  	<props mes-father="message from father" @valueUp="recieve"></props>
	  	
	  	
	  	<h3>父传子 broadcast</h3>
	  	<input v-model="newItem" @keyup.enter="addNew"/>
  		<h3>父传子 broadcast</h3>
	  	<bro1></bro1>
	  	<bro2></bro2>
	  	<bro3></bro3>
	  	
	  	
	  	<!-- p元素，用于展示子组件传递过来的数据 -->
	  	<h3>子传父</h3>
        <p>子组件传递过来的数据 {{childMes}}</p>
	  </div>
	   </div>
	  
	   

</template>

<script>
	import props from '../pages/props';
	import bro1 from '../pages/bro1';
	import bro2 from '../pages/bro2';
	import bro3 from '../pages/bro3';
	
	
	
	export default {
          components: {
		    props,bro1,bro2,bro3 
		  },// 添加data
		  data: function () {
		    return {
		      childMes:'',
		      newItem:'',
		      
		    }
		  },
		
		  // 添加methods，自定义事件valueUp的事件处理函数recieve
		  methods: {
		   
			recieve: function(mes) { 
				console.log("receive");
				
				// recieve 事件需要设置参数，这些参数就是子组件传递过来的数据，因此，参数的个数，也要和子元素传递过来的一致。
		      this.childMes = mes;
		   },
			
			addNew: function() {
				
				console.log("addNew broadcast on onNew");
				
			   this.$broadcast('onAddnew', this.items);
			}
		    
		  },
		  
	}
	
</script>

<style>
</style>