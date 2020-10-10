# arena_test
arena_test


arena submit tf \
             --name=uz-git-09 \
             --image=registry.cn-hangzhou.aliyuncs.com/pai-dlc/pai-tensorflow-training:1.12-cpu-py3 \
             --sync-mode=git \
             --sync-source=https://github.com/bobmayuze/arena_test.git \
             --env GIT_SYNC_BRANCH=main \
             "python code/arena_test/main.py"


k get pods/uz-git-07-chief-0 -oyaml
 k logs pods/uz-git-07-chief-0  -c init-code