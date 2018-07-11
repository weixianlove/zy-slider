# zy-slider
微信小程序双向滑动slider

![双向slider截图](https://github.com/weixianlove/zy-slider/blob/master/屏幕快照%202018-07-11%20下午8.09.46.png);

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
```

###### wxss:
```
.zy-slider {
    margin: 60rpx;
}
```
