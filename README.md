[![zh](https://img.shields.io/badge/lang-zh-blue.svg)](./README.zh.md)

<br />
<div align="center">
    <a href="https://github.com/PlayForDreamDevelopers/support">
        <img src="https://www.pfdm.cn/en/static/img/logo.2b1b07e.png" alt="Logo" width="20%">
    </a>
    <h1 align="center"> PFDM Developer Support </h1>
    <p align="center">
        In this repository, you can find a collection of resources provided by the Play For Dream team for all developers.
        <br />
        <a href="https://github.com/PlayForDreamDevelopers/support/issues/new?template=bug_report.yml">Report Bug</a>
        &middot;
        <a href="https://github.com/PlayForDreamDevelopers/support/issues/new?template=feature_request.yml">Request Feature</a>
        &middot;
        <a href="https://github.com/PlayForDreamDevelopers/support/issues/new?template=documentation_update.yml">Improve Documentation</a>
    </p>

</div>

## About The Project

In this repository, you can find a collection of resources provided by the Play For Dream team for all developers.

> [!note]
> If you encounter any issues during development and are unsure which repository they should be submitted to, you are welcome to [report bug](https://github.com/PlayForDreamDevelopers/support/issues/new?template=bug_report.yml) this repository, and we will categorize them for you

## Unity Mirror Repos

Here are the repositories for the Unity Mirror packages.

> [!tip]
> The details of the mirror package, and how to use mirror package, please refer to [Mirror Package](https://developer.pfdm.cn/yvrdoc/unity/UserManual/DeveloperResources/PackagesMirror.html)

|                [Core][0001]                |                [Utilities][0002]                |                                                             [Platform][0003]                                                             |
| :----------------------------------------: | :---------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------: |
|      Package that provides XR ability      | Package that provides several utilities scripts |                                              Package that provides account platform ability                                              |
|             [Enterprise][0004]             |                 [Player][0005]                  |                                                           [Json-parser][0006]                                                            |
|     Package for _enterprise developer_     |  Package for high performance media playback.   |                                                   Package for convenient json handling                                                   |
|        [Android Device Core][0007]         |                  [UniRx][0008]                  |                                                           [Interaction][0010]                                                            |
| Package for high-performance JNI API calls |           Extension Package for UniRx           | Extension package for [XR Interaction Toolkit](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@3.1/manual/index.html) |

## Unity Samples

Here are the repositories for the Unity samples. For each sample project, our design goal is to provide examples of using specific functionality SDKs in the most minimal and least dependent way possible.

|                                      [DeviceSample][1000]                                       |                                     [YPlayerSample][1001]                                      |                    [SpatialAnchorSample][1002]                    |
| :---------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------: | :---------------------------------------------------------------: |
|               Learn how to get/modify device data via [Enterprise][0004] package                |             Learn how to play video in different way with [YPlayer][0005] package              |              Learn how to create/load spatial anchor              |
|                                    [SpatialMeshSample][1003]                                    |                                   [SceneAnchorSample][1004]                                    |                     [EyeTrackingSample][1005]                     |
|                           Learn how to load and display spatial mesh                            |                             Learn how to create/load scene anchor                              | Learn how to load eye tracking data and use it for interaction UI |
|                                       [HandSample][1006]                                        |                                     [PlatformSample][1007]                                     |                     [GetStarted-Unity][1008]                      |
|                              Learn how to load hand tracking data.                              | Learn how to use the platform package to perform account-related operations, i.e. entitlement. |           Learn how to create a minimal VR application            |
|                                   [CameraSample-Unity][1009]                                    |                                    [LBE Unity Sample][1010]                                    |
| Samples to demonstrate how to get hardware camera information of the Play For Dream MR Devices. |                             A collection of Unity samples for LBE.                             |


## FAQ

### Do I need to import the Unity SDK Integration package for the sample projects?

**No**

Our sample projects are already configured with the SDKs they depend on (usually directly referencing the mirror repositories). You can open the sample projects and the SDKs will be automatically fetched.

If you encounter package import errors after opening the project, you should troubleshoot the error instead of directly importing the SDK Integration package, as the package versions required by the project may be newer than those in the official SDK Integration package.

### What should I do if I encounter package import errors in the sample projects?

This issue usually occurs because you have not configured your GitHub SSH keys, meaning you cannot clone any public GitHub repositories via SSH.

You can try to clone this repository locally using the command line to verify if your SSH keys are configured correctly:

```bash
git clone git@github.com:PlayForDreamDevelopers/support.git
```

If the clone fails, refer to [Configuring GitHub SSH](support/ConfigGithubSSh.md) for guidance.

<!-- For the Unity Mirror package -->

[0001]: https://github.com/PlayForDreamDevelopers/com.yvr.core-mirror
[0002]: https://github.com/PlayForDreamDevelopers/com.yvr.utilities-mirror
[0003]: https://github.com/PlayForDreamDevelopers/com.yvr.platform-mirror
[0004]: https://github.com/PlayForDreamDevelopers/com.yvr.enterprise-mirror
[0005]: https://github.com/PlayForDreamDevelopers/com.yvr.player-mirror
[0006]: https://github.com/PlayForDreamDevelopers/com.yvr.json-parser-mirror

If you encounter package import errors after opening the project, you should troubleshoot the error instead of directly importing the SDK Integration package , as the package versions required by the project may be newer than those in the official SDK Integration package.
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
[0001]: https://github.com/PlayForDreamDevelopers/com.yvr.core-mirror
