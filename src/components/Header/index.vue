<template>
    <div>
        <!-- 导航 -->
        <nav class="nav">
            <div class="nav_logo">
                <img src="./img/logo.png" alt="">
            </div>
            <div class="nav_li">
                <ul>
                    <li><a href="https://shop.lenovo.com.cn/">商城首页</a></li>
                    <li><a href="#">注册</a></li>
                    <li>|</li>
                    <li><a href="#">登录</a></li>
                    <li><a href="#"><img src="./img/phone.png"></a></li>
                </ul>
            </div>
        </nav>
        <!-- 巨幕部分 -->
        <div class="jumbotron">
            <div class="jumbotron_img"><a href="https://shop.lenovo.com.cn/yogacto/index.html?pmf_source=P0000003194M0019"><img src="./img/logo4.png" alt=""></a></div>
        </div>
        <div class="ccc">

        </div>
    </div>
</template>

<script>

export default {
    name:'',
}
</script>

<style lang="css" scoped>
    .nav{
        width:100%;
        height: 60px;
        background: #fff;
        box-shadow: 1px 1px 3px rgb(44, 41, 41);
        top: 0;
    }
    .nav_logo{
        margin-left: 100px;
    }
    .nav_logo img{
        width: 178px;
        margin-top: 12px;
    }
    .nav_li{
        margin-top: -35px;
        margin-right: 140px;
        
        float:right;
    }
    .nav_li ul{
        list-style: none;
    }
    .nav_li li{
        font-size: 14px;
        padding: 5px;
        float: left;
        color: #b5b5b5;;
    }
    .nav_li a{
        color: #b5b5b5;
        text-decoration: none;
    }
    .nav_li a:hover{
        color: black;
    }
    .jumbotron{
        height: 304px;
        width: 1922px;
    }
    .jumbotron_img img{
        display: block;
        width: 100%;
        height: 100%;
    }
</style>