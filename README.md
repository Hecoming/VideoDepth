# VideoDepth
运行环境为python3.10.11 torch2.1.1+cu121 torchvision0.16.1
# 安装依赖包
cd Video-Depth-Anything
pip install -t requirements.txt
(此时会自动安装torch，但安装的torch是CPU版本，Xformer编译有问题)
# 更新torch
pip3 install torch==2.1.1+cu121 --index-url https://download.pytorch.org/whl/cu121
# 运行命令
输出结果在outputs文件夹中
python run.py --input_video ../che.mp4 --output_dir ../outputs --encoder vits
