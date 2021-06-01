# EagerMOT: 3D Multi-Object Tracking via Sensor Fusion
## Read our ICRA 2021 paper [here](https://arxiv.org/abs/2104.14682).

### Check out the [3 minute video](https://youtu.be/RX4xDQ0YXxE) for the quick intro or [the full presentation video](https://youtu.be/k8pKpvbenoM) for more details.

This repo contains code for our ICRA 2021 paper. Benchmark results can be fully reproduced with minimal work, only need to edit data location variables. If desired, our ablation results can also be reproduced by need more adjustments. 
An earlier version of this paper has also appeared as a short [4-page paper](https://motchallenge.net/workshops/bmtt2020/papers/EagerMOT.pdf) at the [CVPR 2020 MOTChallenge Workshop](https://motchallenge.net/workshops/bmtt2020/).

---

Improve your online 3D multi-object tracking performance by using 2D detections to support tracking when 3D association fails. The method adds minimal overhead, does not rely on dedicated hardware on any particular sensor setup. The current Python implementation run at **90 FPS** on KITTI data and can definitely be optimized for actual deployment.

The framework is flexible to work with any 3D/2D detection sources (we used only off-the-shelf models) and can be extended to other tracking-related tasks, e.g. MOTS.

![Visual](figures/test_visualization.gif)


## Abstract
Multi-object tracking (MOT) enables mobile robots to perform well-informed motion planning and navigation by localizing surrounding objects in 3D space and time. Existing methods rely on depth sensors (e.g., LiDAR) to detect and track targets in 3D space, but only up to a limited sensing range due to the sparsity of the signal. On the other hand, cameras provide a dense and rich visual signal that helps to localize even distant objects, but only in the image domain. In this paper, we propose EagerMOT, a simple tracking formulation that eagerly integrates all available object observations from both sensor modalities to obtain a well-informed interpretation of the scene dynamics. Using images, we can identify distant incoming objects, while depth estimates allow for precise trajectory localization as soon as objects are within the depth-sensing range. With EagerMOT, we achieve state-of-the-art results across several MOT tasks on the KITTI and NuScenes datasets.

## Benchmark results

Our current standings on **KITTI** for 2D MOT on [the official leaderboard](http://www.cvlibs.net/datasets/kitti/eval_tracking.php). For 2D MOTS, see [this page](http://www.cvlibs.net/datasets/kitti/eval_mots_detail.php?result=714550ab34eca8356b2163f8c18c246ec18fbf0b). 
Our current standings on **NuScenes** for 3D MOT on [the official leaderboard](https://www.nuscenes.org/tracking?externalData=all&mapData=all&modalities=Any).

## Please cite our paper if you find the code useful
```
@inproceedings{Kim21ICRA,
  title     = {EagerMOT: 3D Multi-Object Tracking via Sensor Fusion},
  author    = {Kim, Aleksandr, O\v{s}ep, Aljo\v{s}a and Leal-Taix{'e}, Laura},
  booktitle = {IEEE International Conference on Robotics and Automation (ICRA)},
  year      = {2021}
}
```


<!-- ##### 
| Method | sAMOTA | AMOTA | AMOTP | Single threshold: | MOTA |Recall | Precision | IDs | 
| :--- | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| AB3DMOT | 0.9143 | 0.4400 | 0.8461 |  | 0.8279 | 0.9198 | 0.9357 | 2 |
| Ours | 0.9240 | 0.4662 | 0.8865 |  | 0.8205 | 0.9338 | 0.9183 | 2 |
 -->












