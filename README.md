# Soda Challenge: Saudi Organic Dates Classification Challenge
> **4th place** Kaggle SODA Challenge (private score: 0.87428)

A image classification project to identify 13 varieties of Arabic date fruits, developed as part of the Saudi Organic Dates Classification (SODA) Challenge on Kaggle.

---
## Results
| Metric| Score | 
|----------|---------|
| Public leaderboard | 0.910| 
| Private leaderboard | 0.874 |
| Public ranking | 2nd place | 
| Private ranking | 4th place |

## Repository Structure
```
|-- SODA Report.docx    # Project report with full methodology and results
|-- soda-competition-notebook (1).ipynb    # Full Training and inference pipeline
|-- README.md
```

## Strategy Summary
- Tried YOLO-based classification first (best score: 0.794)
- Switched to dedicated image classifiers 
- Tested EfficientNet-B3 and ConvNeXt Small individually
- Final approach: ensemble of 4 models trained with different seeds and architectures
- Applied Test Time Augmentation (TTA) with 16 augments at inference

## Score Progression
| Approach | Competition Score (Public) |
|----------|-----------------|
| YOLO baseline |  0.794 |
| EfficientNet-B3 single model |  0.870 |
| ConvNeXt Small single model |  0.873 |
| 2-model ensemble | 0.889 |
| 3-model ensemble |0.899 |
| 4-model ensemble (final) | 0.910 |

## Dataset 
> The dataset is available on Kaggle: [SODA Challenge](https://www.kaggle.com/competitions/soda-challenge/data)
- 1,829 training images evenly distributed among all 13 classes
- 784 test images

---

## Notes
- The notebook is designed to run on Kaggle with GPU enabled
- AI assitance was used during development of the training pipeline
- The difference between private and public scores is simply that the public is the 50% of the data we were allowed to use during the competition, while private is the remaining 50% of the data used for evaluation at the end of the competition.
- For further information read the SODA Report.docx




