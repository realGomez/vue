<template>
	<div>
		<header>
			<div id="mobile-nav-icon"></div>
			<div id="logo">			   
			    <router-link to="/"><img src="../assets/logo.png" alt="fisher"></router-link>
			</div>
		</header>
		<div id="nav">
		     <ul>

		         <li class="nav-level-0"><a href="javascript:void(0)">社交网站嵌入</a>
		            <div class="nav-level-1-wrapper">
		                <ul>
		                    <li>
		                    	<a href="https://developers.facebook.com/" target="_blank">Facebook</a>
		                    </li>
		                    <li>
		                    	<a href="javascript:void(0)" target="_blank">Instagram</a>
		                    </li>
		                    <li>
		                    	<a href="javascript:void(0)" target="_blank">twitter</a>
		                    </li>
		                    <li>
		                    	<a href="javascript:void(0)" target="_blank">wechat</a>
		                    </li>
		                    <li>
		                    	<a href="javascript:void(0)" target="_blank">snapchat</a>
		                    </li>
		                    <li>
		                    	<router-link to="/socialMedia">社交网站嵌入</router-link>
		                    </li>
		                </ul>
		            </div>
		        </li>
		        <li class="nav-level-0"><a href="javascript:void(0)">magento</a>
		            <div class="nav-level-1-wrapper">
		                <ul>
		                    <li>
		                    	<a href="https://docs.magento.com/m2/ce/user_guide/magento/magento-community-edition-2.1-user-guide.html" target="_blank">magneto 使用指导</a>
		                    </li>
		                    <li>
		                    	<a href="https://magento.com/" target="_blank">magneto官网-下载-文档技术中心</a>
		                	</li>
		                    <li>
		                    
                    	    	<router-link to="/magentoCategory">magento技术分析</router-link>
		                	</li>
		                </ul>
		            </div>
		        </li>
		       
		       
		        <li class="nav-level-0"><a href="javascript:void(0)">图文处理工具</a>
		            <div class="nav-level-1-wrapper">
		                <ul>
		                    <li>
		                    	<a href="https://www.fontke.com/tool/convfont/" target="_blank">字客网字-字体格式转换</a>
		                    </li>
		                    <li>
		                    	<a href="https://tinypng.com/" target="_blank">tinypng-图片压缩</a>
		                    </li>
		                    <li>
		                    	<a href="https://transfonter.org/ttc-unpack" target="_blank">transfonter-字体格式转换</a>
		                    </li>
		                    <li>
		                    	<a href="http://www.sfont.cn/tools/font" target="_blank"> sfont-字体格式转换</a>
		                    </li>
		                    <li>
		                    	<a href="http://www.qiuziti.com/" target="_blank">sfont-图文转换</a>
		                    <li>
		                    	<a href="javascript:void(0)" target="_blank">whatfont-字体查询</a>
		                    </li>
		                </ul>
		            </div>
		        </li>
		        </li>
		       
		        <li class="nav-level-0">		        
		        	<a href="javascript:void(0)">技术分享</a>
		            <div class="nav-level-1-wrapper">
		                <ul>
		                    <li>
		                    	<router-link to="/techCategory">经验技术分享</router-link>
		                	</li>		                   		                 
		                     <li>
	                    	<router-link to="/vueCategory">vue学习</router-link>                
		                    </li>
		                </ul>
		            </div>
		        </li>
		         <li class="nav-level-0">
		        	<router-link to="/webpageTest">网页测试</router-link>
		        </li>
		    </ul>
		</div>
		<div id="nav-popup"></div>
		<div id="title">
		 <!--戈麦斯前端-->
		</div>
		<div id="message">
			vue
		</div>
		
	</div>
	
</template>

<script>
	export default {
//		name: 'commonHeader'
	}
</script>
<style scoped>
	header{margin: 20px 0}

	#logo img{width: 100%}
	
	#title{}
	#message{
	    text-align: center;
	    font-size: 14px;
	    padding: 10px 0;
	    background: #f4f4f4;
	}
	
	
