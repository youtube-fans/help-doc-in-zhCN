# 上传 360 度全景视频

要观看 360 度全景视频，您需要在计算机上使用最新版本的 Chrome、Opera、Firefox 或 MS Edge 浏览器。在移动设备上，则需要使用最新版本的 YouTube 应用。

在计算机上，YouTube 支持在 Chrome、Firefox、MS Edge 和 Opera 浏览器中上传和播放 360 度全景视频。要上传 360 度全景视频文件，您需要在上传前使用某个应用或脚本对该文件进行修改。

您还可以在 YouTube 应用中观看 360 度全景视频。要获得身临其境的体验，请详细了解如何使用 [Cardboard](https://support.google.com/youtube/answer/6239930)。

第 1 步：制作视频

市面上现已推出很多与 YouTube 兼容的 360 度全景摄像机。

为取得最佳拍摄效果，请根据 [YouTube 高级规范](https://support.google.com/youtube/answer/1722171)要求，采用高分辨率对视频进行编码。目前，YouTube 支持帧速率为每秒 24、25、30、48、50 或 60 帧的 360 度全景视频。我们建议您以 7168x3584 或更高（最高 8192x4096）的分辨率，上传宽高比为 2:1、等距柱状投影格式的 360 度全景视频。

您也可以使用定制的相机装置和第三方拼接软件来制作 360 度全景视频。

第 2 步：准备上传

您的视频文件中必须包含特定元数据，否则将无法呈现 360 度全景效果。请按以下说明操作，安装可向新文件中添加必要元数据的应用。

**通过应用制作 360 度全景视频文件**

1. 下载最新的 [360 度全景视频元数据应用](https://github.com/google/spatial-media/releases/latest)。
2. 将下载的文件解压缩，然后打开 360 度全景视频元数据应用。如果您使用的是 Mac，则可能需要右键点击该应用，然后点击 **打开** 。
3. 选择视频文件。
4. 选中  **Spherical** （360 度）所对应的复选框，然后点击 Save as（另存为）；切勿选择“3D Top-bottom”（上下格式 3D）复选框。如需了解详情，请参阅[虚拟实境视频](https://support.google.com/youtube/answer/6316263)上传说明。
5. 为即将创建的文件输入名称。
6. 保存文件；新文件将自动创建并保存在与源文件相同的位置。
7. 将新文件上传至 YouTube。
8. 等待系统处理并实现 360 度全景效果，此过程最多可能需要一个小时。

您还可以使用 [Python 脚本](https://github.com/google/spatial-media/blob/master/spatialmedia/README.md)添加元数据。

第 3 步：上传文件

目前这些工具暂不支持 360 度全景视频：YouTube 视频编辑器、增强功能和片尾画面。

发布视频之前，您可以先在自己的计算机上观看视频文件，确保它能够呈现 360 度全景播放效果。视频上传后，最多可能需要等待 1 小时才能实现 360 度全景播放效果。

您可以通过 360 度全景视频左上角的平移按钮，以及可用来旋转视频的 WASD 键来确认视频是否为 360 度全景视频。

了解如何使用[空间音频](https://support.google.com/youtube/answer/6395969)、[360 度视频](https://support.google.com/youtube/answer/6178631)和[虚拟实境视频](https://support.google.com/youtube/answer/6316263)，以便让观看者在观看视频时体验到逼真的全方位环绕音效。