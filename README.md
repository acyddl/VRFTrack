# 🚀 VRFTrack: Visual Reinforcement Fine-Tuning of Large Vision-Language Models for Referring Multi-Object Tracking

**VRFTrack** is a novel Referring Multi-Object Tracking (RMOT) framework that integrates visually reinforced Large Vision-Language Models (LVLMs) with Segment Anything Model 2 (SAM2) for robust language-conditioned tracking. It exploits the reasoning capability of LVLMs for referring localization and uses SAM2-based temporal propagation with Dynamic Memory-guided Association (DMA) to maintain temporally consistent object identities.

<p align="center">
  <img src="./assets/framework.png" width="900"/>
</p>

## 🔧 Features

* **Visual Reinforcement Fine-Tuning (VRFT):** Enhances LVLM-based referring localization through Group Relative Policy Optimization (GRPO) with verifiable rewards.
* **Positive-Negative Sample Design:** Improves target-presence reasoning by jointly optimizing referred-object localization and no-object rejection.
* **Dynamic Memory-guided Association (DMA):** Maintains object-level memories for referred tracklets and integrates LVLM detections with SAM2-assisted historical states.
* **Open-world Referring Tracking:** Supports natural language-conditioned tracking across diverse visual domains and linguistic expressions.

## 📢 Code Availability

The source code, trained models, evaluation scripts, and detailed instructions will be made publicly available upon acceptance.

## 🏆 Main Results

### Refer-KITTI

|   Method  | Backbone |    HOTA   |    DetA   |    AssA   |   DetRe   |   DetPr   |   AssRe   |   AssPr   |    LocA   |
| :-------: | :------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| VRFTrack† | Qwen3-VL |   41.27   |   28.09   |   60.71   |   48.79   |   39.28   |   67.52   |   85.98   |   90.78   |
| VRFTrack⋆ | Qwen3-VL | **52.92** | **42.08** | **67.03** | **59.83** | **65.38** | **68.58** | **88.56** | **91.96** |

### Refer-KITTI-V2

|   Method  | Backbone |    HOTA   |    DetA   |    AssA   |   DetRe   |   DetPr   |   AssRe   |   AssPr   |    LocA   |
| :-------: | :------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| VRFTrack† | Qwen3-VL |   36.17   |   22.46   |   58.54   |   53.97   |   27.19   |   69.68   |   77.19   |   86.63   |
| VRFTrack⋆ | Qwen3-VL | **41.26** | **27.39** | **62.78** | **57.83** | **33.44** | **76.26** | **85.27** | **87.97** |

`†` denotes zero-shot results.
`⋆` denotes results obtained using the LVLM after visual reinforcement fine-tuning.

## 📜 License

![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-green.svg)

The code will be released for academic research purposes upon acceptance. Please check the licenses of the corresponding datasets, Qwen3-VL, and SAM2 before use.

## 🙏 Acknowledgement

We sincerely thank the following projects for their excellent open-source resources:

* [Qwen-VL](https://github.com/QwenLM/Qwen-VL)
* [SAM2](https://github.com/facebookresearch/sam2)
* [TransRMOT](https://github.com/wudongming97/RMOT)
* [TempRMOT](https://github.com/zyn213/TempRMOT)
* [TrackEval](https://github.com/JonathonLuiten/TrackEval)

## 📫 Contact

If you have any questions, feel free to open an issue or contact us.
