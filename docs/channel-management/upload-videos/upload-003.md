# 上传高动态范围 (HDR) 视频

您可以将高动态范围 (HDR) 视频上传到 YouTube。与标准数字视频相比，HDR 视频的对比度更高，色彩更丰富。

观看者可以在兼容的移动设备和 HDR 电视上观看 HDR 视频，还可以利用 Chromecast Ultra 将 HDR 视频传输到 HDR 电视上。观看者将在视频播放器中每个画质选项（例如，1080p HDR）的后面看到“HDR”。

如果在非 HDR 设备上观看，HDR 视频会以标准动态范围 (SDR) 格式播放。

## 上传 HDR 视频

只有编解码器或容器中有 HDR 元数据的 HDR 视频才能在 YouTube 上正常播放。正确记录元数据的最可靠方式是[从支持的应用导出](https://support.google.com/youtube/answer/7126552?hl=zh-Hans&ref_topic=9257439&authuser=0#davinci_resolve)。

如果您无法导出标准 HDR 元数据，那么可以使用 [YouTube HDR 元数据工具](https://github.com/youtubehdr/hdr_metadata)将 HDR 元数据添加到视频中。仅当您的视频是使用 HDR 转换函数进行调色时，此工具才会正确工作。

**注意** ：如果您不确定自己的视频是否使用 HDR 转换函数进行了调色，则使用此工具将会严重扭曲您的视频。许多标题中包含“HDR”的视频不是使用 HDR 转换函数进行调色的。这些视频无法使用此工具。如果您不熟悉如何调色或从未对自己的视频进行过 HDR 调色，请不要使用 YouTube HDR 元数据工具。

如果您要对视频调色，请按 Rec. 2020 标准通过 PQ 或 HLG 转换函数进行调色。使用其他配置（包括 DCI P3）会产生不正确的结果。

在将视频正确标记为 HDR 后，可按照上传普通视频的流程将其上传。YouTube 会检测 HDR 元数据并对其进行处理，生成适用于 HDR 设备的 HDR 转换代码，以及适用于其他设备的 SDR 向下转换代码。

**注意** ：目前无法使用 YouTube 网络编辑器修改 HDR 视频。

## HDR 视频要求

在您上传视频后，YouTube 支持所有分辨率，且在必要时会自动将 HDR 视频转换为 SDR 视频。

## 上传要求

分辨率 720p、1080p、1440p、2160p
为获得最佳效果，请使用 UHD（而非 DCI）宽度（例如使用 3840x1600，而不要使用 4096x1716）。
帧速率 23.976、24、25、29.97、30、48、50、59.94、60
色深 10 位或 12 位
原色 Rec. 2020
颜色矩阵 Rec. 2020 非恒定亮度
EOTF PQ 或 HLG (Rec. 2100)
视频比特率 如果采用的是 H.264 编码，请使用[推荐的上传编码设置](https://support.google.com/youtube/answer/1722171)。
音频 与[推荐的上传编码设置](https://support.google.com/youtube/answer/1722171)相同

## HDR 视频文件编码

经测试，下列容器与编解码器的配对组合可正常发挥作用。您也许还可以使用其他带有 HDR 元数据的高品质 10 位编解码器。

|**容器**|**编码**|
| --- | --- |
|MOV/QuickTime|H.264 10 位

VP9 Profile 2

ProRes 422

ProRes 4444

DNxHR HQX|
|MP4|H.264 10 位

VP9 Profile 2

DNxHR HQX|
|MKV|H.264 10 位

VP9 Profile 2

ProRes 422

ProRes 4444

DNxHR HQX|

## HDR 元数据

要获得处理，HDR 视频必须将以下属性标记正确：

* 转换函数（PQ 或 HLG）
* 原色 (Rec. 2020)
* 矩阵（Rec. 2020 非恒定亮度）

使用 PQ 信号的 HDR 视频还应说明其在制作母版时所用的显示设备（SMPTE ST 2086 母版元数据）以及关于亮度的详细信息（CEA 861-3 MaxFALL 和 MaxCLL）。如果缺少这些信息，我们会使用 Sony BVM-X300 母版显示设备所对应的值。

您可以选择在 HDR 视频中包含动态 (HDR10+) 元数据，并且可以将这些元数据作为 [ITU-T T.35 终端代码](https://www.webmproject.org/vp9/#hdr10-metadata-handling)或 SEI 标头。

## HDR 制作工具

以下是您可以用来向 YouTube 上传 HDR 视频的工具示例：

* DaVinci Resolve
* Adobe Premiere Pro
* Adobe After Effects
* Final Cut Pro X

## 常见问题

## 不正确的色彩空间标记

在电影行业里，HDR 视频的母版通常是在 DCI P3 色彩空间里制作完成，采用 DCI (~D50) 或 D65 白点。这种格式不能用于向消费类电子产品传输内容。在制作母版时，请选择 Rec. 2020 原色（在许多应用中，Rec. 2100 标准指的是 Rec. 2020 色彩）。

一个很常见的错误就是在 P3 中制作母版，然后使用 Rec. 2020 原色标记结果。这样做会导致色调移位的过饱和图像。

## 围绕 SDR 转换的更多控件

YouTube 的 SDR 自动向下转换功能使用方便，可让您轻松取得理想结果。不过，对于难度大的视频片段，此功能可能无法提供完美的结果。我们正在努力优化 SDR 自动向下转换功能，以便能够出色处理所有材料。

您可以以 3D 查询表（简称 LUT）这种形式为 YouTube SDR 向下转换功能提供一些辅助信息。要生成此 LUT，请执行以下操作：

1. 在调色应用中加载您的 HDR 视频，但不要应用任何色彩管理。
2. 为您用于制作母版的显示设备设置 Rec. 709 色彩和 Gamma 2.4 转换函数。
3. 应用从 Rec. 2020 + ST. 2084 转换为 Rec. 709 的现有 LUT，然后在后续节点中更改主校正器、曲线和键，以获得所需的显示效果。
4. 以 .cube 格式将 LUT 导出到 HDR 视频所在的文件夹。
5. 选择 LUT 和 HDR 视频，然后拖放到元数据工具中。

该工具将应用 BVM-X300 的元数据，同时纳入 LUT 中的数据，以便为 SDR 向下转换功能提供辅助信息。

**注意** ：目前没有可用于支持 SDR 向下转化功能的空间或时间控件。这意味着，涉及模糊处理等控件的 Power Window（遮罩）和键将无法正常工作，而应用到个体镜头的调整也无法生效。

## 阴影中的噪点

在 PQ (ST 2084) 中制作母版时，大量的信号范围会被专用于处理阴影细节。ProRes 和 DNxHR 等数字中间编解码器会保留图像范围中的细节。在视频的深色图像区域可能会有噪点（看起来被图像中的高亮部分遮盖住了）。

YouTube 的视频处理流程可能会移除某些噪点以满足传输比特率要求。在为上传视频而渲染视频之前对视频进行去噪处理，能让您获得更大的控制力。如果视频在播放时看起来有“压缩过度”的感觉，也可以进行去噪处理。

我们一直在努力提高 YouTube 视频的画质，包括更好地处理上述情况。