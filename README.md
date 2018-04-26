# vue 添加购物车抛物线效果

> 基于 vue 实现一个类似饿了么，京东到家添加购物车的抛物线效果

## 构建运行

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```
## Q&A
* 为什么使用嵌套了的div来表示小球？
> 首先这是模拟了一个抛物线的效果，先普及一个基本知识，抛物线运动：分为水平的匀速运动和竖直向的自由落体（加速）。这里实现的思路是一个小球需要做2种运动，那么可以让这个小球做竖直向的加速运动，把这个小球放到一个盒子里面，让这个盒子做水平向的匀速运动。这样就完成模拟了一个抛物线运动，具体方法是在css里面分别设置transition，通过贝塞尔transition来模拟加速运动。如图所示：
![](http://cdn.zhangxuefei.site/wp-content/uploads/2018/04/img_5ae179323671c.png)
* 为什么使用了一个balls数组，而且存放5个元素
> 首先由于添加的过程，点击添加按钮可能比较连续，这样要模拟多个小球进入购物车的情况，所以需要预先准备几个box元素。为什么是5个？小球可以重复使用，根据网上的经验这里使用了5个，当然完全可以设置为7个8个。

## 效果
![](http://cdn.zhangxuefei.site/wp-content/uploads/2018/04/g-170x300.gif)
