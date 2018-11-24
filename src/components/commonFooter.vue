<template>
	<footer>
	  <ul>
	      <li>
	          <h3>Google Tool</h3>
	          <ul>
	              <li><router-link to="/googleCategory">谷歌前端技术应用</router-link>  </li>
	          </ul>
	      </li>
	      <li>
	          <h3>social</h3>
	          <ul>
	              <li> <router-link to="/socialMedia">社交网站嵌入</router-link></li>
	          </ul>
	      </li>
	      <li>
	          <h3>Magento</h3>
	          <ul>
	              <li><router-link to="/magentoCategory">magento技术集合</router-link></li>
	          </ul>
	      </li>
	      <li>
	          <h3>技术分享</h3>
	          <ul>
	              <li><router-link to="/techCategory">前端技术分享</router-link></li>
	          </ul>
	      </li>
	  </ul>
	    <div class="beian">
	        <a href="http://www.miitbeian.gov.cn/" target="_blank">
	        	<img src="../assets/police.png" alt="">
	        	<span>粤ICP备18091059号</span></a>
	    </div>
	</footer>
</template>

<script>
	export default {
		name: 'commonFooter'
	}
</script>

<style>
	beian{
	
	}
	.beian a{
	    display: block;
	    width: 188px;
	    margin: 50px auto;
	    color: #fff;
	    text-decoration: none;
	}

.beian span{ vertical-align: middle;margin-left: 6px;}

.beian img{ vertical-align: middle;}

@media screen and (min-width:768px){

    /*footer*/
    footer{background: #000e22;padding: 20px 0 60px;margin-top: 60px;}
    footer>ul{padding: 0;margin: 0;font-size: 0}
    footer>ul a{color: #fff;text-decoration: none;position: relative;}
    footer>ul>li>ul>li a:after{
    	display: block;
        content: '';
        width: 0;
        height: 1px;
        background: #ffffff;
        position: absolute;
        left: 50%;
        top: 18px;
        transition: all 600ms;     
    }
    footer>ul>li>ul>li a:hover:after{
         	width: 100%;
            left: 0;
     }
    footer>ul>li{
    	 display: inline-block;
    	 width: 25%;font-size: 12px;
    	 list-style: none;
    	 text-align: center;color: #fff;
	 }
    footer>ul>li>ul{margin: 0; padding: 0}
    footer>ul>li>ul>li{list-style: none}
}

/*mobile*/
@media screen and (max-width:768px){
  
    /*footer*/
    footer{background: #000e22;padding: 10px 0 60px;margin-top: 60px;}
    footer>ul{padding: 0;margin: 0;font-size: 0}
    footer>ul a{color: #fff;text-decoration: none;}
    footer>ul>li{ font-size: 12px;list-style: none;text-align: center;color: #fff}
    footer>ul>li>ul{margin: 0; padding: 0}
    footer>ul>li>ul>li{list-style: none}
}
</style>