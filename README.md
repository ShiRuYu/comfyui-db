# ComfyUI 工作流与插件目录

这里收录个人使用的 ComfyUI 工作流、相关自定义节点和插件 Git 地址。工作流 JSON 可从本仓库下载；原发布页链接目前未收录。

## 工作流

| 名称 | 说明 | 文件 |
| --- | --- | --- |
| Qwen-Image 2.1 功能流（高清局部编辑与扩图） | 基于 Qwen-Image 2.1，包含高清局部编辑、图像扩展和生图功能。 | [下载 JSON](workflows/qwen-image21-highres-edit-outpaint.json) |
| Qwen-Image 2.1 图像编辑与生图（Viggle Turbo 六步版） | 基于 Qwen-Image 2.1 和 Viggle Turbo 六步 LoRA 的图像编辑与生图工作流，需配套自定义节点脚本。 | [下载 JSON](workflows/qwen-image21-viggle-turbo-6step.json)；[自定义节点脚本](workflows/viggle_turbo.py) |
| Qwen-Image 2.1 图像编辑（GGUF） | GGUF 量化版 Qwen-Image 2.1 图像编辑模板，支持编辑主图和多张参考图、尺寸控制及结果对比；需要 ComfyUI-GGUF 插件。([插件链接](https://github.com/leejet/ComfyUI-GGUF.git)) | [打开工作流](workflows/image_qwen_image_2_1_image_edit_gguf.json) |
| Qwen-Image 2.1 图像编辑 | Qwen-Image 2.1 图像编辑模板，支持编辑主图并结合参考图，附编辑提示、尺寸控制和示例素材说明。 | [打开工作流](workflows/image_qwen_image_2_1_image_edit1.json) |
| Qwen-Image 2.1 文生图 | Qwen-Image 2.1 文生图模板，支持 LoRA 与尺寸设置，并附透明背景 PNG 的提示写法和模型下载说明。 | [打开工作流](workflows/image_qwen_image_2_1_t2i1.json) |
| Z-Image-Turbo Fun Union ControlNet | Z-Image-Turbo 搭配 Fun Union ControlNet 的控制图生成模板，以 Canny 为示例，可替换为 HED、深度、姿态或 MLSD 等控制条件。 | [打开工作流](workflows/image_z_image_turbo_fun_union_controlnet2.json) |
| Z-Image-Turbo 文生图 | Z-Image-Turbo 文生图模板，包含提示词示例、模型下载链接和工作流问题反馈说明。 | [打开工作流](workflows/image_z_image_turbo1.json) |
| Qwen-Image 2.1 Viggle Turbo 六步图像编辑 | 支持多张参考图和可选提示词增强的 Viggle Turbo 六步图像编辑工作流，采用 CFG 关闭采样；需要自定义 Viggle 节点和模型。 | [打开工作流](workflows/Qwen-Image-2.1-viggle-turbo-i2i-6step.json)；[Viggle 节点脚本](workflows/viggle_turbo.py) |
| Qwen-Image 2.1 Viggle Turbo 六步文生图 | 支持可选提示词增强和画幅设置的 Viggle Turbo 六步文生图工作流，采用 CFG 关闭采样；需要自定义 Viggle 节点和模型。 | [打开工作流](workflows/Qwen-Image-2.1-viggle-turbo-t2i-6step.json)；[Viggle 节点脚本](workflows/viggle_turbo.py) |

### 使用 Viggle Turbo 工作流

将 [`viggle_turbo.py`](workflows/viggle_turbo.py) 放入 ComfyUI 的 `custom_nodes` 目录，然后重启 ComfyUI。工作流所需的模型和示例输入图片没有包含在本仓库中；模型下载地址保留在工作流 JSON 内，使用时请按需准备模型并重新选择输入图片。

## 插件

| 插件 | 用途 | Git 地址 | ComfyUI-aki-v3.2 `custom_nodes` |
| --- | --- | --- | --- |
| ComfyUI-Inpaint-CropAndStitch | 局部修复 | [GitHub](https://github.com/lquesada/ComfyUI-Inpaint-CropAndStitch.git) | 已安装 |
| rgthree-comfy | 基础节点/随机种子/图像对比 | [GitHub](https://github.com/rgthree/rgthree-comfy) | 已安装 |
| ComfyUI-Easy-Use | 基础插件 | [GitHub](https://github.com/yolain/ComfyUI-Easy-Use.git) | 已安装 |
| ComfyUI-KJNodes | 基础节点 | [GitHub](https://github.com/kijai/ComfyUI-KJNodes.git) | 已安装 |
| ComfyUI_essentials | 运算节点/锐化 | [GitHub](https://github.com/cubiq/ComfyUI_essentials.git) | 已安装 |
| ComfyTV | 节点画布式媒体工作台，可将图像、视频、音频等处理阶段串成完整流程。 | [GitHub](https://github.com/jtydhr88/ComfyTV.git) | 已安装 |
| comfyui_controlnet_aux | ControlNet 辅助预处理节点，可生成 Canny、姿态、深度等控制提示图。 | [GitHub](https://github.com/Fannovel16/comfyui_controlnet_aux) | 已安装 |
| ComfyUI_Custom_Nodes_AlekPet | 自定义节点合集，包含姿态与涂鸦控制、提示词翻译、图像视频生成和实用工具。 | [GitHub](https://github.com/AlekPet/ComfyUI_Custom_Nodes_AlekPet) | 已安装 |
| ComfyUI_IPAdapter_plus | IPAdapter 图像条件节点，可将参考图中的主体或风格迁移到生成结果。 | [GitHub](https://github.com/cubiq/ComfyUI_IPAdapter_plus) | 已安装 |
| ComfyUI_UltimateSDUpscale | 将大图切块进行图生图扩散放大，以较低显存需求改善放大细节。 | [GitHub](https://github.com/ssitu/ComfyUI_UltimateSDUpscale) | 已安装 |
| ComfyUI-Crystools | 包含资源监控、进度与耗时、图像和 JSON 对比、元数据及调试工具。 | [GitHub](https://github.com/crystian/ComfyUI-Crystools) | 已安装 |
| ComfyUI-DD-Translation | 面向新版 ComfyUI 的简体中文界面翻译，并适配常用自定义节点。 | [GitHub](https://github.com/Dontdrunk/ComfyUI-DD-Translation) | 已安装 |
| ComfyUI-GGUF | 为 ComfyUI 增加 GGUF 量化格式模型的加载与推理节点。 | [GitHub](https://github.com/leejet/ComfyUI-GGUF.git) | 已安装 |
| ComfyUI-Impact-Pack | 图像增强节点合集，提供检测、细化、放大和管线等功能。 | [GitHub](https://github.com/ltdrdata/ComfyUI-Impact-Pack) | 已安装 |
| ComfyUI-LTXVideo | 为 LTX-2 视频生成提供额外的 ComfyUI 节点和示例工作流。 | [GitHub](https://github.com/Lightricks/ComfyUI-LTXVideo) | 已安装 |
| ComfyUI-Manager | 管理 ComfyUI 自定义节点的安装、移除、启用、停用和更新。 | [GitHub](https://github.com/Comfy-Org/ComfyUI-Manager) | 已安装 |
| ComfyUI-Prompt-Assistant | 调用云端或本地大模型翻译、扩写和润色提示词，并支持图像视频描述及历史记录。 | [GitHub](https://github.com/yawiii/ComfyUI-Prompt-Assistant.git) | 已安装 |
| ComfyUI-RMBG | 提供背景移除、图像抠图及人物、服装和物体分割节点。 | [GitHub](https://github.com/1038lab/ComfyUI-RMBG) | 已安装 |
| ComfyUI-VideoHelperSuite | 视频工作流节点，可加载视频或图像序列、抽取帧并将图像合成为视频。 | [GitHub](https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite) | 已安装 |
| ComfyUI-WanVideoWrapper | 为 WanVideo 及相关视频模型提供 ComfyUI 包装节点和工作流支持。 | [GitHub](https://github.com/kijai/ComfyUI-WanVideoWrapper) | 已安装 |

状态对应 `data/plugins.json` 中的 `installed` 字段；`true` 表示在记录的 `custom_nodes` 目录中找到该插件，`false` 表示未在该目录发现。

机器可读清单见 [`data/workflows.json`](data/workflows.json) 和 [`data/plugins.json`](data/plugins.json)。新增条目时同步更新对应 JSON 和本页索引；无需运行导入工具。

## 附录：安装与缺失节点排查

- 如果提示缺少节点，可先使用启动器的“工作流识别安装”功能检查并安装。
- 也可查看《常见问题记录》第 37 条：[夸克网盘文档](https://pan.quark.cn/s/b06e81f2d921)。
- 视频教程《ComfyUI从不认识到入门 完全指南》从 25:25 开始：[哔哩哔哩视频](https://www.bilibili.com/video/BV1XtFszgEo9/?share_source=copy_web&vd_source=f2ad5368a0b81f0dcc67cf3fda328164)。
- [Comfyui-TE 启动器下载](https://pan.quark.cn/s/100dd5a95c01)。
- 如果插件已安装仍提示缺少，可尝试更新 ComfyUI 核心和插件。
