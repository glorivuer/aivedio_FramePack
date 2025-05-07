
https://note.com/npaka/n/n33d1a0f1bbc1
https://note.com/npaka/n/n33d1a0f1bbc1
「Google Colab」で「FramePack-eichi」 
https://note.com/npaka/n/n1932501c05b6
在 Colab 上运行
（1）安装FramePack。
# FramePackのインストール
!git clone https://github.com/lllyasviel/FramePack
%cd FramePack
!pip install -r requirements.txt

（2）安装FramePack-eichi。
# FramePack-eichiのインストール
!git clone https://github.com/git-ai-code/FramePack-eichi.git tmp
!mv ./tmp/webui/* .
!rm -rf ./tmp

(3) 运行FramePack-eichi。
# FramePack-eichiの実行
!python endframe_ichi.py --share

（4）Gradio 共享链接将会显示，请点击它。

（5）指定图像和提示，然后点击“开始生成”。
这次我们指定了第一张图像（Image）和最后一张图像（Final）。

Cute cat-eared maid dancing in a cafe.
![image](https://github.com/user-attachments/assets/0e1d8025-2949-430b-97cd-db450d34f580)


（6）等待视频生成。
图像在几分钟内生成。当我尝试时，视频生成了，但没有显示视频预览。


（7）下载并转换视频。
生成的 mp4 文件无法在 QuickTime 中播放，因此我使用 ffmpe 或类似的标准编解码器再次对其进行了转换。





“FramePack-eichi”是“FramePack”的扩展版本，是一种在本地环境中运行的视频生成AI。
- 多关键帧支持
指定多个关键帧图像可以实现更复杂的动画。
- 灵活的视频长度设置
只需单击一下即可设置视频长度，从 1 秒到 20 秒，并且支持短视频和长视频。
・各部分的提示设置
您可以为每个部分指定单独的提示，以获得更精细的细节。
- 混元LoRA实验支持
​自定义您的模型以添加您自己独特的表达。

- 输出文件夹管理功能
它支持指定输出文件夹和独立于操作系统的打开方式。

・快速管理功能
​提示可以轻松保存、编辑和重复使用。

・日志功能
输出详细的进度信息和处理时间，并且在 Windows 上还提供声音通知。

・跨平台兼容性
基本功能在 Windows 以外的环境中可用。


