https://x.com/CandidEighty/status/1929243622819717558


https://www.reddit.com/r/unstable_diffusion/s/RWa1KoysiO

第一步是提高分辨率，然后使用 DaVinci Resolve 的颜色选项卡为 VACE 创建蒙版。
我发现自己制作蒙版比使用某种分割模型更重要，这样我可以更好地控制蒙版。Resolve 的 Magic Mask 2 是一个很好的基础，但之后你可能需要补充一些手动创建/跟踪/关键帧形状的蒙版。

其思路是尝试用白色遮盖所有你希望 WAN VACE 改变的内容，并用黑色保留尽可能多的保持不变的内容。

WAN VACE 只会在白色区域上进行操作，并将其生成的内容与现有的未遮盖内容混合。

源视频分辨率为 1080p，因此其画质比 WAN VACE 生成的视频（约 960x540）更高。

因此，在使用 WAN VACE 生成 nsfw 视频后，我会重复使用遮罩，这样我只需要编辑视频中更改的部分，其余部分则保持原始画质。

我使用 ComfyUI 中的 SDXL 图像修复功能，为 AI 裸露上身的女性创建了一帧 NSFW 静态帧。务必确保使用的帧来自剪辑片段，否则，虽然效果还不错，但可能看起来不像你想要的参考帧。
![image](https://github.com/user-attachments/assets/f4e78af1-ec83-49f3-89dc-1691961f5ae4)

我修改的帧来自视频接近尾声的部分，因为之前的帧有很多运动模糊。

完全脱掉衬衫比我用 VACE 将 SFW 视频修改成 NSFW 视频的做法更进一步。我们拭目以待它的效果。

我修改的帧来自视频接近尾声的部分，因为之前的帧有很多运动模糊。

完全脱掉衬衫比我用 VACE 将 SFW 视频修改成 NSFW 视频的做法更进一步。我们看看 VACE 如何处理这个问题。直接用 WAN 处理的效果还不错，但修改区域周围有一个变色的光晕。Fusion 应该可以使用我在原帖中创建的遮罩，通过色彩校正节点来修正这个问题。

我能够使用色彩校正节点去除奇怪的光晕（尽管我必须调整 CC 节点上的原始蒙版，以防止其渗入背景）。

然后，我对素材进行了去噪，添加了调色，并添加了一些光晕和颗粒感。







I wrote a series of posts about how to do this on Twitter. But basically, you need to mask out the parts of the image that you want to change (and as best you can, only those parts). You can do that using After Effects or Resolve for more control.

Then you need to use SDXL (or another model) inpainting to generate one altered frame. You feed the video, the mask video, and the reference image into a simple Wan VACE workflow and render it out. It can help to use a LORA with breast bounce physics (there are some on Civit), but it's not strictly necessary from what I can tell.

EDIT: Twitter thread link (you'll need to be logged into an account that can view NSFW stuff)

You can use SAM2 Segmentation in comfy instead, much easier and faster.

Thanks! I've actually tried this The problem is I often want to make minor tweaks to the mask (erode/dilate). Getting a realistic result depends a lot on the mask including only exactly what you want to change (plus like 10–20px padding) and not masking the rest.

There are probably a bunch of situations where it's quicker/easier, but the tests/projects I've done have needed a custom touch: either using magic mask in Resolve and modifying, or just rotoscoping a generic shape to cover the region I want to mask.

There are mask manipulation nodes also in comfy that can grow mask by desired px count. SAM2 segmentation can mask only specific areas.



There's a wan vace subject replacement workflow on civit, which uses SAM2 you can use as reference. Here is a workflow i made, too: https://file.purinnyova.com/share/gSYhZyLq This workflow does both mask out the subject and overlay OpenPose on top of that.
