# JTF-SISR
# Gradient-guided Single Image Super-resolution based on Joint Trilateral Feature Filtering

The state of the arts (SOTAs) of single image super-resolution always exploit guidance from gradient prior.The fusion of gradient guidance is implemented by channel-wise concatenation followed by a convolutional layer. However,
the kernels sharing in spatial positions cannot adaptively tune the effect of gradient guidance for all feature positions. Toresolve this problem, a novel network module is proposed to
simulate the traditional Joint Trilateral Filter (JTF) by extending the definition domain from pixels to features. Moreover, to improve the efficiency and flexibility, the functions of JTF kernelgeneration for image features and gradient features are explicitly
learned instead of individual kernel weights, e.g., the exponentialfunctions in the traditional JTF. Based on the proposed JTF modules, this paper follows the gradient-guided framework which
simultaneously infers high-resolution (HR) image features and HR gradient features within two parallel branches, respectively.Specifically, by treating image features and gradient features
as cross guidance to each other, the proposed JTF modules adaptively adjust the fusion patterns for local features via a bi-directional way. By doing so, the quality of image features
and gradient features is alternatively enhanced. Compared with SOTAs, the proposed JTF-SISR shows improvement which is evaluated for multiple upsampling scales and degradation modes
on 5 synthetic datasets, i.e., Set5, Set14, B100, Urban100 and Manga109, and 1 real dataset, i.e., RealSRSet. 

### Train

Explain how to run the project

```
python main.py --model model --save cen_x4(Folder Name) –scale 4 --save_models --save_results --patch_size 128 --batch_size 16
```

### Test

Explain how to test the project

```
python main.py --model model --save cen_x4 --scale 4 --save_results --test_only --pre_train /experiment/cen_x4/model/model_best.pt (Path to save the model) --date_test Set5
```


## Result

The BI/BD/DN result in the paper
Please click here to download more visualization results [result](https://drive.google.com/drive/folders/1FnKew6XgPcoQawIG9r95vqQAV9-ghJQ1?usp=sharing). 

## The code is shared via download for now
You can download the code by clicking  [here](https://drive.google.com/drive/folders/11GY1ycIF4q_jlWdF6YSvX-9QRCD8XK8j?usp=sharing).
