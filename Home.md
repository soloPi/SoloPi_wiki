### 上手视频  Tutorial Videos

<video src = "Home/oneToMany.mp4" control="control" ></video>
[一机多控](Home/oneToMany.mp4)

### 简介 Introduction

SoloPi是一个无线化、非侵入式的Android自动化工具，公测版拥有录制回放、性能测试、一机多控三项主要功能，能为测试开发人员节省宝贵时间。
<br/>SoloPi is a wireless, non-invasive automation testing tool in android system, there are three main functionalities in public beta edition includes, record and replay, performance testing, control multiple phones from one phone(OneToMany).


如果你是第一次使用SoloPi，推荐你先了解SoloPi的[第一次使用](FirstUse)，再阅读下文中功能介绍部分。
<br/>If you are first time SoloPi User, Please read the SoloPi [first time user instructions](FirstUse), then read the document below.

### FAQ

SoloPi的 [FAQ](FAQ) 文档
<br/>SoloPi’s [FAQ](FAQ) document


### 功能介绍

#### 录制回放 Record and Replay

SoloPi拥有录制操作的能力，用户只需要通过SoloPi执行用例步骤，SoloPi就能够将用户的操作记录下来，并且支持在各个设备上进行回放，这一切都能够在手机上独立完成。详见[录制回放](RecordCase)一篇。
<br/>SoloPi has the ability to record user actions on the mobile phone, user only needs to record the detailed steps they want to test for their app as test cases. The recorded test cases can be replayed on any other android mobile devices. For more details, please read [record and replay](RecordCase) section.

#### 性能工具 Performance Testing Tool

SoloPi能够记录待测应用的各项指标，你可以在悬浮窗中观察实时更新的数据，也可以对性能数据进行录制，在录制结束后查看图表；同时，Soloπ还支持性能加压，能够对CPU、内存进行限制，复现应用在性能较差、网络环境不佳场景下的表现。
<br/>Soloπ can record app performance metrics, you can monitor app live performance data within the floating windows or record the app performance and visualize the data into chart. SoloPi also supports benchmark app testing through add load into CPU and Memory, User can monitor the app performance in different scenarios, replicate the performance issues under certain circumstances.

除了常规性能指标，SoloPi还提供了启动耗时计算工具，测试同学只需要点击两次按钮，就可以得到最贴近用户体验的启动耗时数据。同时，启动耗时计算工具还可以通过广播调用，可以非常方便的与UI自动化测试打通。详见[性能工具](Performance)一篇。
<br/>SoloPi also provides load time testing tool, which can be done through 2 clicks, this tool calculates the loading time performance which matches user experience. Load Time testing tool supports remote control through UI automation testing. For details, please read [performance testing tools](Performance).


#### 一机多控 OneToMany

SoloPi支持通过操作一台主机设备来控制多台从机设备，不需要在各个设备上分别进行重复冗杂的兼容性测试，能够极大提升兼容性测试的效率。详见[一机多控](OneToMany)一篇。
<br/>SoloPi support testing multiple android mobile through one device, User only need to operate on one device once and SoloPi will replay action to multiple devices in real time, which improves testing efficiency and testing coverage. For details, check [“One to Many”](OneToMany) section
