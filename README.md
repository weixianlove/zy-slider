# zy-slider
微信小程序双向滑动slider，可用于价格范围选取等功能。




<img src="https://user-images.githubusercontent.com/12731778/43645614-0b99621c-9765-11e8-8787-c1ac2d544c11.png" height = "500" />

一个选择数值范围的slider，双向可以滑动

先在要使用的地方的json文件中引入该组件
```
{
  "usingComponents": {
      "zy-slider": "../../component/zyslider"
  },
  "navigationBarTitleText": "zy-slider"
}
```

然后在wxml中使用
```
<view class="zy-slider">
    <zy-slider minValue="0" maxValue="100" min="0" max="100" bind:lowValueChange="lowValueChangeAction"
                bind:heighValueChange="heighValueChangeAction" />
</view>
```

###### 参数说明：
```
min: Number/String slider 最小值
max: Number/String slider 最大值
minValue: Number/String slider 左边滑块初始位置
maxValue: Number/String slider 右边滑块初始位置
bind:lowValueChange : function 左边滑块回调 {lowValue：lowValue}
bind:heighValueChange : function  右边滑块回调 {heighValue：heighValue}
blockColor : String slider 圆形滑块颜色（默认 #19896f）
backgroundColor : String slider 背景条的颜色（默认 #ddd）
selectedColor : String slider 已选择部分的颜色（默认 #19896f）
```
###### 方法说明：
```
reset(): 重置组件
show(): 显示组件
hide(): 隐藏组件
```
说明一下为何需要调用方法来隐藏 / 显示组件，若组件的上层 ```view```加上 ```style="display: none;"```隐藏再显示，组件恢复显示后布局可能会乱掉：

<img src="https://user-images.githubusercontent.com/12731778/43646337-3e6af154-9767-11e8-9a6e-ea4791b941f7.png" height = "100" />

解决方法是将组件放在需要隐藏的 ```view``` 之外，并单独调用内部的 ```show()``` 与 ```hide()``` 方法来单独显示 / 隐藏组件。


###### wxss:
```
.zy-slider {
    margin: 60rpx;
}
```

[简书](https://www.jianshu.com/p/7eaf95d1ae1f)地址
