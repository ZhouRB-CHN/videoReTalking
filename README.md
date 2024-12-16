## videoReTalking

### 1. 运行准备

```powershell
# 创建并激活一个新的虚拟环境
conda create --name venv python = 3.10
conda activate venv

# 安装对应python包和torch
pip install -r requirements.txt
pip install torch==1.10.2+cull3 torchvision==0.3.0 --extra-index-url https://download.pytorch.org/whl/cull3
```

### 2. 数据准备

将音频和视频素材放到项目目录下的`./examples/audio`和`./examples/face`中

### 3. 启动推理

```python
# 以命令行的方式进行启动(例)
python inference.py  --face examples/face/1.mp4  --audio examples/audio/1.wav  --outfile results/1_3.mp4
```

其他参数说明

`--exp_img`: 预训练表情模板，默认值为neutral，可以设置为smile或指向一个图片路径

`--up_face`: 可以选择"surprise"或"angry"来改变表情
