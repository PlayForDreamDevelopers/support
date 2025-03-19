[![en](https://img.shields.io/badge/lang-en-red.svg)](./README.md)

<br />
<div align="center">
    <a href="https://github.com/PlayForDreamDevelopers/support">
        <img src="https://www.pfdm.cn/en/static/img/logo.2b1b07e.png" alt="Logo" width="20%">
    </a>
    <h1 align="center"> PFDM 开发者支持 </h1>
    <p align="center">
        在这个仓库中，您可以找到由 Play For Dream 团队为所有开发者提供的资源集合。
        <br />
        <a href="https://github.com/PlayForDreamDevelopers/support/issues/new?template=bug_report.yml">报告问题</a>
        &middot;
        <a href="https://github.com/PlayForDreamDevelopers/support/issues/new?template=feature_request.yml">请求功能</a>
        &middot;
        <a href="https://github.com/PlayForDreamDevelopers/support/issues/new?template=documentation_update.yml">改进文档</a>
    </p>

</div>

## 关于项目

在这个仓库中，您可以找到由 Play For Dream 团队为所有开发者提供的资源集合。

> [!note]
> 如果您在开发过程中遇到任何问题，并且不确定应该提交到哪个仓库，欢迎您在此仓库中[报告问题](https://github.com/PlayForDreamDevelopers/support/issues/new?template=bug_report.yml)，我们会为您分类。

## Unity 镜像仓库

以下是 Unity 镜像包的仓库。

> [!tip]
> 有关镜像包的详细信息以及如何使用镜像包，请参阅 [镜像包](https://developer.pfdm.cn/yvrdoc/unity_CN/UserManual_CN/DeveloperResources/PackagesMirror.html)。

|        [核心][0001]         |    [实用工具][0002]    |                                                    [平台][0003]                                                    |
| :-------------------------: | :--------------------: | :----------------------------------------------------------------------------------------------------------------: |
|      提供 XR 功能的包       |  提供多个实用脚本的包  |                                                提供账户平台功能的包                                                |
|        [企业][0004]         |     [播放器][0005]     |                                                [Json 解析器][0006]                                                 |
|    为企业开发者提供的包     | 提供高性能媒体播放的包 |                                              提供方便的 json 处理的包                                              |
|    [安卓设备核心][0007]     |     [UniRx][0008]      |                                                    [交互][0010]                                                    |
| 提供高性能 JNI API 调用的包 |     UniRx 的扩展包     | [XR 交互工具包](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@3.1/manual/index.html) 的扩展包 |

## Unity 示例

以下是 Unity 示例的仓库。对于每个示例项目，我们的设计目标是以最小和最少依赖的方式提供使用特定功能 SDK 的示例。

|               [设备示例][1000]                |               [YPlayer 示例][1001]                |            [空间锚点示例][1002]            |
| :-------------------------------------------: | :-----------------------------------------------: | :----------------------------------------: |
| 了解如何通过 [企业][0004] 包获取/修改设备数据 | 了解如何通过 [YPlayer][0005] 包以不同方式播放视频 |         了解如何创建/加载空间锚点          |
|             [空间网格示例][1003]              |               [场景锚点示例][1004]                |            [眼动追踪示例][1005]            |
|          了解如何加载和显示空间网格           |             了解如何创建/加载场景锚点             | 了解如何加载眼动追踪数据并将其用于交互界面 |
|               [手部示例][1006]                |                 [平台示例][1007]                  |            [入门示例][1008]                  |
|          了解如何加载手部追踪数据。           |  了解如何使用平台包执行账户相关操作，例如授权。   |了解如何使用YVR Unity SDK和Unity XR交互工具包创建简单的VR应用程序|
|[相机示例][1009]|[LBE示例][1010]||
|提供了几个示例，展示如何获取 Play For Dream MR 设备的硬件相机信息。|提供了一些 LBE Unity示例||

<!-- For the Unity Mirror package -->

[0001]: https://github.com/PlayForDreamDevelopers/com.yvr.core-mirror
[0002]: https://github.com/PlayForDreamDevelopers/com.yvr.utilities-mirror
[0003]: https://github.com/PlayForDreamDevelopers/com.yvr.platform-mirror
[0004]: https://github.com/PlayForDreamDevelopers/com.yvr.enterprise-mirror
[0005]: https://github.com/PlayForDreamDevelopers/com.yvr.player-mirror
[0006]: https://github.com/PlayForDreamDevelopers/com.yvr.json-parser-mirror
[0007]: https://github.com/PlayForDreamDevelopers/com.yvr.android-device.core-mirror
[0008]: https://github.com/PlayForDreamDevelopers/com.yvr.unirx-mirror
[0010]: https://github.com/PlayForDreamDevelopers/com.yvr.interaction-mirror

<!-- For the Unity samples -->

[1000]: https://github.com/PlayForDreamDevelopers/DeviceSample-Unity
[1001]: https://github.com/PlayForDreamDevelopers/YPlayerSample-Unity
[1002]: https://github.com/PlayForDreamDevelopers/SpatialAnchorSample-Unity
[1003]: https://github.com/PlayForDreamDevelopers/SpatialMeshSample-Unity
[1004]: https://github.com/PlayForDreamDevelopers/SceneAnchorSample-Unity
[1005]: https://github.com/PlayForDreamDevelopers/EyeTrackingSample-Unity
[1006]: https://github.com/PlayForDreamDevelopers/HandSample-Unity
[1007]: https://github.com/PlayForDreamDevelopers/PlatformSample-Unity
[1008]: https://github.com/PlayForDreamDevelopers/GetStarted-Unity
[1009]: https://github.com/PlayForDreamDevelopers/CameraSample-Unity
[1010]: https://github.com/PlayForDreamDevelopers/LBESample-Unity/blob/main/README.zh.md