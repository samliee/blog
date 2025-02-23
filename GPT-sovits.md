Repo: https://github.com/RVC-Boss/GPT-SoVITS

## System Requirements
- Ubuntu 20.04 LTSC
- Rocm installed

## Miniconda


## Install Pytorch

https://pytorch.org/

Select Compute Platform -> Rocm

## launch.sh

From https://zhuanlan.zhihu.com/p/681958706

```bash
#!/bin/sh

##source venv/bin/activate

export HSA_OVERRIDE_GFX_VERSION=10.3.0 #具体值可参考MarkA文章

export HIP_VISIBLE_DEVICES=0
export PYTORCH_HIP_ALLOC_CONF=garbage_collection_threshold:0.8,max_split_size_mb:512

python webui.py --listen
```

## run webui.py

```bash
bash launch.sh
```

## Extra Link
- Chinese Document: https://www.yuque.com/baicaigongchang1145haoyuangong/ib3g1e/
