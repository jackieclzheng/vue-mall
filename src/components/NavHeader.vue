<template>
    <div class="header">
        <div class="inner">
            <div class="demo1"><img src="./../images/logo.jpg" alt=""></div>
            <div class="demo2"><a href="" v-for="item in caidan" :key="item.id">{{item}}</a></div>
            <div class="demo3"><form action="" method="get">
                <input type="search" name="search" placeholder=" 请输入关键字...">
            </form>
            <img id="fdj" src="./../images/搜索图标.png" alt=""></div>
            <div class="demo4"><a href="">登录 |</a>
                <a href=""> 注册</a></div>
            <div class="demo5"><img id="fdj" src="./../images/右上角logo1.jpg" alt=""></div>
        </div>
    </div>
</template>

<script>
export default {
    name:'nav-header',
    data: function(){
        return{
            caidan:['首页','课程','Java','我的',]
        }
    }
}
</script>

<style>
    .header{
        position: absolute;
        top: 0px;
        width: 100%;
        height: 78px;
        line-height: 78px;
        border: 1px solid black;
        box-shadow: 0px 10px 10px #DCF2E5;
    }
    .inner{
        position: relative;
        width: 90%;
        height: 100%;
        line-height: 100%;
        margin: 0 auto;
    }
    
    .demo2 a{
        position: relative;
        color: black;
        font-size: 22px;
        text-decoration: none;
        margin-left: 40px;
    }
    form{
        position: relative;
        top:18px;
        left: 10%;
    }
    input{
        height: 38px;
        width: 280px;
        background-color: #E9E9E9;
        border-radius: 8px;
        border:none
    }
 
        
    .demo1,.demo2,.demo3,.demo4,.demo5{
        height: 100%;
        position: relative;
        float: left;
    }
    .demo1{
        width: 15%;
    }
    .demo1 img{
        width: 100%;
        height: 98%;
    }
    .demo2{
        margin-left: 50px;
        top: 30px;
    }
    .demo3{
        margin-left: 50px;
    }
    .demo3 #fdj{
        position: relative;
        width: 10%;
        top: -8px;
        left: 54%;
    }
    .demo4{
        margin-left: 60px;
    }
    .demo4 a{
        position:relative;
        top: 30px;
        color: gray;
        text-decoration: none;
    }
    .demo5{
        width: 50px;
        height: 50px;
        border: 1px solid black;
        margin: 15px auto auto 30px;
        border-radius: 25px;

    }
</style>