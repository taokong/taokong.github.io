### Hyper R-CNN Installation

0. Build Caffe and pycaffe

    **Note:** Caffe *must* be built with support for Python layers!

      ```make
        # In your Makefile.config, make sure to have this line uncommented
        WITH_PYTHON_LAYER := 1
        # Unrelatedly, it's also recommended that you use CUDNN
        USE_CUDNN := 1
        # We use NCLL for multi-gpu training
        USE_NCCL := 1
        ```

1. Build the Cython modules
    ```
    cd $Hyper-R-CNN/lib
    make
    ```

2. installation for training and testing models on COCO dataset

    2.1 Create symlinks for the COCO dataset

        cd $Hyper-R-CNN/data
        ln -s $coco coco

    2.2 For training of COCO, use the 'train_hyper_rcnn/train_coco_hyper.sh'

    2.3 For testing of COCO, use the 'train_hyper_rcnn/test_coco_hyper.sh'
