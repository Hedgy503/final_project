
# cat_vs_dog

Helps differentiate the difference between the dogs and cats. Because certain breeds of both animals look opposite to each other.


## The Algorithm

The code gives the percentage of how much the animal is. Add images or other descriptions for your project here. 

## Running this project

1. cd ~/jetson-inference/
./docker/run.sh 



Opens the docker.



cd python/training/classification

Opens the folder.

python3 train.py  --lr 0.5 --model-dir=models/cat_vs_dog data/cat_vs_dog

python3 onnx_export.py --model-dir=models/cat_vs_dog


NET=models/cat_vs_dog
DATASET=data/cat_vs_dog

imagenet.py \
  --model=$NET/resnet18.onnx \
  --labels=$DATASET/labels.txt \
  --input_blob=input_0 \
  --output_blob=output_0 \
  $DATASET/test/cats/cat.10.jpg $DATASET/cat_1_output.jpg

2. Make sure to include any required libraries that need to be installed for your project to run.
