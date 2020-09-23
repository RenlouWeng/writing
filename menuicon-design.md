#实际操作

``` html
<!DOCTYPE html>
<html>
<head>
</head>

<style type="text/css" media="screen">
       
.menuicon{
    width: 48px;
    height: 48px;
    z-index: 1;  
    position: absolute;
    background-color: #f5f5f5;
}
.menuicon-label{
    width: 48px;
    height: 48px;
    display: block;
    position: absolute;
    cursor: pointer;
    z-index: 2;
}

#menuicon-label-state{
    display: none;
}

/* 当checkbox被点击的时候，将menuicon-bread-top和menuicon-bread-bottom各自向反方向旋转45度，同时menuicon-bread-crust-top和menuicon-bread-crust-bottom移到中间的位置 */
#menuicon-label-state:checked ~ .menuicon-bread-top{
    transform: rotate(45deg);
}
#menuicon-label-state:checked ~ .menuicon-bread-bottom{
    transform: rotate(-45deg);
}
#menuicon-label-state:checked ~ .menuicon-bread .menuicon-bread-crust-top{
    transform: none;
}
#menuicon-label-state:checked ~ .menuicon-bread .menuicon-bread-crust-bottom{
    transform: none;
}

.menuicon-bread{
    width: 30px;
    height: 30px;
    display: inline-block;
    left: 9px;
    top: 9px;
    position: absolute;
}

.menuicon-bread-crust{
    width: 16px;
    height: 1px;
    left: 7px;
    position: absolute;
    display: inline-block;
    background: red;
}

.menuicon-bread-crust-top{
    top: 14px;
    position: absolute;
    display: inline;
    transform: translateY(-3px);
}
.menuicon-bread-crust-bottom{
    bottom: 14px;
    position: absolute;
    display: inline;
    transform: translateY(3px);
}

</style>

<body>
    <div class = "menuicon">
        <label class = "menuicon-label" for="menuicon-label-state"></label>
        <input type="checkbox" id="menuicon-label-state">
        <span class="menuicon-bread menuicon-bread-top">
            <span class="menuicon-bread-crust menuicon-bread-crust-top"></span>
        </span>
        <span class="menuicon-bread menuicon-bread-bottom">
            <span class="menuicon-bread-crust menuicon-bread-crust-bottom"></span>
        </span>
    </div>
</body>
    
    
</html>
```