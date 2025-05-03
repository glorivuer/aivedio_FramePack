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
![image](https://github.com/user-attachments/assets/f41ded20-c29b-4658-918c-4d608ee39286)
![image](https://github.com/user-attachments/assets/f87ae9f9-94f3-42cd-a5b5-125561f535ff)

每个项目/设置
生成模式
正常：一般生成 / 循环：用于循环播放视频

截面框架尺寸
1 秒 = 高质量，正常速度 / 0.5 秒 = 更流畅的动作（实验性功能）

所有填充
数字越小，对之前的图片的影响越小，并且运动越多。

视频长度
设置关键帧图像的复制范围和视频的长度

最终帧（可选）
Final 是最后一幅图像，Image 是第一幅图像（需要最后的关键帧图像或其中之一）。

张量数据设置
选中此框以上传张量数据。

解决
输出视频的参考分辨率。目前仅支持 512、640 或 768（建议使用 640）

完成的框架
逐帧生成视频，并显示完成的帧视频。然后将完成的帧连接起来，这样当您完成后，您将看到所有帧都连接在一起的完整视频。

开始生成/停止生成按钮
单击“开始生成”按钮开始生成视频。如果想要中途停止生成，只需按“结束生成”按钮即可停止并结束生成。

部分设置
当您想在第一幅插图和最后一幅插图之间插入另一幅插图来控制移动时，请使用此功能。

图像
在这里设置您想要制作成视频的插图。

LoRA设置
勾选使用 LoRA（需要 16GB VRAM 或更高）

迅速的
写提示来控制视频。

及时管理
注册、反映、清除和删除提示。注册常用的提示很方便。

使用 TeaCache
这会提高速度，但可能会导致手和手指的表现稍差。

使用随机种子
选中此框将每次创建一个随机种子值。

视频总长度（秒）
设置要生成的视频的长度。

计步器
不建议更改此值。

蒸馏CFG规模
不建议更改此值。

要保存的 GPU 内存量（GB）（值越低 = VRAM 越多）
指定要释放的 GPU 内存量。值越小 = 可用 VRAM 越多 = 速度越快，值越大 = 使用的 VRAM 越少 = 更安全

MP4压缩
数字越小，质量越高。 0 表示无压缩。如果出现黑屏，请将其设置为 16。

完成后保留每个部分的视频 - 如果未选中，则仅保存最终视频（默认关闭）
1 秒 = 高质量，正常速度 / 0.5 秒 = 更流畅的动作（实验性功能）

完成后还会保存张量数据（.safetensors）——这些数据稍后可以合并到另一个视频中
1 秒 = 高质量，正常速度 / 0.5 秒 = 更流畅的动作（实验性功能）

静态图像存储部分
1 秒 = 高质量，正常速度 / 0.5 秒 = 更流畅的动作（实验性功能）

EndFrame效果调整
调整最后一帧对整个视频的影响程度。较低的值对最后一帧的影响较小，从而可以更快地过渡到第一帧。 1.00 为正常运行。

输出目标设置
输出目的地仅限于webui下。

我们先尝试制作一个视频
设置有很多，但你不需要全部了解。让我们开始制作吧！

准备视频的插图
请准备一幅你想制作成视频的插图。

![image](https://github.com/user-attachments/assets/1452adfd-6893-468d-adfb-50f400030dc3)
确定视频的长度
确定视频的长度。这次我将在 3 秒内尝试。
视频长度越长，生成所需的时间越长。
![image](https://github.com/user-attachments/assets/1892f879-8576-4144-a39b-66dfa6c529d8)

将插图设置为图像
将您准备好的插图拖放到图像中。
![image](https://github.com/user-attachments/assets/b414f5e2-ec31-479a-bd15-68a8ba1fd519)

提示设置
默认提示是“一个角色做一些简单的身体动作”。

这次我将尝试按原样使用它。

![image](https://github.com/user-attachments/assets/4055f74a-40b9-4b50-afab-cd231ee233db)

按下生成按钮
单击“生成”按钮开始生成。
![image](https://github.com/user-attachments/assets/4046906a-1473-4e19-b33f-6dc078f8e6bc)

视频完成
就是这样！很简单！
请参阅本文以获取姿势集合。

https://gosuloli.com/archives/1591
https://gosuloli.com/archives/1578
https://gosuloli.com/archives/1600


您可能觉得视频制作很困难，但使用 FramePack-eichi（EasyWanVideo 版本），任何人都可以轻松创建高质量的视频。首先学习基本的用法，熟悉之后，下一步就是尝试更高级的设置。

FramePack-eichi 已更新一些我从未使用过的新功能。将来，我想探索使用这些功能可以做什么以及使用 FramePack-eichi 可以创建什么级别的视频。

最新资讯将会在X上发布，请关注我们！

https://x.com/Celestia_chibi



