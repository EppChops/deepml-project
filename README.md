# GIT (Generative Image 2 Text)
The git model that was used was the one from the github repo from the paper [GIT: A Generative Image-to-text Transformer for Vision and Language](https://arxiv.org/abs/2205.14100)

## Installation
Follow the instructions for installation from the github repo: [GIT: Installation](https://github.com/microsoft/GenerativeImage2Text/blob/main/README.md#installation)

## Inference on GIT Base
Inference on a single image is done through running the following command:
```shell
  # single image, captioning
  AZFUSE_TSV_USE_FUSE=1 python -m generativeimage2text.inference -p "{'type': 'test_git_inference_single_image', \
        'image_path': 'imagenet/[image_name].jpg', \
        'model_name': 'GIT_BASE', \
        'prefix': '', \
  }"
```

To run our chosen images a sequence of commands were used where the image path is changed every time according to the path to the images.

Image paths used:

```shell
'imagenet/ILSVRC2012_val_00004565.jpg'
'imagenet/ILSVRC2012_val_00004576.jpg'
'imagenet/ILSVRC2012_val_00004616.jpg'
'imagenet/ILSVRC2012_val_00004636.jpg'
'imagenet/ILSVRC2012_val_00004672.jpg'
'imagenet/ILSVRC2012_val_00004703.jpg'
'imagenet/ILSVRC2012_val_00004720.jpg'
'imagenet/ILSVRC2012_val_00004745.jpg'
'imagenet/ILSVRC2012_val_00004759.jpg'
'imagenet/ILSVRC2012_val_00004855.jpg'
'imagenet/ILSVRC2012_val_00004867.jpg'
'imagenet/ILSVRC2012_val_00004877.jpg'
'imagenet/ILSVRC2012_val_00004912.jpg'
'imagenet/ILSVRC2012_val_00004914.jpg'
'imagenet/ILSVRC2012_val_00004933.jpg'
'imagenet/ILSVRC2012_val_00004954.jpg'
'imagenet/ILSVRC2012_val_00004956.jpg'
'imagenet/ILSVRC2012_val_00004961.jpg'
'imagenet/ILSVRC2012_val_00004965.jpg'
'imagenet/ILSVRC2012_val_00004984.jpg'
```

Simply rerun the inference given the first command for every image path to obtain the image captionings used in the project for the GIT base model. 

# BLIP

## Conda enviroment
For running the blip model, we had to construct our own conda enviroment to fix some dependency issues, this yml file is provided by us.
```shell
conda env create -f blip.yml
```

## Selecting images
place any images in the imagenet folder (right now the images there are our sample images, but any can be placed here).

## Running BLIP
```shell
conda activate blip
python blip.py
```
