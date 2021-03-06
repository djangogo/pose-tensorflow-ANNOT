# Human Pose Estimation with TensorFlow
这是pose-tensorflow的注释加强版，便于自己理解用，此外还添加了一些好用的功能

1. 添加了指定数据集目录的功能

欢迎提问题一起讨论，下面给出作者的信息

Here you can find the implementation of the CNN-based human body part detectors,
presented in the [DeeperCut](http://arxiv.org/abs/1605.03170) paper:

**Eldar Insafutdinov, Leonid Pishchulin, Bjoern Andres, Mykhaylo Andriluka, and Bernt Schiele
DeeperCut:  A Deeper, Stronger, and Faster Multi-Person Pose Estimation Model
In _European Conference on Computer Vision (ECCV)_, 2016**
For more information visit http://pose.mpi-inf.mpg.de

Python 3 is required to run this code.
First of all, you should install TensorFlow as described in the
[official documentation](https://www.tensorflow.org/install/).
We recommended to use `virtualenv`.

You will also need to install the following Python packages:

```
$ pip install scipy scikit-image matplotlib pyyaml easydict
```

When running training or prediction scripts, please make sure to set the environment variable
`TF_CUDNN_USE_AUTOTUNE` to 0 (see [this ticket](https://github.com/tensorflow/tensorflow/issues/5048)
for explanation).

If your machine has multiple GPUs, you can select which GPU you want to run on
by setting the environment variable, eg. `CUDA_VISIBLE_DEVICES=0`.

## Demo code

```
# Download pre-trained model files
$ cd models/mpii
$ ./download_models.sh
$ cd -

# Run demo of single person pose estimation
$ TF_CUDNN_USE_AUTOTUNE=0 python demo/singleperson.py
```

## Training models

Please follow these [instructions](models/README.md)

## Citation
Please cite Deep(er)Cut in your publications if it helps your research:

    @article{insafutdinov2016deepercut,
        author = {Eldar Insafutdinov and Leonid Pishchulin and Bjoern Andres and Mykhaylo Andriluka and Bernt Schiele},
        url = {http://arxiv.org/abs/1605.03170}
        title = {DeeperCut: A Deeper, Stronger, and Faster Multi-Person Pose Estimation Model},
        year = {2016}
    }

    @inproceedings{pishchulin16cvpr,
	    title = {DeepCut: Joint Subset Partition and Labeling for Multi Person Pose Estimation},
	    booktitle = {CVPR'16},
	    url = {},
	    author = {Leonid Pishchulin and Eldar Insafutdinov and Siyu Tang and Bjoern Andres and Mykhaylo Andriluka and Peter Gehler and Bernt Schiele}
    }
