<template>
    <div class="footer">
        <!-- 底部的头部 -->
        <div class="foot-top">
            <div class="ns">
                <img src="./img/footer.png" alt="">
            </div>
        </div>
        <!-- 底部主要内容 -->
        <ul class="foot-box">
            <li class="foot-li">
                <a href="#" class="foot-title">购物指南</a>
                <a href="#">服务商信息</a>
                <a href="#">购物流程</a>
                <a href="#">注册登录</a>
                <a href="#">商品评价</a>
            </li>
            <li class="foot-li">
                <a href="#" class="foot-title">配送方式</a>
                <a href="#">配送方式</a>
                <a href="#">配送方式信息</a>
                <a href="#">签收原则</a>
                <a href="#">物流查询</a>
            </li>
            <li class="foot-li">
                <a href="#" class="foot-title">支付方式</a>
                <a href="#">分期支付</a>
                <a href="#">支付方式</a>
                <a href="#">支付问题</a>
            </li>
            <li class="foot-li">
                <a href="#" class="foot-title">订单信息</a>
                <a href="#">订单信息</a>
                <a href="#">发票信息</a>
                <a href="#">手机激活查询</a>
            </li>
            <li class="foot-li">
                <a href="#" class="foot-title">售后服务</a>
                <a href="#">售后服务总则</a>
                <a href="#">24小时在线客服</a>
                <a href="#">联想服务入口</a>
                <a href="#">热门解决方案</a>
                <a href="#">Lenovo Quick Fix工具</a>
            </li>
            <li class="foot-li">
                <a href="#" class="foot-title">其他说明</a>
                <a href="#">服务承诺</a>
                <a href="#">账户安全</a>
                <a href="#">手机产品购买须知</a>
                <a href="#">环境信息</a>
            </li>
            <li class="phone-box">
                <h3>400-xxx-xxxx</h3>
                <span>周一到周日 9:00-21:00</span>
                <a href="#" class="phone-a"></a>
            </li>
        </ul>
        <!-- 底部说明 -->
        <div class="footer-bot">
            <span>个人用vue框架仿造的无交互简易联想商品页作品，如有侵权，联系删除</span>
        </div>
    </div>
</template>

<script>
    export default {
        name:''
    }
</script>

<style lang="css" scoped>
    .footer{
        background-color:#FBFBFB ;
        width: 100%;
    }
    .foot-top{
        height: 199px;
        background: #fff;
    }
    .ns{
        width: 1200px;
        height: 199px;
        margin: 0 auto;
    }
    .ns img{
        width: 1200px;
        height: 199px;
    }
    .foot-box{
        width: 1200px;
        height: 160px;
        list-style: none;
        margin: auto;
        padding: 70px 0 70px 76px;
        position: relative;
    }
    .foot-li{
        width: 152px;
        height: 134px;
        float: left;
    }
    .foot-box a{
        color: #757575;
        text-decoration: none;
    }
    .foot-box li>a{
        display: block;
        font-size: 13px;
        line-height: 13px;
        margin-bottom: 12px;
    }
    .foot-title{
        font-size: 16px !important;
        line-height: 16px;
        margin-bottom: 18px !important;
        font-weight: 600 !important;
        color: #424242 !important;
    }
    .phone-box{
        width: 223px;
        border-left: 1px solid #ccc;
        padding-left: 58px;
        margin-left: 5px;
        float: left;
    }
    .foot-box h3{
        color: red;
    }
    .foot-box span{
        font-size: 12px;
        color: #757575;
        line-height: 25px;
    }
    .phone-a{
        background: url(./img/phone.png);
        display: inline-block;
        width: 139px;
        height: 36px;
    }

    .footer-bot{
        width: 100%;
        height: 47px;
        border-top:1px solid #424141;
        background: #272727;
    }
    .footer-bot span{
        color: #757575;
        font-size: 14px;
        line-height: 46px;    
        margin-left: 725px;
    }
</style>