# layout-001
今天我们来实现一个 80 * 80 的红色方块在页面中居中的效果。

1. 定义背景页面

首先，我们需要把页面的高度重置为 100%。

通过对html 和 body 的 class 添加 h-full 属性，可以让页面保持 100% 的高度。
h-full 表示高度为 100%。
```html
<html lang="en" class="h-full">
<body class="h-full">
</body>
</html>
```

2. 添加 80 * 80 的红色方块   
Tailwind CSS 默认的body 字体大小为 16px，w-20 表示是宽度为 5rem(width: 5rem), 这样换算下来就是 80px。  
同理，h-20 表示高度为 80px。  
我们为方块添加上颜色为 bg-red-500，这样一个红色方块就添加成功了。  


```html
<body class="h-full">
    <div class="w-20 h-20 bg-red-500 "> 
    </div>
</body>
```
不过这个红色方块还在左上角，接下来我们把它放到中间居中。

3. 让 红色方块居中

在 body 中，添加 flex, justify-center items-center，就可以让它完全居中显示了。  


我们在方块的父节点，也就是 body 上添加 flex 布局, 这样 body 就遵循 flex 布局规则了。  
flex 定义了两根轴，一根叫主轴，一根叫交叉轴，如果只有一根主轴和一根交叉轴的时候，我们完全可以看成是 x 轴和 y轴，也就是水平的一根 x 轴 和垂直的一根 y 轴。
水平居中使用 justify-center ,它可以让子节点的元素沿着容器主轴的中心点对齐，简单的话描述就是水平居中。
垂直居中使用 items-center, 它可以让子节点元素沿着容器的交叉轴中心对齐项目，说人话就是垂直居中。

```html
  <body class="h-full bg-gray-800 flex  justify-center items-center">
    <div class="w-20 h-20 bg-red-500 "> 
    </div>
  </body>
```

1. 应用
- 登录窗口
- 弹出窗口