@media screen and (min-width:768px){

    #logo{width: 60px;height: 60px;margin: 0 auto}
    /*navigation*/
    #nav{height:60px;line-height:60px;background: #000e22;}
    #nav >ul{padding: 0; text-align: center;position: relative;margin: 0;font-size: 0}
    #nav a{text-decoration: none;}
    #nav ul>li{list-style: none;display: inline-block;padding: 0px 20px;font-size: 16px;}
    /*#nav ul>li:hover ul{display: block}*/

    #nav >ul>li>a{position: relative;display: block}
    #nav >ul>li>a:after{
                    display: block;
                    content: '';
                    width: 0;
                    height: 2px;
                    background: #ffffff;
                    position: absolute;
                    left: 50%;
                    top: 44px;
                    transition: all 600ms;

    }
    #nav >ul>li:hover >a:after{
        width: 100%;
        left: 0;
    }
    #nav >ul>li>a{color: #fff;}
    #nav ul>li>.nav-level-1-wrapper a{
        color: #000;
        position: relative;
        display: block;
        margin-bottom: 20px;
        padding: 3px 5px;
    }
    #nav ul>li>.nav-level-1-wrapper a:after{
        display: block;
        content: '';
        width: 0;
        height: 0;
        border-width: 0;
        border-style: solid;
        border-color: #000;
        position: absolute;
         left: 0;
        top: 0;
        transition: all 600ms;
        /*border-radius: 3px;*/
    }

    #nav ul>li>.nav-level-1-wrapper li:hover a:after{
        width: 100%;
        height: 100%;
        border-width: 1px 0 0 1px;

    }

    #nav ul>li>.nav-level-1-wrapper a:before{
        display: block;
        content: '';
        width: 0;
        height: 0;
        border-width: 0;
        border-style: solid;
        border-color: #000;
        position: absolute;
        right: -1px;
        bottom: -1px;
        transition: all 600ms;
        /*border-radius: 5px;*/
    }
    #nav ul>li>.nav-level-1-wrapper li:hover a:before{
        width: 100%;
        height: 100%;
        border-width: 0 1px  1px 0;

    }


    #nav ul>li>.nav-level-1-wrapper ul{
        width: 100%;
        background: #fff;
    }


    .nav-level-1-wrapper{
        position: absolute;
        box-shadow: 0 2px 4px 0 rgba(0,0,0,.3);
        width: 100%;
        left: 0;
        top: 59px;
        /*height: 0;*/
        line-height: normal;
        overflow: hidden;
        padding: 0;
        background: transparent;
        z-index: 6;
        transition: all 300ms;
        display: none;
        padding: 20px 0 30px;
        background: #fff;
    }
    #nav ul>li:hover .nav-level-1-wrapper{
        /*height:200px;*/
        z-index: 9;
        display: block;
    }

 
}

/*mobile*/
@media screen and (max-width:768px){
    #logo{width: 30px;height: 30px;margin: 0 auto}
    header{position: relative}
    #mobile-nav-icon{
        position: absolute;
        left: 10px;
        top: 5px;
        display: inline-block;
        width: 17px;
        height: 12px;
        border-width: 2px 0;
        border-style: solid;
        border-color: #000;
    }

    /*naigation*/
    #mobile-nav-icon:after{
        height: 0;
        position: absolute;
        left: 0;
        top: 5px;
        display: inline-block;
        width: 15px;
        content: '';
        border: 1px solid #000;

    }
    #nav{
        /*display: none;*/
        position: fixed;
        top: 0;
        left: -110%;
        height: 100vh;
        width: 80%;
        background: rgba(255,255,255,0.9);
        overflow-y: scroll;
        -webkit-overflow-scrolling: touch;
        transition: left 500ms;
        z-index: 99;
    }
    #nav-popup.active{
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        background: rgba(0,0,0,0.4);
        z-index: 98;
    }
    #nav.active{left: 0}
    #nav >ul{padding: 0;position: relative;margin: 0;font-size: 0;padding-bottom: 200px;}
    #nav a{text-decoration: none;}
    #nav ul>li{list-style: none;font-size: 16px;}
    #nav >ul>li{border-bottom: 1px solid #000;padding: 10px 20px;}
    #nav >ul>li a{display: block}
    #nav >ul>li >a:after{display: inline-block;content: "+";float: right;}
    #nav >ul>li.active> a:after{content: "_";margin-top: -8px;padding-right: 2px;}

    #nav ul>li>a{color: #000;}
    #nav ul>li>.nav-level-1-wrapper ul a{color: #000}
    #nav ul>li>.nav-level-1-wrapper{
        display: none;
        padding: 0;
    }
    #nav ul>li>ul>li{padding: 5px 10px}

  
}
</style>