<template>
<!-- 轮播图 -->
<div class="showImg" >

    <img  @mouseover="changeInterval(true)" 
         @mouseleave="changeInterval(false)"  
         v-for="(item) in imgArr" 
         :key="item.id"
         :src="item.url" 
         alt="暂无图片" 
         v-show="item.id===currentIndex" 
         >

    <div  @click="clickIcon('up')"   class="iconDiv icon-left"> 
        <i class="el-icon-caret-left"><img src="./img/向左.png" alt=""></i>
    </div>

    <div  @click="clickIcon('down')"  class="iconDiv icon-right">
        <i class="el-icon-caret-right"><img src="./img/向右.png" alt=""></i>
    </div>

    <div class="banner-circle">
        <ul>
            <li @click="changeImg(item.id)" 
                v-for="(item) in imgArr" 
                :key="item.id"
                :class="item.id===currentIndex? 'active': '' "
             ></li>
        </ul>
    </div>
</div>
</template>

<script>
    export default{
        name:'',
        data(){
			return {
				currentIndex :0,
				timer:null,
				imgArr:[
					{	id:0,
                        url:require("./img/sp.jpg")
					},{
						id:1,
						url:require("./img/sp2.jpg")
					},{
						id:2,
						url:require("./img/sp3.jpg")
					},{
						id:3,
						url:require("./img/sp4.jpg")
					},
				]
			}
		},
		methods:{

			startInterval(){

				clearInterval(this.timer);
				this.timer = setInterval(()=>{
					this.currentIndex++;
					if(this.currentIndex > this.imgArr.length-1){
						this.currentIndex = 0
					}
				},3000)
			},
			clickIcon(val){
				if(val==='down'){
					this.currentIndex++;
					if(this.currentIndex===this.imgArr.length){
						this.currentIndex = 0;
					}
				}else{
					if(this.currentIndex === 0){
						this.currentIndex = this.imgArr.length;
					}
					this.currentIndex--;
				}
			},
			changeImg(index){
				this.currentIndex = index
			},
			changeInterval(val){
				if(val){
					clearInterval(this.timer)
				}else{
					this.startInterval()
				}
			}
		},
		mounted(){
			this.startInterval()
		}
	}

   
</script>

<style scoped>
    li {
        list-style-type: none;
    }
    .showImg{
        position: relative;
        width: 100%;
        height: 700px;
        margin: -10px auto;
        overflow: hidden;
    }
    .showImg img{
        width: 100%;
        height: 100%;
    }
    .showImg img:hover{
        cursor: pointer;
    }
    .iconDiv{
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        width: 30px;
        height: 30px;
        border: 1px solid #666;
        border-radius: 15px;
        background-color: rgba(125,125,125,.2);
        line-height: 30px;
        text-align: center;
        font-size: 25px;
        cursor: pointer;
    }
    .iconDiv{
        width: 30px;
        height: 30px;
    }
    .iconDiv:hover{
        background-color: white;
    }
    .icon-left{
        left: 10px;
    }
    .icon-right{
        right: 10px;
    }
    .banner-circle{
        position: absolute;
        bottom: 0;
        width: 100%;
        height: 20px;
        
    }
    .banner-circle ul{
        margin: 0 50px;
        height: 100%;
        text-align: right;
    }
    .banner-circle ul li{
        display: inline-block;
        width: 14px;
        height: 14px;
        margin: 0 5px;
        border-radius: 7px;
        background-color: rgba(125,125,125,.8);
        cursor: pointer;
    }
    .active{
        background-color: black !important; 
    }

</style>