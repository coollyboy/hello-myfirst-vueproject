<template>
	<div  id="muco">
		<!-- <h1 v-text="msg"></h1> -->
		<div class="top">
          <div class="top_content">
                <ul>
                      <li v-for="itemtop in itemtops "><a>{{itemtop.addour}}</a></li>
                </ul>
          </div>
      </div><!--top结束-->
      <div class="wrap">
             <div class="logo">
              	<div class="logo_left">
              		<img src="./assets/logo.jpg" alt="慕课网"/>
              	</div>
              	<div class="logo_right">
              		<img src="./assets/tel.jpg" alt="服务热线" /><div class="logo_right_tel" v-html="tel"></div>
              	</div>
            </div> <!--logo结束-->
	        <div class="nav">
	            <div class="nav_left"></div>
	            <div class="nav_mid">
	                  <div class="nav_mid_left">
	                        <ul>
	                          <li v-for="list in listhtml "><a> {{list.url}} </a></li>
	                        </ul>
	                  </div>
	                  <div class="nav_mid_right">
	                    <form action="" method="post">
	                      <input type="text" class="search_text" v-model ="inputtext"/>
	                    </form>
	                  </div>
	             </div> 
	            <div class="nav_right"></div>
	       </div><!-- nav结束 -->
	        <div class="ad" id="picBox"> 
		          <div class="loading"><img src="./assets/loading.gif" alt="图片加载中..."/></div>
		           <div class="pic">
		              <ul>
		                 <li><img src="./assets/ad2.jpg"/></li>
		                 <li><img src="./assets/ad3.jpg"/></li>
		                 <li><img src="./assets/ad4.jpg"/></li>
		              </ul>
		          </div>
            </div>
      </div>
	</div>
</template>
<script>
	export default {
		name: 'muco',
		data () {
			return{
				itemtops:[
                         {addour:'加入我们',
                          istype:'0',
				           },
				          {addour:'加入收藏',
				           istype:'1',
				           },
				          {addour:'设为首页',
				           istype:'2',
				           },
                      ],
                tel:'24小时服务热线：<span class="tel">123-456-7890 <span>',
                listhtml:[
                    {
                    	url:'首页',
                    },
                     {
                    	url:'关于慕课',
                    },
                     {
                    	url:'新闻动态',
                    },
                     {
                    	url:'课程中心',
                    },
                     {
                    	url:'在线课程',
                    },
                     {
                    	url:'人才招聘',
                    },
                ],
                inputtext:"",
			}
		},
	methods: {
     
	 },
	}

</script>


<style>
h1{
  font-weight: normal;
  text-align: center;
}
.top{
	width: 100%;
	height: 27px;
	background:url(./assets/top_bg.jpg)repeat-x;
}
.top_content
{
	width: 1000px;
	margin: 0 auto;
}
.top_content li
{
	list-style-image: url(./assets/li_bg.gif);
	
	float: right;
	width: 80px;
	line-height: 27px;
}
.top_content a:link,.top_content a:visited
{
	color: #8E8E8E;
	text-decoration: none;
}
.top_content a:hover,.top_content a:active
{
	color: #900;
	text-decoration: none;
}
.wrap
{
	width: 1000px;
	margin: 0 auto;
}
.logo
{
	height: 84px;
	background-color: #fff;
}
.logo_left
{
	width: 200px;
	float: left;
}
.logo_right
{
	width: 300px;
	float: right;
	margin-top: 28px;
	color:#8E8E8E;

}
.logo_right img
{
	vertical-align: middle;
	margin-right: 10px;
	float: left;
}
.logo_right_tel{
	float:left;
}
.tel{
	font-family: "微软雅黑";
	font-size: 16px;
	color: red;
}
.nav
{  
	height: 40px;
}
.nav_left
{  
	width: 10px;
	background-image: url(./assets/nav_left.jpg);
	background-repeat: no-repeat;
	
}
.nav_mid
{
	width: 980px;
	background-image: url(./assets/nav_bg.jpg);
	background-repeat: repeat-x;
	
}
.nav_right
{
	width: 10px;
	background: url(./assets/nav_right.jpg)no-repeat;
	
}
.nav_left,.nav_mid,.nav_right
{
	float: left;
	height: 40px;
}
.nav_mid_left,.nav_mid_right
{
	float: left;
}
.nav_mid_left
{
	width: 680px;
}
.nav_mid_right
{
	width: 300px;
}
.nav_mid_left li
{
    list-style-type: none;
	float: left;
	width: 100px;
	line-height: 10px;
	text-align: center;
	color: white;
}
.nav_mid_left a:link,.nav_mid_left a:visited
{
	text-decoration: none;
	color: #fff;
	font-size: 16px;
	font-family: "微软雅黑";
}
.nav_mid_left a:hover,.nav_mid_left a:active
{
	text-decoration: none;
	color: #ff0;
	font-size: 16px;
	font-family: "微软雅黑";
}
.search_text{
	width: 190px;
	height: 25px;
	margin-top: 5px;
	background-image: url(./assets/search.jpg);
	background-repeat: no-repeat;
	background-position: right center;
	background-color: #fff;
	padding-right: 25px;
	border: 1px solid #fff;
	border-radius: 5px;
}
</style>