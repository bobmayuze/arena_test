# arena_test
arena_test


arena submit tf \
             --name=uz-git-04 \
             --gpus=1 \
             --image=tensorflow/tensorflow:1.5.0-devel-gpu \
             --sync-mode=git \
             --sync-source=https://github.com/bobmayuze/arena_test.git:main \
             "python code/main.py"

arena submit tf \
             --name=tf-git \
             --gpus=1 \
             --image=tensorflow/tensorflow:1.5.0-devel-gpu \
             --sync-mode=git \
             --sync-source=https://code.aliyun.com/xiaozhou/tensorflow-sample-code.git \
             "python code/tensorflow-sample-code/tfjob/docker/mnist/main.py --max_steps 10000 --data_dir=code/tensorflow-sample-code/data"

arena submit tf \
             --name=uz-git-03 \
             --cpu=4 \
             --memory=30Gi \             
             --gpus=1 \
             --image=tensorflow/tensorflow:1.5.0-devel-gpu \
             --sync-mode=git \
             --sync-source=https://github.com/bobmayuze/arena_test.git \
             "python code/main.py"             

arena submit pytorch \
    --name=uz-git-t1 \
    --image=registry-vpc.cn-hangzhou.aliyuncs.com/pai-dlc/pai-pytorch-training:1.5-gpu-py3 \
    --cpu=4 \
    --memory=30Gi \
    --gpus=1 \
    --workers=1 \
    --sync-mode=git \
    --sync-source=https://github.com/bobmayuze/arena_test.git \
    "python code/main.py"    