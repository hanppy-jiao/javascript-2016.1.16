# javascript-2016.1.16
获取ID，innerHTML，改变html属性，display，className


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
</head>
<style>
    body{font-size: 20px;}
    #txt{
        width: 800px;
        height: 600px;
        padding: 5px;
        border: 1px solid #FF6600;
    }
    p{
        line-height: 20px;
       text-indent: 2em;
    }
</style>
<script>
    //改变颜色
    function changeColor(){
        var txt=document.getElementById("txt");
        txt.style.color="red";
        txt.style.backgroundColor="blue";
    }
    //改变宽高
    function changeHw(){
        var txt=document.getElementById("txt");
        txt.style.width="500px";
        txt.style.height="500px";

    }
    function dis(){
        var txt=document.getElementById("txt");
        txt.style.display="none";
    }
    function show(){
        var txt=document.getElementById("txt");
        txt.style.display="block";
    }
    function qx(){
        var message=confirm("确定要重置所有设置？");
        if(message==true){
            txt.removeAttribute('style');
        }
    }
</script>
<body>
<h2 id="con">javascript入门编程</h2>
<div id="txt">
    <h5>JavaScript为网页添加动态效果并实现与用户交互的功能。</h5>
    <p>1. JavaScript入门篇，让不懂JS的你，快速了解JS。</p>
    <p>2. JavaScript进阶篇，让你掌握JS的基础语法、函数、数组、事件、内置对象、BOM浏览器、DOM操作。</p>
    <p>3. 学完以上两门基础课后，在深入学习JavaScript的变量作用域、事件、对象、运动、cookie、
        正则表达式、ajax等课程。</p>
</div>
<form>
    <input type="button" value="改变颜色" onclick="changeColor()">
    <input type="button" value="改变宽高" onclick="changeHw()">
    <input type="button" value="隐藏内容" onclick="dis()">
    <input type="button" value="显示内容" onclick="show()">
    <input type="button" value="取消设置" onclick="qx()">
</form>

</body>
</html>
