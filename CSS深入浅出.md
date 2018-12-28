# CSS深入浅出

## 一、文档流（Normal Flow）

### 1.1、文字两端对齐

```
多行文字两端对齐使用，使用text-align: justify;
通过伪元素达到多行文字的效果
.wzj{
	border: 1px solid #000;
	display: inline-block;
	width: 100px;
	height: 20px;	
	line-height: 20px;
	text-align: justify;				
	overflow: hidden;
}
.wzj::after{
	content: "";
	display: inline-block;
	width: 100%;
	border: 1px solid red;
}
```

### 1.2、文字溢出隐藏

1.单行溢出隐藏

```
 .wzj {
     width: 200px;
     border: 1px solid red;
     white-space: nowrap;
     overflow: hidden;
     text-overflow: ellipsis;
 }
 
 <!-- 单行文字溢出隐藏 -->
 <div class="wzj">不练剑了！不练剑了！不练剑了！</div>
```

2、多行文字溢出隐藏

```
   .wzj1 {
      width: 200px;
      border: 1px solid red;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
    }
    <!-- 多行文字溢出隐藏 -->
    <!-- css multiline text ellipsis -->
    <div class="wzj1">不练剑了！不练剑了！不练剑了！不练剑了！不练剑了！不练剑了！不练剑了！不练剑了！不练剑了！</div>
```

## 二、移动端

响应式项目，根据开发端不同分为

1. 先做手机，Mobile first
2. 先做PC，desktop first

### 2.1、移动端视口

```
<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
```

### 2.2、手机端的交互方式不一样

1. 没有 hover
2. 有 touch 事件
3. 没有 resize
4. 没有滚动条

## 三、Flex布局

### 3.1、特点

1. 与方向无关
2. 空间自动分配，自动对齐
3. 简单线性布局

### 3.2、flex布局检测

[flex测试游戏]: http://flexboxfroggy.com/#zh-cn

## 四、BFC

没有定义，只有特性/功能

### 4.1、触发条件

1. 浮动
2. 定位
3. 非块盒的块容器
4. overflow不为visible

## 五、手机专用自适应方案

前端像素单位：px,em,rem,vh,vw

### 5.1、rem

rem是根元素font-size大小，就是html的font-size

### 5.2、rem和em区别

rem是font-size为参考，em参考是自身的font-size

## 六、涟漪按钮实现

```
关键点
```

