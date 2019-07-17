> 推荐看完P0、P1部分，P2部分可以使用Ctrl + F 查找你关注的内容

### P0

**请务必先看下环境准备一篇，很多问题都可以在环境准备完成后避免，尤其是小米、华为、VIVO、OPPO https://github.com/alipay/SoloPi/wiki/FirstUse** 

**请务必先看下环境准备一篇，很多问题都可以在环境准备完成后避免，尤其是小米、华为、VIVO、OPPO https://github.com/alipay/SoloPi/wiki/FirstUse** 

**请务必先看下环境准备一篇，很多问题都可以在环境准备完成后避免，尤其是小米、华为、VIVO、OPPO https://github.com/alipay/SoloPi/wiki/FirstUse** 



#### P1: 功能使用指南

录制回放： https://github.com/alipay/SoloPi/wiki/RecordCase

一机多控： https://github.com/alipay/SoloPi/wiki/OneToMany

性能工具： https://github.com/alipay/SoloPi/wiki/Performance

响应耗时： https://github.com/alipay/SoloPi/wiki/Performance#响应耗时计算工具

用例导出、导入、删除： https://github.com/alipay/SoloPi/wiki/RecordCase#用例列表

用例编辑：  https://github.com/alipay/SoloPi/wiki/CaseEdit

特定功能使用：  https://github.com/alipay/SoloPi/wiki/Actions



#### P2: 常见问题

Q: （小米）开始录制后点击控件没有弹出操作框

A: 请到`环境准备`一篇，看下小米的准备要求。

<br/>

Q: （华为）断开与PC连接后就提示ADB连接中断

A: 请到`环境准备`一篇，看下华为的准备要求。

<br/>

Q: （魅族）怎么找不到Soloπ的辅助功能

A: 在跳转后的`无障碍`菜单下。

<br/>

Q: （OPPO）Soloπ用一会儿就提示ADB连接断开

A: 部分OPPO手机有10分钟中断ADB的机制，可以通过连接PC来保持adb开启。

<br/>

Q: XX模拟器上用不了

A: Soloπ目前没有对模拟器进行兼容，请使用真机。

<br/>

Q: Soloπ录制开始后，手机卡住导致无法正常操作，点击控件也没有弹出功能框。

A: 可以使用双指进行操作，同时用两个手指进行点击、滑动，大概率是小米的情况，可以看下第一条。

<br/>

Q: 通用(控件)模式怎么回放失败了啊？

A: 在用例录制时点到控件会有红色框提示操作区域，可以确认下是不是操作到你实际想要操作的控件；同时，用例编辑页面也能看到控件的截图，可以确认下用例是否符合预期。

<br/>

Q: 图像模式怎么回放失败了啊？

A: 可以看一下你框选的区域是不是容易变化、或者特征过少（没什么边界信息），这些可能导致图像查找不到。

<br/>

Q: 想自定义数据存放的文件夹

A: 正在开发。

<br/>

Q: 一机多控主从机连不上。

A: 具体需要分析下

   场景一： 主机扫从机二维码，两边都没有toast提示

   原因：请看下主从机是不是在同一个wifi网络下，两边IP是否可以互联。网络问题可以通过以下方式验证：将主从机连接到同一个手机开的热点，然后再启动一机多控，看看是否可以连接。

   场景二： 有toast，从机悬浮窗没有缩小。

   分析：可能从机之前被扫过码，可以尝试先关闭从机的悬浮窗，然后重新启动一机多控。如果还是不行，可以在群里抛出来。

<br/>

Q: 连接成功，从机没有跟着主机操作

A: 主从机需要在同一个界面上才可以同步操作，同时也可以看下是不是从机或主机网络状态出现变化，导致IP地址变化。校验方法：执行全局滑动操作。

<br/>

Q: 我在主机上执行导出的用例，怎么通过`adb pull /storage/emulated/0/xxx`拉不出来？

A: 请通过一下三个步骤进行确认：

   第一步：请确认下Soloπ设置里 导入外部用例 菜单项内容，是 `/storage/emulated/0/solopi/import` ，还是 `/storage/emulated/0/Android/data/com.alipay.hulu/files/solopi/import` ，或者是其他的值，这个决定export目录具体是在哪个位置。

   第二步：在手机上使用任意的文件管理器，以华为自带的文件管理为例，看下内部存储中是否有 `solopi` 文件夹，如果有的话进入查看是否有 `export` 文件夹，这里是用例实际导出的目录。如果导入外部用以菜单项内容为 Android/data/com.alipay.hulu， 则进入内部存储中 `Android/data/com.alipay.hulu/files/solopi/export` 目录。同样确认下是否生成导出的用例json文件。

   第三步：如果步骤2中找不到对应的用例，再执行一次导出用例，然后将/sdcard/Android/data/com.alipay.hulu/cache/logs/中最新一条log日志导出来提一下issue。

<br/>

Q: 我自己打的包，卡在闪屏不动了

A: 看下有没有关闭instant run

<br/>

Q: 我自己打的包，XXXX功能用不了

A: 看看我们提供的release包是否可用，确认下包括buildTool版本、targetApi版本、gradle版本是否改过，改动这些信息可能导致功能无法使用。

<br/>

Q: 点击开始后没有跳转到应用首页

A: 可以看下应用是不是有两个Launcher，比如引入了LeakCanary，会多生成一个Launcher图标，导致soloπ无法进入应用，可以手动启动一下应用。

<br/>

Q: 响应耗时算的和我点结束的时间一样

A: 响应耗时的终点是根据当前屏幕是否在变化而确定的，如果屏幕上有较大区域的动画，或者是在拍照预览界面，会给响应耗时计算带来误差。

<br/>

Q: XXX类型应用支持吗？

A: 可能支持，你可以下载试用一下，控件模式找不到的切换成图像模式。

<br/>

Q: 我的游戏怎么拿不到FPS数值？

A: 目前我们的FPS暂时只支持Native、H5应用，游戏应用暂不支持，相关支持正在做。

<br/>

Q: 图像模式用不了

A: 看看手机能不能访问外网，第一次使用时会自动下载图像处理和截图的插件，**需要访问github的cdn**。关于如何确定你的手机能否正常访问，你可以在手机上手动下载这个文件进行测试 https://github.com/alipay/SoloPi/raw/master/plugins/hulu_imageCompare_v8a.zip

<br/>

Q: 辅助功能已经开启了，但还是校验失败

A: 可以先将Soloπ的辅助功能关闭掉，然后重启下Soloπ，再去开启辅助功能。

<br/>

Q: 如何接入Jenkins

A: 相关内容正在研究。

<br/>

Q: 用例批量导出

A: 相关内容正在研究。

<br/>

Q: 用例执行结果有保存吗？

A: 现在还没有保存结果，相关内容之后会进行补充。