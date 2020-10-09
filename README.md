# arena_test
arena_test


arena submit tf \
             --name=uz-git-01 \
             --gpus=1 \
             --image=tensorflow/tensorflow:1.5.0-devel-gpu \
             --sync-mode=git \
             --sync-source=https://github.com/bobmayuze/arena_test.git \
             "python code/main.py"