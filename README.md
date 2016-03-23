# Chapter1-Task5-Vizards

> 百度IFE - 第一阶段 - 任务5 - 零基础HTML及CSS编码(二)

### 任务描述
- 基于第一个任务“零基础HTML编码”的代码，参考下图，在步骤一的代码基础上增加CSS样式代码的编写
  ![任务5效果图](http://7xrp04.com1.z0.glb.clouddn.com/task_1_5_1.jpg)
- 头部和底部的黑色区域始终是100%宽
- 页面右侧部分为固定宽度，左侧保持与浏览器窗口变化同步自适应变化
- 左侧的各个模块里面的内容宽度跟随左侧整体宽度同步自适应变化
- 10张图片需要永远都完整展现，所以会随着宽度变窄，从两行变成三行甚至更多，也有可能随着宽度变宽，变成一行
- HTML 及 CSS 代码结构清晰、规范

### 参考资料
- [MDN HTML入门](https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/Introduction)
- [MDN CSS入门教程](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Getting_started)

### 实现总结
1. 页面采用HTML5标准，结构如下：

   >body
   >>header
   >>>nav
   
   >>main
   >>>article
   
   >>>aside
   
   >>footer
   
2. 在页面header标签的nav中，由于其前面的h1标签向左浮动(```float:left```)，它的子元素向右浮动(```float:right```)，
   如果不清除浮动就会导致header标签无法被撑开，其高度为0，因此在这里使用了一个nav标签的伪元素，代码如下：
   
   ```
   header nav:after {
      content: "";
      display: block;
      height: 0;
      clear: both;
      visibility: hidden;
   }
   ```
   
   由于```nav:after```本身被设为不可见，但是它作为header的子元素，```clear:both```生效了，因此使用伪元素也是清除浮动的一个重要方法
   
### 任务完成情况
- [x] 代码实现
- [x] 任务总结
- [x] 任务提交  
