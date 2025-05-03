# aivedio_FramePack
任何人都可以轻松制作视频！ FramePack-eichi（EasyWanVideo版）简介  https://gosuloli.com/archives/1612

介绍
您需要：
基本用法
UI屏幕
每个项目/设置
生成模式
截面框架尺寸
所有填充
视频长度
最终帧（可选）
张量数据设置
解决
完成的框架
开始生成/停止生成按钮
部分设置
图像
LoRA设置
迅速的
及时管理
使用 TeaCache
使用随机种子
视频总长度（秒）
计步器
蒸馏CFG规模
要保存的 GPU 内存量（GB）（值越低 = VRAM 越多）
MP4压缩
完成后保留每个部分的视频 - 如果未选中，则仅保存最终视频（默认关闭）
完成后还会保存张量数据（.safetensors）——这些数据稍后可以合并到另一个视频中
静态图像存储部分
EndFrame效果调整
输出目标设置
我们先尝试制作一个视频
准备视频的插图
确定视频的长度
将插图设置为图像
提示设置
按下生成按钮
视频完成
概括

您想尝试视频制作但不知道从哪里开始吗？那么 FramePack-eichi 非常适合您。它是一款可以让任何人轻松制作高质量视频的工具，并且具有适合初学者的界面。

EasyWanVideo 允许您使用基于 FramePack-eichi 的 WebUI 版本。对于任何想要开始视频制作的人来说，这都是一个很好的起点。

EasyWanVideo 还可以使用与 FramePack 不同的视频生成模型（称为 Wan2.1）。目前这两个是最强的本地视频生成AI，所以我用的是EasyWanVideo的FramePack-eichi。

您需要：
安装 EasyWanVideo
请参阅以下文章了解安装说明。
由于更新，内容可能会发生变化，因此如果不起作用，请检查 EasyWanVideo 网站。
https://github.com/Zuntan03/EasyWanVideo
https://gosuloli.com/archives/1493


简单的安装步骤

右键单击并从 Zuntan03/EasyWanVideo（https://github.com/Zuntan03/EasyWanVideo）保存 EasyWanVideoInstaller.bat。
在浅路径（例如 C:/EasyWan/ 或 D:/EasyWan/）中准备一个空的安装文件夹，将 EasyWanVideoInstaller.bat 移动到那里并运行它。
当您看到消息“Windows 保护了您的 PC”时，请单击“高级”视图中的“运行”。
EasyWanVideo 安装完成后，您会在文件夹中找到 FramePackEichi.bat，双击它即可启动它。

FramePackEichi 安装仅在第一次启动。下载大约 50GB 需要一段时间。

安装完成后，FramePackEichi WebUI 将启动。
从下次开始，您将需要启动 FramePackEichi.bat 来使用 FramePackEichi。

如果您已经安装了 EasyWanVideo，请使用 Update.bat 进行更新以确保安全。

基本用法
UI屏幕
这是 UI 屏幕的图像。
![image](https://github.com/user-attachments/assets/4ee923d5-e582-4568-bfa8-4418566d1901)

