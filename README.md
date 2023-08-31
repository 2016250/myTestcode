# gator:particle Light Sensor

[![Community Discord](https://img.shields.io/discord/448979533891371018.svg)](https://aka.ms/makecodecommunity)

The gator:particle, which includes the MAX30102 particle sensor can be purchased [here.](https://www.sparkfun.com/products/15271)
The gator:particle contains a MAX30102 particle sensor, which is mainly used for measuring heartrate.

![SparkFun gator:particle](https://raw.githubusercontent.com/sparkfun/pxt-gator-particle/master/icon.png)  

## ~ hint

To use this package, go to https://makecode.microbit.org, click ``Add package`` and search for **gator-particle**. The package is located [here](https://makecode.microbit.org/pkg/sparkfun/pxt-gator-particle)

## ~

## Basic usage

```blocks
//Initializes the gator:particle so we can use it
gatorParticle.begin()
```

Use ``||Initialize gator:particle sensor||`` to start the gator:particle up so we can read from it.

```blocks
//Reads a value from the Red or Infrared LED
gatorParticle.color(LEDToRead.Red)
```

Use ``||Red value||`` to get the value from the red channel. Grabbing the infrared channel is as easy as using the dropdown to call ``||Infrared value||``

```blocks
//Reads the heartbeat of a finger pressed to the sensor in BPM or as a running average of 4 BPM readings.
gatorParticle.heartbeat(heartbeatType.BPM)
```

Use ``||heartbeat in BPM||`` to get the heartbeat of finger on the sensor in BPM. Grabbing the average BPM is as easy as using the dropdown to call ``||heartbeat in AVG||``

## Example: Red Detector

```blocks
//Read red value and write it to the micro:bit screen as a bar graph.
gatorParticle.begin()
basic.forever(function () {
    led.plotBarGraph(
    gatorParticle.color(LEDToRead.red),
    65000
    )
})
```

## Supported targets

* for PXT/microbit

## License

MIT

```package
gatorParticle=github:sparkfun/pxt-gator-particle
```



> 在 [https://2016250.github.io/mytestcode/](https://2016250.github.io/mytestcode/) 打开此页面

## 用作扩展

此仓库可以作为 **插件** 添加到 MakeCode 中。

* 打开 [https://makecode.microbit.org/](https://makecode.microbit.org/)
* 点击 **新项目**
* 点击齿轮图标菜单下的 **扩展**
* 搜索 **https://github.com/2016250/mytestcode** 并导入

## 编辑此项目

在 MakeCode 中编辑此仓库。

* 打开 [https://makecode.microbit.org/](https://makecode.microbit.org/)
* 点击 **导入**，然后点击 **导入 URL**
* 粘贴 **https://github.com/2016250/mytestcode** 并点击导入

#### 元数据（用于搜索、渲染）

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
