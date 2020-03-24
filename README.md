# Nearest Neighbor Image Classification of packs on shop shelf
In a nutshell:
1. Classify Product shots from 10 classes - 2744 in total ([dataset source](https://github.com/gulvarol/grocerydataset))
- [Part-1](https://github.com/gulvarol/grocerydataset/releases/download/1.0/GroceryDataset_part1.tar.gz)
- [Part-2](https://github.com/gulvarol/grocerydataset/releases/download/1.0/GroceryDataset_part2.tar.gz)
2. Used **`50% (1374) for training, 50% (1370) for validating`**. Doesn't need many images for training.
3. Used predictor vector of [tensorflow_hub classifier](https://www.tensorflow.org/tutorials/images/transfer_learning_with_hub) as **`1001-dimensional feature vector`** to represent each image
4. **`5-stage feature transformation`** on raw numbers to compute a **`novel similarity metric`** (Bonding Quotient) between images
5. The transformation involved computing dataset distribution specific 5-point scale and weights
6. **`Top-1 Validation accuracy: 99.6 (1364/1370 correct).`**
7. **`Top-5 Validation Accuracy: 99.9 (1368/1370 correct).`**
8. Error analysis indicate blurred images are hard to recognize as it gets mixed up with blurred images of other classes.
9. This also showed that there are instances of image labeling errors. Thorough checking needed of labeling
