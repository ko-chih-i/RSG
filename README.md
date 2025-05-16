## RSG: A Simple but Effective Module for Learning Imbalanced Datasets (CVPR 2021)

A Pytorch implementation of our CVPR 2021 paper "RSG: A Simple but Effective Module for Learning Imbalanced Datasets". RSG (Rare-class Sample Generator) is a flexible module that can generate rare-class samples during training and can be combined with any backbone network. RSG is only used in the training phase, so it will not bring additional burdens to the backbone network in the testing phase.


How to train
-----------------
 To reimplement the result of ResNet-32 on long-tailed CIFAR-10 ($\rho$ = 100) with RSG and LDAM-DRW:

   ```
   %env CUDA_VISIBLE_DEVICES=0,1
!python /content/RSG/Imbalanced_Classification/cifar_train.py --imb_type exp --imb_factor 0.01 --loss_type LDAM --train_rule DRW --seed 42
   ```

Citation
-----------------

  ```
  @inproceedings{Jianfeng2021RSG,
    title = {RSG: A Simple but Effective Module for Learning Imbalanced Datasets},
    author = {Jianfeng Wang and Thomas Lukasiewicz and Xiaolin Hu and Jianfei Cai and Zhenghua Xu},
    booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
    year={2021}
  }
  ```
