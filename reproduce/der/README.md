# DER

## Abstract

We address the problem of class incremental learning, which is a core step towards achieving adaptive vision intelligence. In particular, we consider the task setting of incremental learning with limited memory and aim to achieve a better stability-plasticity trade-off. To this end, we propose a novel two-stage learning approach that utilizes a dynamically expandable representation for more effective incremental concept modeling. Specifically, at each incremental step, we freeze the previously learned representation and augment it with additional feature dimensions from a new learnable feature extractor. Moreover, we dynamically expand the representation according to the complexity of novel concepts by introducing a channel-level mask-based pruning strategy. This enables us to integrate new visual concepts with retaining learned knowledge. Furthermore, we introduce an auxiliary loss to encourage the model to learn diverse and discriminate features for novel concepts. We conduct extensive experiments on the three class incremental learning benchmarks and our method consistently outperforms other methods with a large margin.


## Citation

```
@inproceedings{DBLP:conf/cvpr/YanX021,
  author       = {Shipeng Yan and
                  Jiangwei Xie and
                  Xuming He},
  title        = {{DER:} Dynamically Expandable Representation for Class Incremental
                  Learning},
  booktitle    = {{IEEE} Conference on Computer Vision and Pattern Recognition, {CVPR}
                  2021, virtual, June 19-25, 2021},
  pages        = {3014--3023},
  publisher    = {Computer Vision Foundation / {IEEE}},
  year         = {2021},
  url          = {https://openaccess.thecvf.com/content/CVPR2021/html/Yan\_DER\_Dynamically\_Expandable\_Representation\_for\_Class\_Incremental\_Learning\_CVPR\_2021\_paper.html},
  doi          = {10.1109/CVPR46437.2021.00303},
  timestamp    = {Mon, 18 Jul 2022 16:47:40 +0200},
  biburl       = {https://dblp.org/rec/conf/cvpr/YanX021.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
}
```

## How to Reproduce DER

- **Step1: 修改`run_trainer.py`中`Config`参数为`./config/der.yaml`**

- **Step2: python run_trainer.py**:

## Results and models

| Method | Backbone | Pretrained |  Dataset  | Epochs |    Split    | Precision |
| :----: | :------: | :--------: | :-------: | :----: | :---------: | :-------: |
|  DER   | Resnet18 |   False    | CIFAR-100 |  170   | Base0 Inc10 |  64.90%   |

