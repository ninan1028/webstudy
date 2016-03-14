
### less的一些笔记 

 less的注释 
两种方式 
/*nihao  */
//注释文本 

  声明变量  用 @声明 

@bg:red
body { b0ackground:@bg;}

 混合的两种方式 
1 直接一个类 
  .border { border: 1px solid blue ;}
 .box{
 width:20px;
.border;
 }

2 包含参数 
.border(@width){ border:@width solid blue;}
//默认参数
.border1(@width:1px){ border:@width solid blue;}

使用 
.box{
.border(1px)
}
.box{
.border();
}
