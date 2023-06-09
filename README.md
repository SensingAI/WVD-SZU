# WVD-SZU (ICME2023)：Need a dog seeing eye? A Walk Viewpoint Dataset for Freespace Detection in Unstructured Environments
<div align=center><img src="https://www.szu.edu.cn/images/logo_03.png" width="325" height="80">  <img src="https://github.com/SensingAI/WVD-SZU/raw/main/images/SensingAi.png" width="125" ></div> 
<div align=center><img src="http://iip.szu.edu.cn/uploads/admin/202010/5f866c5e7eb7e.jpg" width="525" height="95"></div>

Wenbin Zou, Guoguang Hua, Guangxu Chen, Zaiyue He, Guangli Liu, Pengfei Chen, Yuyang Li, Huakun Li, Lei Zheng, Shishun Tian<sup>*</sup> <br>

  1. [Shenzhen University](http://ceie.szu.edu.cn/)  2. [Guangdong KLIIP](http://iip.szu.edu.cn/)   <br>

  [[Website](https: "Coming Soon")] [Paper] [[Github](https://github.com/SensingAI/WVD-SZU/)]


## Updates
* 27/04/2023 `v1.0 release`

## Overview
**Freespace Detection** (FD) is crucial for robust and safe autonomous navigation. However, existing datasets usually concentrate on structure road environments. The FD in unstructured environments, e.g., walk assistance for the visually-impaired, has been rarely investigated. In this paper, We propose a novel dataset called the **Walk Viewpoint Dataset (WVD)**. Different from the previous datasets, we focus on the walk viewpoint, where FD can provide the potential for improving the walking of visually impaired people. The target regions of WVD are annotated with **20 categories** by fine-grained labels, which consist of **3,737** images and depth images. Moreover, we propose a new annotation hierarchy, which allows different degrees of complexity and creates opportunities for new training methods. Finally, our study provides the statistical analysis of label characteristics and baseline analysis, which demonstrates its distinction compared to previous datasets.

<img src="https://github.com/SensingAI/WVD-SZU/raw/main/images/Examples_00.jpg" width="925" >

## Folder Structure
```
WVD-SZU
 |--test.txt
 |--train.txt
 |--trainval.txt
 |--images/   -- directory containing ".png" files from the color camera (realsense).
 |--labels    -- directory containing color image label.
 |--Middle_group 
      |--shenzhen_*_Img.png
      |--gt_label/     --directory contianin color image label with 6 Middle label (SafeLevel-*).
 |--Traver
      |--shenzhen_*_Img.png
      |--gt_label/     --directory contianin color image label with 2 Root label (Traversable or Non-traversable).
```
## Download Link on BaiDu Cloud
Link:https://pan.baidu.com/s/1KsVTrJcD4vilYRi7jVo7Xg

PassWord:akig
:blush:

**Note:** This is a part of dataset. Full data download is coming soon.

## Annotated Data
**Category:**
With the goal of providing data to enhance unstructure environment navigation, we defined the WVD dataset. WVD contains diverse categories that can easily be spotted from a walk viewpoint, e.g., pedestrian-area and bike-lane. Visually impaired people who are trailed tend to struggle with walking straight, so they tend to touch the Blind to follow over a straightFor mobile robots, the definitions of safe regions are different, e.g., the sidewalk is higher than the bike-lane, and the bike-lane is higher than the road in safety factors. Overall, 20 categories are present in the data.

**Images Statics:**

<img src="https://github.com/SensingAI/WVD-SZU/raw/main/images/static2_00.jpg" width="855" >

**Note:**

(1) Two inset to better visualize some of categories.

(2) If you can't access the file, please email every author with the title "WVD-SZU Aceess Request..."

## Benchmarks
**The MIoU Score of Models at Three Levels**
Methods | Root | Middle | Category
--- | --- | --- | --- 
DeeplabV3+ | 96.41 % | 70.56 % | 43.33 %
RFNet | 97.61 % | 74.69 % | 60.98 %
PPLiteSeg | 97.35 % | 78.64 % | 61.61 %

**Per Categories on The Testing Split**
Methods | Sidewalk | Ped.A | Blind | Cur.C | Lawn | Bik.L | Crosswalk | Cat.B | Manhole | Gra.W | Dir.W | Mul.W | Puddle | Asp.R | Spe.B | Cem.R | Parking | Curb | Pohthole | Stair
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- 
DeeplabV3+ | 84 | 70 | 67 | 27 | 75 | 80 | 86 | 42 | 43 | 0 | 0 | 4 | 0 | 78 | 0 | 8 | 0 | 56 | 18 | 73
RFNet | 88 | 76 | 76 | 39 | 82 | 86 | 95 | 70 | 59 | 5 | 1 | 43 | 7 | 83 | 62 | 71 | 89 | 68 | 27 | 90
PPLiteSeg | 92 | 84 | 82 | 39 | 85 | 82 | 83 | 74 | 45 | 1 | 1 | 58 | 0 | 79 | 46 | 44 | 53 | 61 | 23 | 85

<img src="https://github.com/SensingAI/WVD-SZU/raw/main/images/Results_00.jpg" width="925" >

## Citation
```
@misc{zou2023wvd,
      title={Need a dog for seeing eye? A Walk Viewpoint Dataset for Freespace Detection in Unstructured Environments}, 
      author={Wenbin Zou and Guoguang Hua and Guangxu Chen and Zaiyue He and Guangli Liu and Pengfei Chen and Yuyang Li and Huakun Li and Lei Zheng and Shishun Tian},
      year={2023},
      eprint={},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

## Collaborator
<img src="https://github.com/SensingAI/WVD-SZU/raw/main/images/SensingAi.png" width="125" >

## License
All datasets and code on this page are copyright by us and published under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 License.








