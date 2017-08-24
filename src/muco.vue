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
	</div>
</template>
<script>
	export default {
		name: 'muco',
		data () {
			return{
				// msg:'this is my first vue component',
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
			}
		}
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
</style>