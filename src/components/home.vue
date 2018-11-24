<template>
 <main id="main">
    <div class="home-banner">
        <a href="javascript:void(0)">
        	<img src="../assets/home/home-banner.jpg" alt="">
        </a>
    </div>

    <h2> 前端技术 </h2>
    <div class="home-items item-3 fl-left">
        <router-link to="/googleCategory">
        	<img src="../assets/home/google.jpg" alt="">
        </router-link> 
        <div class="home-item-content-wrapper">
            <div class="home-item-content">
                <h3>Google Tool</h3>
                <p>tag manager、优化测试</p>
              <router-link to="/googleCategory">谷歌前端技术应用</router-link>                                
            </div>
            <div class="home-item-content-bro"></div>
        </div>
    </div>
    <div class="home-items item-2 fl-right">
        <router-link to="/社交网站嵌入">
        	<img src="../assets/home/social.jpg" alt="">
        </router-link>
        <div class="home-item-content-wrapper">
            <div class="home-item-content">
                <h3>social media</h3>
                <p>facebook、twitter、instagram，导出图片，第三方登陆</p>
                <router-link to="/socialMedia">社交网站嵌入</router-link>
            </div>
        </div>
    </div>
    <div class="home-items item-1 fl-left">
       <router-link to="/magentoCategory">
       	<img src="../assets/home/magento.jpg" alt="">
       </router-link>
        <div class="home-item-content-wrapper">
            <div class="home-item-content">
                <h3>magento</h3>
                <p>magento bug分析、magento 插件</p>
                <router-link to="/magentoCategory">magento开发</router-link>
            </div>
            <div class="home-item-content-bro"></div>
        </div>
    </div>

    <div class="home-items item-2 fl-right">
        <router-link to="/socialMedia">
        	<img src="../assets/home/tech.jpg" alt=""></router-link>
        <div class="home-item-content-wrapper">
            <div class="home-item-content">
                <h3>前端技术</h3>
                <p>js、css、浏览器兼容、移动端开发、支付宝微信支付</p>
                <router-link to="/techCategory">前端技术分享</router-link>
            </div>
        </div>
    </div>
    <div class="home-items item-1 fl-left">
       <router-link to="/magentoCategory">
       	<img src="../assets/home/vue.jpg" alt="">
       </router-link>
        <div class="home-item-content-wrapper">
            <div class="home-item-content">
                <h3>VUE</h3>
                <p>vue的入门</p>
                <router-link to="/vueCategory">vue开发</router-link>
            </div>
            <div class="home-item-content-bro"></div>
        </div>
    </div>
    
    <a href="./../pages/gold.html">gold</a>
    <div id="instagram">
    	#instagram
    </div>
    
</main>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

#test-links{padding: 20px;text-align: center}
#test-links li{
    list-style: none;
}


/*pc*/
@media screen and (min-width:768px){
    .home-banner a{display: block;font-size: 0;}
    .home-banner img{width: 100%;}
    .home-items{font-size: 0;position: relative;}
     h2{text-align: center}
    .home-items >a{display: inline-block;width: 50%;overflow: hidden}  
    .home-items img{width: 100%;transition: all 600ms}
    .home-items img:hover{opacity: 0.8;transform: scale(1.05)}
    .home-items .home-item-content-wrapper{display: inline-block;width: 50%;font-size: 16px;}
    .home-items.fl-left{text-align: right;}
    .home-items.fl-left .home-item-content-wrapper{
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        text-align: center;
    }
    .home-items.fl-left .home-item-content-bro{
        display: inline-block;
        height: 100%;
        vertical-align: middle;
    }
    .home-items.fl-left .home-item-content{
        display: inline-block;
        vertical-align: middle;
    }

    .home-items.fl-right >a{vertical-align: middle;}
    .home-items.fl-right .home-item-content-wrapper{
        vertical-align: middle;
    }
    .home-items .home-item-content{
        text-align: center;
    }
    .home-items .home-item-content a{color: #000;text-decoration: none;}
    .home-items .home-item-content a:after{   
	    border-radius: 50%;
	    display: inline-block;
	    content: ">";
	    background: #000;
	    color: #fff;
	    width: 18px;
	    height: 18px;
	    line-height: 18px;
	    text-align: center;
	    margin-left: 3px;
	}
}

/*mobile*/
@media screen and (max-width:768px){
    .home-banner a{display: block;font-size: 0;}
    .home-banner img{width: 100%;}
    h2{text-align: center}
    .home-items img{width: 100%;}
    .home-items >a{display: block;font-size: 0;}
    .home-item-content-wrapper{text-align: center;margin: 20px 0 30px}
    .home-items .home-item-content a{color: #000;text-decoration: none;}
}
</style>
