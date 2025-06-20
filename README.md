# VideoDepth
运行环境为python3.10.11 torch2.1.1+cu121 torchvision0.16.1
# 安装依赖包
pip install -t requirements.txt

(此时会自动安装torch，但安装的torch是CPU版本，Xformer编译有问题)
# 更新torch
pip3 install torch==2.1.1+cu121 --index-url https://download.pytorch.org/whl/cu121
# 运行命令
输出结果在outputs文件夹中

python run.py --input_video /che.mp4 --output_dir /outputs --encoder vits

--input_video：输入视频的路径

--output_dir：保存输出结果的路径

--input_size（可选）：默认情况下，我们使用输入大小进行模型推理。518

--max_res（可选）：默认情况下，我们使用最大分辨率进行模型推理。1280

--encoder（可选）：对于 video-depth-anything-v2-small，对于 video-depth-anything-v2-large。vitsvitl

--max_len（可选）：输入视频的最大长度，表示无限制-1

--target_fps（可选）：输入视频的目标 FPS，即原始 FPS-1

--fp32（可选）：使用精度进行推理。默认情况下，我们使用 .fp32fp16

--grayscale（可选）：保存灰度深度图，而不应用调色板。

--save_npz（可选）：以格式保存深度图。npz

--save_exr（可选）：以格式保存深度图。exr
