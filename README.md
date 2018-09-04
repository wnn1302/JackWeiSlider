# JackWeiSlider
这是一个jQuery滑动条（Slider）插件，简单易用，自持自定义样式。

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
设置拖动事件监听，返回当前进度比例。

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
### 3、GitHub地址

https://github.com/wnn1302/JackWeiSlider

### 4、注意事项:bug:

先说个Sorry啦，由于本作者偷懒了没做移动端适配，如需要在移动端使用需要自行配置哦~:green_heart::green_heart::green_heart:
