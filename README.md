# Applet
微信小程序
/*
设置页面路径 数组的第一项代表小程序的初始页面。小程序中新增/减少页面，都需要对 pages 数组进行修改。
用于设置小程序的状态栏、导航条、标题、窗口背景色。
当设置 position 为 top 时，将不会显示 icon
tabBar 中的 list 是一个数组，只能配置最少2个、最多5个 tab，tab 按数组的顺序排序。 
*/

多了一些 wx:if 这样的属性以及 {{ }} 这样的表达式 在网页的一般开发流程中，我们通常会通过 JS 操作 DOM (对应 HTML 的描述产生的树)，以引起界面的一些变化响应用户的行为。例如，用户点击某个按钮的时候，JS 会记录一些状态到 JS 变量里边，同时通过 DOM API 操控 DOM 的属性或者行为，进而引起界面一些变化。当项目越来越大的时候，你的代码会充斥着非常多的界面交互逻辑和程序的各种状态变量，显然这不是一个很好的开发模式，因此就有了 MVVM 的开发模式(例如 React, Vue)，提倡把渲染和逻辑分离。简单来说就是不要再让 JS 直接操控 DOM，JS只需要管理状态即可，然后再通过一种模板语法来描述状态和界面结构的关系即可。 小程序的框架也是用到了这个思路，如果你需要把一个 Hello World 的字符串显示在界面上

小程序的启动
微信客户端在打开小程序之前，会把整个小程序的代码包下载到本地。
紧接着通过 app.json 的 pages 字段就可以知道你当前小程序的所有页面路径:

navigateTo, redirectTo 只能打开非 tabBar 页面。
switchTab 只能打开 tabBar 页面。
reLaunch 可以打开任意页面。
页面底部的 tabBar 由页面决定，即只要是定义为 tabBar 的页面，底部都有 tabBar。
调用页面路由带的参数可以在目标页面的onLoad中获取。

组件引用
