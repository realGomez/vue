<template>
  <div id="app">
    <commonHeader></commonHeader>
    <main id="main">
    <router-view/>
    </main>
     <commonFooter></commonFooter>
  </div>
</template>

<script>
		import commonHeader from './components/commonHeader';  
	  import commonFooter from './components/commonFooter';
		export default {
		  name: 'App',
		  components: {
		    commonHeader,
		    commonFooter
		  }
		}
</script>

<style>
	body,html{margin: 0}
	header, footer, main {
	    display: block;
	}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /*margin-top: 60px;*/
}
#main{
	min-height: 500px;
}
</style>
