# 使用示例，根据实际路径修改

## env
cd /home/fudan248/zhangjinyu/code_repo/DATA620004-SS24/pj1/code/mmdetection
conda activate mmdetection

## single GPU trainig
CUDA_VISIBLE_DEVICES=6 python tools/train.py configs/yolo/yolov3_large_voc_v1_sgd.py

## multiple GPU training
bash ./tools/dist_train.sh ./configs/yolo/yolov3_large_voc_v1_sgd.py 8

## test
python tools/test.py configs/yolo/yolov3_large_voc_v1_sgd.py ckpts/latest.pth 