# birds-eye-view

This repo is a copy of the original [repo](https://github.com/SAmmarAbbas/birds-eye-view), which is an implementation of the paper: ["A Geometric Approach to Obtain a Bird's Eye View from an Image", Ammar Abbas, Andrew Zisserman](https://arxiv.org/abs/1905.02231). The code estimates the homography matrix for a bird's eye view transformation along with some of the cameras's intrinsic and extrinsic parameters.

### How to use: 
- To run the code, you need to use an environment with TensorFlow 1.8 or 1.13.2, OpenCV, Numpy, and Matplotlib.

- Make sure the following file are installed completely: 

    ```data/saved_models/incp4/model.ckpt-17721.data-00000-of-00001```
    
    ```data/saved_models/vgg16/model.ckpt-20227.data-00000-of-00001```
    
    the files can be found [here](https://drive.google.com/open?id=1o9ydKCnh0oyIMFAw7oNxQohFa0XM4V-g).

- To predict bird's eye view from an image or a video, run the Following command: 

  ```python scripts/predict_horizon_vpz_homography.py --view_path $VIEW_PATH --model_name $CNN_MODEL```
  
  _Where:_
  
  $VIEW_PATH: path to the image/video
  
  $CNN_MODEL: name of the cnn model (available options: vgg-16, inception-v4)
  
  * Sample images and videos are provided in images and videos folders.
  * The output of the homography matrix will be saved as a .txt file in output folder along with the transformed image/video.

