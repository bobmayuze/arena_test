# arena_test
arena_test


arena submit tf \
             --name=uz-git-02 \
             --gpus=1 \
             --image=tensorflow/tensorflow:1.5.0-devel-gpu \
             --sync-mode=git \
             --sync-source=https://github.com/bobmayuze/arena_test.git \
             "python code/main.py"

arena submit tf \
             --name=uz-git-02 \
             --gpus=1 \
             --image=tensorflow/tensorflow:1.5.0-devel-gpu \
             --sync-mode=git \
             --sync-source=https://github.com/bobmayuze/arena_test.git \
             "python code/main.py"             

arena submit pytorch \
    --name=hsi-new-7 \
    --image=registry-vpc.cn-hangzhou.aliyuncs.com/pai-dlc/pai-pytorch-training:1.5-gpu-py3 \
    --cpu=8 \
    --memory=60Gi \
    --gpus=2 \
    --workers=1 \
    --sync-mode=git \
    --sync-source=https://github.com/graduter/hsi-3d-final.git \
    --data=yidi-hsi:/data/ \
    "pip install -r code/hsi-3d-final/requirements.txt && python code/hsi-3d-final/hsi1/p2_3D_noft_modified_multiG.py --data_dir=/data/hsi-data/ --result_dir=/data/hsi-data/result7.txt --model_name=resnet3D_modified_7"    