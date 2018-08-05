# JackWeiSlider
这是一个jQuery插件，简单易用，自持自定义样式的滑动条（Slider）

### 1、函数（Method）

#### enable():
允许鼠标拖动，默认允许。

#### disEnable():
禁止鼠标拖动。

#### setText(text):
设置提示文字，默认显示当前进度百分比。

#### setProgress(progress):
设置初始进度，默认为0.3，按归一化计算。

#### setOnStartDragCallback(callback):
设置开始拖动事件监听。

#### setOnDragCallback(callback):
设置拖动事件监听。

#### setOnStopDragCallback(callback):
设置停止拖动事件监听。


### 2、开发示例
![实际效果](https://github.com/wnn1302/JackWeiSlider/blob/master/screenshot.png)

```
<div id="sliderParent" style="padding: 50px;background-color: gray;display: inline-block;">
```

```

var option = {
        color: 'deepskyblue',
        width: '400px',
        progress: 0.3,
        handleSrc: 'img/slider_handle.png',
        isCustomText: false
    };
   
$('#sliderParent')
        .jackWeiSlider(option)
        // .setText('2018-4-5 02:39:00')
        .setProgress(0.6)
        .setOnStartDragCallback(function () {
            console.log('start');
        })
        .setOnDragCallback(function (p) {
            console.log(p);
        })
        .setOnStopDragCallback(function () {
            console.log('stop');
        });
```
