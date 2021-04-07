# Awesome-Temporal-Sentence-Grounding-in-Videos[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<p align="center">
  <img width="250" src="https://camo.githubusercontent.com/1131548cf666e1150ebd2a52f44776d539f06324/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f6d61737465722f6d656469612f6c6f676f2e737667" "Awesome!">
</p>

A curated list of grounding natural language in video also referred as Single Video Moment Retrieval (SVMR).

## Task definition:

- Given an untrimmed video and a language query, the video grounding task aims to localize a temporal moment in the video that matches the query.

  <div align="center"><img height="200px" src="https://res.cloudinary.com/dzu6x6nqi/image/upload/v1554267644/Awesome%20Language%20Moment%20Retrieval/TALL_-_2.png"></div>

## Standard evaluation metrics:

- Recall@k for IoU=m ([link](https://medium.com/qloo/popular-evaluation-metrics-in-recommender-systems-explained-324ff2fb427d)).
- Mean rank.


## Change Log

- Added details of model acronym for each paper. 
- Added several missing GitHub references.
- Added recent papers (last update data 06/04/2021).
- Added performances in tables. 


## Table of Contents

- [Papers](#papers)
  - [Survey](#survey)
  - [Before](#before) - [2017](#2017) - [2018](#2018) - [2019](#2019) - [2020](#2020)
- [Dataset](#dataset)
- [Benchmark Results](#benchmark-results)
- [Popular Implementations](#popular-implementations)
  - [PyTorch](#pytorch)
  - [TensorFlow](#tensorflow)
  - [Other](#other)

## Dataset
  
|Dataset | Features | Train | Val | Test | Vocab. Size |
|---     | ---      | :---:   | :---: | :---:  | :---:|
|        |          |         | N. videos / N. queries|  | (Unique words) 
| [ActivityNet Captions](http://cs.stanford.edu/people/ranjaykrishna/densevid/) | [C3D](https://drive.google.com/file/d/1HNnP-cAFZlJV3n3ZGTLqWF84VBv4us7M/view?usp=sharing) | 10009 / 37421 | 4917 / 17505 (val1) <br/> 4885 / 17031 (val2)| 5044 / ? | 15406
| [TACoS](http://www.coli.uni-saarland.de/projects/smile/page.php?id=software)  | [C3D](https://drive.google.com/file/d/1Hpc-rJKAfNRxIkR30KLHFoyJbUEzJaK_/view?usp=sharing) |&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 75 / 10146 | &nbsp;&nbsp;&nbsp;&nbsp; 27 / 4589 |&nbsp;&nbsp;&nbsp;&nbsp; 25 / 4083 | 2255
| [DiDeMo](<https://github.com/LisaAnne/LocalizingMoments>)                     | [VGG16](https://drive.google.com/file/d/1ATtF1LEw6ZBrBZF5z93MKQyukbZKg4FX/view?usp=sharing) | &nbsp;8511 / 33005 | 1094 / 4180 | 1037 / 4021 | 7523
| [Charades-STA](<https://allenai.org/plato/charades/>)                         | [VGG16](https://drive.google.com/file/d/1P5qCMOsCdDAgF8ej9HOfgZYv3XqR8koy/view?usp=sharing)<br/>[I3D (LGI)](https://drive.google.com/file/d/13Cl87OYnISc8x5FNf7TEplxX2AAJu9jc/view?usp=sharing)<br/>[I3D (DRN)](https://drive.google.com/file/d/17QXZdHVcNqKSYbPuvjib6XgSkEDJarMy/view?usp=sharing) | &nbsp;5336 / 12404 | 0 / 0 | 1334 / 3720 | 1289


## Papers
Markdown format:

```markdown
* `ID` | `Model Acronym` | `Conference` | [Paper Name](link) | Author 1 et al |  [GitHub](link)
```

## Analysis papers
|ID| Model | Venue | Title | Authors  | Code  |
|---| ---  | --- | --- | --- | --- 
|-  |`--`  | `BMVC 2020` | [Uncovering Hidden Challenges in Query-Based Video Moment Retrieval](https://arxiv.org/pdf/2009.00325.pdf) | Otani et al | 
|-  |`--`  | `ArXiv 2020`  | [A Closer Look at Temporal Sentence Grounding in Videos: Datasets and Metrics](https://arxiv.org/pdf/2101.09028.pdf) | Yuan et al | [GitHub](https://github.com/yytzsy/grounding_changing_distribution)

## Before
|ID| Model | Venue | Title | Authors  | Code  |
|---| --- | --- | --- | --- | --- |
|1|  | `ACL 2013`    | [Grounded Language Learning from Video Described with Sentences](https://www.aclweb.org/anthology/P13-1006/) |  Yu et al
|2|  | `CVPR 2014`   | [Visual Semantic Search: Retrieving Videos via Complex Textual Queries](<https://www.cv-foundation.org/openaccess/content_cvpr_2014/papers/Lin_Visual_Semantic_Search_2014_CVPR_paper.pdf>) |  Lin et al
|3|  | `AAAI 2015`   |  [Jointly Modeling Deep Video and Compositional Text to Bridge Vision and Language in a Unified Framework](https://www.aaai.org/ocs/index.php/AAAI/AAAI15/paper/view/9734) | Xu et al
|4|  |  `IJCAI 2016` | [Unsupervised Alignment of Actions in Video with Text Descriptions](https://pdfs.semanticscholar.org/5893/7d427ff36e1470b18120245148355047e4ea.pdf) |  Song et al
 

## 2017

|ID| Model | Venue | Title | Authors  | Code  |
| --- | --- | --- | --- | --- | --- |
|5| `MCN`   | `ICCV`  | [Localizing Moments in Video with Natural Language](https://arxiv.org/abs/1708.01641)  | Hendricks et al | [GitHub](<https://people.eecs.berkeley.edu/~lisa_anne/didemo.html>)|
|6| `CTRL`  | `ICCV`  | [TALL: Temporal Activity Localization via Language Query](https://arxiv.org/abs/1705.02101)  | Gao et al | [GitHub](<https://github.com/jiyanggao/TALL>)  |
|7| `--`    | `ArXiv` | [Where to Play: Retrieval of Video Segments using Natural-Language Queries](<https://arxiv.org/abs/1707.00251>) | Lee et al | 


## 2018

|ID| Model | Venue | Title | Authors | Code  |
| --- | --- | --- | --- | --- | --- |
|8|`FIFO` | `ECCV`   | [Find and Focus: Retrieve and Localize Video Events with Natural Language Queries](<http://openaccess.thecvf.com/content_ECCV_2018/papers/Dian_SHAO_Find_and_Focus_ECCV_2018_paper.pdf>) | Shao et al | | 
|9|`TMN`  | `ECCV`   | [Temporal Modular Networks for Retrieving Complex Compositional Activities in Videos](<http://svl.stanford.edu/assets/papers/liu2018eccv.pdf>)  | B. Liu et al | |
|10|`TGN`  | `EMNLP`  | [Temporally Grounding Natural Sentence in Video](<https://aclweb.org/anthology/papers/D/D18/D18-1015/>)  | Chen et al | [GitHub](https://github.com/JaywongWang/TGN)
|11|`TEMPO`| `EMNLP`  | [Localizing Moments in Video with Temporal Language](<https://arxiv.org/abs/1809.01337>)                 | Hendricks et al | [GitHub](https://github.com/LisaAnne/TemporalLanguageRelease)
|12|`ACRN` | `SIGIR`  | [Attentive Moment Retrieval in Videos](http://staff.ustc.edu.cn/~hexn/papers/sigir18-video-retrieval.pdf)| Liu et al | [GitHub](https://sigir2018.wixsite.com/acrn)
|13|`MCF`  | `IJCAI`  | [Multi-modal Circulant Fusion for Video-to-Language and Backward](https://pdfs.semanticscholar.org/e2e5/cef45c60c52fb0d0415cca6cbf35beab3873.pdf) | Wu et al | [GitHub](<https://github.com/AmingWu/Multi-modal-Circulant-Fusion/>)
|14|`ROLE` | `ACM MM` | [Cross-modal Moment Localization in Videos](https://liqiangnie.github.io/paper/p843-liu.pdf)             |  Liu et al |  [GitHub](https://acmmm18.wixsite.com/role)
|015|`VAL`  | `PRCM`   | [VAL: Visual-attention action localizer](https://link.springer.com/content/pdf/10.1007%2F978-3-030-00767-6_32.pdf) | Song et al 
|16|`ASST` | `ArXiv`  | [Attentive Sequence to Sequence Translation for Localizing Clips of Interest by Natural Language Descriptions](https://arxiv.org/pdf/1808.08803.pdf) | Ning et al 



## 2019
|ID| Model | Venue | Title | Authors | Code  |
| --- | --- | --- | --- | --- | --- |
|17|`QSPN`| `AAAI` | [Multilevel Language and Vision Integration for Text-to-Clip Retrieval](<https://arxiv.org/abs/1804.05113>)| Xu et al | [GitHub](<https://github.com/VisionLearningGroup/Text-to-Clip_Retrieval>)
|18|`LNet`| `AAAI` | [Localizing Natural Language in Videos ](https://www.aaai.org/ojs/index.php/AAAI/article/view/4827/4700)| Chen et al
|19|`A2C` | `AAAI` | [Read, Watch, and Move: Reinforcement Learning for Temporally Grounding Natural Language Descriptions in Videos](https://arxiv.org/abs/1901.06829)| Dongliang et al | [GitHub](https://github.com/WuJie1010/Temporally-language-grounding)
|20|`ABLR`| `AAAI` | [To Find Where You Talk: Temporal Sentence Localization in Video with Attention Based Location Regression](http://arxiv.org/abs/1804.07014)| Yuan et al | [GitHub](https://github.com/yytzsy/ABLR_GitHub)
|21|`SAP` | `AAAI` | [Semantic Proposal for Activity Localization in Videos via Sentence Query](http://yugangjiang.info/publication/19AAAI-actionlocalization.pdf)| Chen et al
|22|`MAN`| `CVPR` | [MAN: Moment Alignment Network for Natural Language Moment Retrieval via Iterative Graph Adjustment](https://arxiv.org/abs/1812.00087)| Zhang et al | [GitHub](https://github.com/dazhang-cv/MAN)
|23|`TGA`| `CVPR` | [Weakly Supervised Video Moment Retrieval From Text Queries](<https://arxiv.org/abs/1904.03282>)| Mithun et al | [GitHub](https://github.com/niluthpol/weak_supervised_video_moment)
|24|`SMRL`| `CVPR` | [Language-Driven Temporal Activity Localization_ A Semantic Matching Reinforcement Learning Model](<http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Language-Driven_Temporal_Activity_Localization_A_Semantic_Matching_Reinforcement_Learning_Model_CVPR_2019_paper.pdf>)|  Wang et al 
|25|`SCDM`| `NIPS` | [Semantic Conditioned Dynamic Modulation for Temporal Sentence Grounding in Videos](https://arxiv.org/pdf/1910.14303.pdf)| Yuan et al | [GitHub](https://github.com/yytzsy/SCDM)
|26|`WSDEC`| `EMNLP` | [WSLLN: Weakly Supervised Natural Language Localization Networks](https://arxiv.org/abs/1909.00239)| Gao et al 
|27|`DEBUG`| `EMNLP` | [DEBUG: A Dense Bottom-Up Grounding Approach for Natural Language Video Localization](https://www.aclweb.org/anthology/D19-1518.pdf)| Lu et al
|28|`ExCL`| `NAACL` | [ExCL: Extractive Clip Localization Using Natural Language Descriptions](https://arxiv.org/abs/1904.02755)| Ghosh et al
|29|`CMIN`| `SIGIR` | [Cross-Modal Interaction Networks for Query-Based Moment Retrieval in Videos](https://arxiv.org/abs/1906.02497)| Zhang et al |  [GitHub](https://github.com/ikuinen/CMIN_moment_retrieval)
|30|`CMIN`| `IEEE` | [Moment Retrieval via Cross-Modal Interaction Networks With Query Reconstruction](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8962274&tag=1)| Zhang et al | [GitHub](https://github.com/ikuinen/CMIN_moment_retrieval)
|31|`SLTA`| `ICMR` | [Cross-Modal Video Moment Retrieval with Spatial and Language-Temporal Attention](https://dl.acm.org/citation.cfm?id=3325019)| Jiang et al | [GitHub](https://github.com/BonnieHuangxin/SLTA)
|32|`ACL`| `WACV` | [MAC: Mining Activity Concepts for Language-based Temporal Localization](https://arxiv.org/abs/1811.08925)| Ge et al | [GitHub](https://github.com/runzhouge/MAC)
|33|`WSSTG`| `ACL` | [Weakly-Supervised Spatio-Temporally Grounding Natural Sentence in Video](https://www.aclweb.org/anthology/P19-1183.pdf)| Chen et al | [GitHub](https://github.com/zfchenUnique/WSSTG)
|34|`TCMN`| `ACM` | [Exploiting Temporal Relationships in Video Moment Localization with Natural Language](https://arxiv.org/pdf/1908.03846.pdf)| Zhang et al | [GitHub](https://github.com/Sy-Zhang/TCMN-Release)
|35|`CAL`| `ArXiv` | [Temporal Localization of Moments in Video Collections with Natural Language](https://arxiv.org/abs/1907.12763v1)| Escorcia et al| [GitHub](https://github.com/escorciav/moments-retrieval-page)

 

## 2020
|ID| Model | Venue | Title | Authors | Code  |
| ---| --- | --- | --- | --- | --- |
|36|`CBP`    | `AAAI` | [Temporally Grounding Language Queries in Videos by Contextual Boundary-aware Prediction](https://arxiv.org/pdf/1909.05010.pdf) | Wang et al | [GitHub](https://github.com/JaywongWang/CBP)
|37|`TSP-PRL`|	`AAAI` |	[Tree-Structured Policy based Progressive Reinforcement Learning for Temporally Language Grounding in Video](https://arxiv.org/pdf/238.06680.pdf)| Wu et al| [GitHub](https://github.com/WuJie1010/TSP-PRL)
|39|`2DTAN`  | `AAAI` | [Learning 2D Temporal Localization Networks for Moment Localization with Natural Language](https://arxiv.org/abs/1912.03590) | Zhang et al | [GitHub1](https://github.com/microsoft/2D-TAN), [GitHub2](https://github.com/ChenJoya/2dtan)
|40|`SCN`    | `AAAI` | [Weakly-Supervised Video Moment Retrieval via Semantic Completion Network](https://arxiv.org/pdf/1911.08199.pdf) | Lin et al | | 
|41|`GDP`    | `AAAI` | [Rethinking the Bottom-Up Framework for Query-based Video Localization](https://zjuchenlong.github.io/papers/AAAI_2020.pdf) |  Chen et al | 
|42|`DRN`    | `CVPR` | [Dense Regression Network for Video Grounding](http://openaccess.thecvf.com/content_CVPR_2020/papers/Zeng_Dense_Regression_Network_for_Video_Grounding_CVPR_2020_paper.pdf) | Zeng et al | [GitHub](https://github.com/Alvin-Zeng/DRN)
|43|`STGRN`  | `CVPR` | [Where Does It Exist: Spatio-Temporal Video Grounding for Multi-Form Sentences](http://openaccess.thecvf.com/content_CVPR_2020/papers/Zhang_Where_Does_It_Exist_Spatio-Temporal_Video_Grounding_for_Multi-Form_Sentences_CVPR_2020_paper.pdf) | Zhang et al | [GitHub](https://github.com/Guaranteer/VidSTG-Dataset)
|44|`LGI`    | `CVPR` | [Local-Global Video-Text Interactions for Temporal Grounding](http://openaccess.thecvf.com/content_CVPR_2020/papers/Mun_Local-Global_Video-Text_Interactions_for_Temporal_Grounding_CVPR_2020_paper.pdf) |  Mun et al | [GitHub](https://github.com/JonghwanMun/LGI4temporalgrounding)
|45|`VLANet` | `ECCV` | [VLANet: Video-Language Alignment Network for Weakly-Supervised Video Moment Retrieval](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123730154.pdf) | Ma et al | 
|46|`HVTG`   | `ECCV` | [Hierarchical Visual-Textual Graph for Temporal Activity Localization via Language](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123650596.pdf) | Chen et al | [GitHub](https://github.com/forwchen/HVTG)
|47|`PMI`    | `ECCV` | [Learning Modality Interaction for Temporal Sentence Localization and Event Captioning in Videos](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123490324.pdf) | Chen et al | 
|48|`TripNet`| `BMVC` | [Tripping through time Efficient Localization of Activities in Videos](https://arxiv.org/pdf/1904.09936.pdf) | Hahn et al | 
|50|`VSLNet` | `ACL`  | [Span-based Localizing Network for Natural Language Video Localization](https://arxiv.org/pdf/2004.13931.pdf) | Zhang et al  | [GitHub](https://github.com/IsaacChanghau/VSLNet)
|51|`TMLGA`  | `WACV` | [Proposal-free Temporal Moment Localization of a Natural-Language Query in Video using Guided Attention](http://openaccess.thecvf.com/content_WACV_2020/papers/Rodriguez_Proposal-free_Temporal_Moment_Localization_of_a_Natural-Language_Query_in_Video_WACV_2020_paper.pdf) |  Rodriguez-Opazo et al| [GitHub](https://github.com/crodriguezo/TMLGA)
|52|`--`     | `NIPS` | [Counterfactual Contrastive Learning for Weakly-Supervised Vision-Language Grounding](https://papers.nips.cc/paper/2020/file/d27b95cac4c27feb850aaa4070cc4675-Paper.pdf) |  Zhang et al | 
|53|`RTBPN`  | `ACM`  | [Regularized Two-Branch Proposal Networks for Weakly-Supervised Moment Retrieval in Videos](https://dl.acm.org/doi/pdf/10.1145/3394171.3413967) |  Zhang et al | 
|54|`STRONG` | `ACM`  | [STRONG: Spatio-Temporal Reinforcement Learning for Cross-Modal Video Moment Localization](http://data-science.ustc.edu.cn/_upload/article/files/c4/4f/10f4da284171a6275429698edccf/16741411-8b8b-405a-90a8-5c4baac1c620.pdf) | Cao et al | 
|55|`--`     | `ACM`  | [Adversarial Video Moment Retrieval by Jointly Modeling Ranking and Localization](https://dl.acm.org/doi/pdf/10.1145/3394171.3413841) | Cao et al | 
|56|`DPIN`   | `ACM`  | [Dual Path Interaction Network for Video Moment Localization](https://dl.acm.org/doi/abs/10.1145/3394171.3413975) | Wang et al | 
|57|`STVG`   | `ACM`  | [Weakly-Supervised Video Object Grounding by Exploring Spatio-Temporal Contexts](https://dl.acm.org/doi/abs/10.1145/3394171.3413610) | Yang et al | 
|58|`FIAN`   | `ACM`  | [Fine-grained Iterative Attention Network for Temporal Language Localization in Videos](https://dl.acm.org/doi/abs/10.1145/3394171.3414053) | Qu et al | 
|59|`CSMGAN` | `ACM`  | [Jointly Cross- and Self-Modal Graph Attention Network for Query-Based Moment Localization](https://dl.acm.org/doi/abs/10.1145/3394171.3414026) | Liu et all|  [GitHub](https://github.com/liudaizong/CSMGAN)
|60|`--`      | `DAVU`  | [Cross-Modality Video Segment Retrieval with Ensemble Learning](https://link.springer.com/chapter/10.1007/978-3-030-30671-7_5#Sec12) | Yu et al | 
|61|`SMRN`    | `ISNN`  | [Semantic Modulation Based Residual Network for Temporal Language Queries Grounding in Video](https://link.springer.com/chapter/10.1007/978-3-030-64221-1_11) |Chen et al | 
|62|`--`    | `Journal`  | [Cross-modal video moment retrieval based on visual-textual relationship alignment](https://engine.scichina.com/publisher/scp/journal/SSI/50/6/10.1360/SSI-2019-0292?slug=fulltext) |  Chen et al| 
|63|``    | `ArXiv`  | [Video Moment Retrieval via Natural Language Queries](https://arxiv.org/abs/2009.02406) | Yu et al | 
|65|`WSTG`| `ArXiv`  | [Look Closer to Ground Better: Weakly-Supervised Temporal Grounding of Sentence in Video](https://arxiv.org/pdf/266.09308.pdf) | Chen et al | 
|67|`MARN`| `ArXiv`  | [Weakly-Supervised Multi-Level Attentional Reconstruction Network for Grounding Textual Queries in Videos](https://arxiv.org/pdf/2003.07048.pdf) | Song et al | 
|68|`LGN` | `ArXiv`  | [Language Guided Networks for Cross-modal Moment Retrieval](https://arxiv.org/pdf/2006.10457.pdf) | Liu et al | 
|69|`ACRM`| `ArXiv`  | [Frame-wise Cross-modal Match for Video Moment Retrieval](https://arxiv.org/abs/2009.10434) | Tang et al | 
|70|`CMA` | `ArXiv`  | [A Simple Yet Effective Method for Video Temporal Grounding with Cross-Modality Attention](https://arxiv.org/pdf/2009.11232.pdf) |  Zhang et al| 
|71|`--`  | `ArXiv`  | [Natural Language Video Localization: A Revisit in Span-based Question Answering Framework](https://arxiv.org/pdf/2102.13558.pdf) | Zhang et al | 
|72|`VLG-Net`| `ArXiv`  | [VLG-Net: Video-Language Graph Matching Network for Video Grounding](https://arxiv.org/pdf/2011.10132.pdf) | Soldan et al | 
 


|``| `` | [Multi-Scale 2D Temporal Adjacent Networks for Moment Localization with Natural Language](https://arxiv.org/pdf/2012.02646.pdf) - Songyang Zhang et al, `TPAMI submission`.



### 2021





## Benchmark Results

#### ActivityNet Captions

|                 | R@1 IoU@0.1 | R@1 IoU@0.3 | R@1 IoU@0.5 | R@1 IoU@0.7 | R@5 IoU@0.1 | R@5 IoU@0.3 | R@5 IoU@0.5 | R@5 IoU@0.7 | Method |
| :---: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :----: |
|       MCN       |    42.80    |    21.37    |    9.58     |      -      |      -      |      -      |      -      |      -      |   PB   |
|      CTRL       |    49.09    |    28.70    |    14.0     |      -      |      -      |      -      |      -      |      -      |   PB   |
|      ACRN       |    50.37    |    31.29    |    16.17    |      -      |      -      |      -      |      -      |      -      |   PB   |
|      QSPN       |      -      |    45.3     |    27.7     |    13.6     |      -      |    75.7     |    59.2     |    38.3     |   PB   |
|       TGN       |    70.06    |    45.51    |    28.47    |      -      |    79.10    |    57.32    |    44.20    |      -      |   PB   |
|      SCDM       |      -      |    54.80    |    36.75    |    19.86    |      -      |    77.29    |    64.99    |    41.53    |   PB   |
|       CBP       |      -      |    54.30    |    35.76    |    17.80    |      -      |    77.63    |    65.89    |    46.20    |   PB   |
|     TripNet     |      -      |    48.42    |    32.19    |    13.93    |      -      |      -      |      -      |      -      |   RL   |
|      ABLR       |    73.30    |    55.67    |    36.79    |      -      |      -      |      -      |      -      |      -      |   RL   |
|      ExCL       |      -      |    63.30    |    43.6     |    24.1     |      -      |      -      |      -      |      -      |   PF   |
|      PFGA       |    75.25    |    51.28    |    33.04    |    19.26    |      -      |      -      |      -      |      -      |   PF   |
| WSDEC-X(Weakly) |    62.7     |    42.0     |    23.3     |      -      |      -      |      -      |      -      |      -      |        |
| WSLLN (Weakly)  |    75.4     |    42.8     |    22.7     |      -      |      -      |      -      |      -      |      -      |        |

#### Charades-STA

|         | R@1 IoU@0.1 | R@1 IoU@0.3 | R@1 IoU@0.5 | R@1 IoU@0.7 | R@5 IoU@0.1 | R@5 IoU@0.3 | R@5 IoU@0.5 | R@5 IoU@0.7 | Method |
| :-----: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :----: |
|  CTRL   |      -      |      -      |    23.63    |    8.89     |      -      |      -      |    58.92    |    29.52    |   PB   |
|  ABLR   |      -      |      -      |    24.36    |    9.01     |      -      |      -      |      -      |      -      |   PB   |
|  SMRL   |      -      |      -      |    24.36    |    11.17    |      -      |      -      |    61.25    |    32.08    |   PB   |
|  ACL-K  |      -      |      -      |    30.48    |    12.20    |      -      |      -      |    64.84    |    35.13    |   PB   |
|   SAP   |      -      |      -      |    27.42    |    13.36    |      -      |      -      |    66.37    |    38.15    |   PB   |
|  QSPN   |      -      |    54.7     |    35.6     |    15.8     |      -      |    95.8     |    79.4     |    45.4     |   PB   |
|   MAN   |      -      |      -      |    46.53    |    22.72    |      -      |      -      |    86.23    |    53.72    |   PB   |
|  SCDM   |      -      |      -      |    54.44    |    33.43    |      -      |      -      |    74.43    |    58.08    |   PB   |
|   CBP   |      -      |      -      |    36.80    |    18.87    |      -      |      -      |    70.94    |    50.19    |   PB   |
| TripNet |      -      |    51.33    |    36.61    |    14.50    |      -      |      -      |      -      |      -      |   RL   |
|  ExCL   |      -      |    65.1     |    44.1     |    23.3     |      -      |      -      |      -      |      -      |   RL   |
|  PFGA   |      -      |    67.53    |    52.02    |    33.74    |      -      |      -      |      -      |      -      |   PF   |

#### DiDeMo

|                | R@1 IoU@0.1 | R@1 IoU@0.3 | R@1 IoU@0.5 | R@1 IoU@0.7 | R@5 IoU@0.1 | R@5 IoU@0.3 | R@5 IoU@0.5 | R@5 IoU@0.7 |
| :--: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: |
|      TMN       |    22.92    |      -      |      -      |      -      |    76.08    |      -      |      -      |      -      |
|      MCN       |    28.10    |      -      |      -      |      -      |    78.21    |      -      |      -      |      -      |
|      TGN       |    28.23    |      -      |      -      |      -      |    79.26    |      -      |      -      |      -      |
|      MAN       |    27.02    |      -      |      -      |      -      |    81.70    |      -      |      -      |      -      |
| WSLLN (Weakly) |    19.4     |      -      |      -      |      -      |    54.4     |      -      |      -      |      -      |

#### TACoS

|         | R@1 IoU@0.1 | R@1 IoU@0.3 | R@1 IoU@0.5 | R@1 IoU@0.7 | R@5 IoU@0.1 | R@5 IoU@0.3 | R@5 IoU@0.5 | R@5 IoU@0.7 | Method |
| :-----: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :----: |
|   MCN   |    2.62     |    1.64     |    1.25     |      -      |    2.88     |    1.82     |    1.01     |      -      |   PB   |
|  CTRL   |    24.32    |    18.32    |    13.30    |      -      |    48.73    |    36.69    |    25.42    |      -      |   PB   |
|   TGN   |    41.87    |    21.77    |    18.90    |      -      |    53.40    |    39.06    |    31.02    |      -      |   PB   |
|  ACRN   |    24.22    |    19.52    |    14.62    |      -      |    47.42    |    34.97    |    24.88    |      -      |   PB   |
|  ACL-K  |    31.64    |    24.17    |    20.01    |      -      |    57.85    |    42.15    |    30.66    |      -      |   PB   |
|  SCDM   |      -      |    26.11    |    21.17    |      -      |      -      |    40.16    |    32.18    |      -      |   PB   |
|   CBP   |      -      |    27.31    |    24.79    |    19.10    |      -      |    43.64    |    37.40    |    25.59    |   PB   |
| TripNet |      -      |    23.95    |    19.17    |    9.52     |      -      |      -      |      -      |      -      |   RL   |
|  SMRL   |    26.51    |    20.25    |    15.95    |      -      |    50.01    |    38.47    |    27.84    |      -      |   RL   |
|  ABLR   |    34.7     |    19.5     |     9.4     |      -      |      -      |      -      |      -      |      -      |   RL   |
|  ExCL   |      -      |    45.5     |    28.0     |    14.6     |      -      |      -      |      -      |      -      |   PF   |

## Popular Implementations

### PyTorch

- [ikuinen/CMIN_moment_retrieval](https://github.com/ikuinen/CMIN_moment_retrieval)

### TensorFlow

- [jiyanggao/TALL](<https://github.com/jiyanggao/TALL>)
- [runzhouge/MAC](https://github.com/runzhouge/MAC)
- [BonnieHuangxin/SLTA](https://github.com/BonnieHuangxin/SLTA)
- [yytzsy/ABLR_code](https://github.com/yytzsy/ABLR_code)
- [yytzsy/SCDM](https://github.com/yytzsy/SCDM)
- [JaywongWang/TGN](https://github.com/JaywongWang/TGN)
- [JaywongWang/CBP](https://github.com/JaywongWang/CBP)

### Others

- None.

## Licenses

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [muketong](https://github.com/iworldtong) all copyright and related or neighboring rights to this work.

