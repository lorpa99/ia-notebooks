# 01 – k-Nearest Neighbors from scratch with NumPy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lorpa99/ia-notebooks/blob/main/01-knn-from-scratch-numpy/01-knn-from-scratch-numpy.ipynb)

**Level 1 – From scratch.** No machine learning library is used to build the model: only NumPy. scikit-learn provides the datasets and the final comparison.

## Goal

Go from Python lists to NumPy arrays, then use those arrays to build, evaluate and understand a k-Nearest Neighbors classifier, ending with a real task: recognizing handwritten digits.

The notebook has two parts.

**Part A – NumPy.** Why lists are not enough (time and memory measured, not asserted); shape, dtype, views vs copies; vectorized operations and boolean masks; matrices and `axis`; broadcasting, including the three-dimensional case; `argsort`, fancy indexing and `np.unique`. Every tool is introduced because it is needed in Part B.

**Part B – kNN.** The algorithm stated and worked out by hand on nine points; a vectorized implementation (`distances_from`, `majority_vote`, `knn_predict_one`, then a `KNN` class with a scikit-learn-style `fit`/`predict` interface built on an all-pairs distance matrix); training/validation/test split written from scratch; the overfitting/underfitting curve as k varies and the decision regions; why feature scaling matters and why mean and standard deviation are computed on the training set only (data leakage); handwritten digits with 98.9% test accuracy, with the first misclassified digit explained by showing the neighbors that voted; comparison with `KNeighborsClassifier(algorithm="brute")` (identical predictions) and the matrix-product identity that makes the library 70× faster; the curse of dimensionality measured.

Every function of the algorithm is followed by a cell of `assert` checks on small hand-computed cases.

## What it shows

- Vectorization as a habit: each step is written first with a loop, then without, and the two are compared for speed and results.
- Honest evaluation: three data portions, k chosen on the validation set, test set opened once at the end.
- A from-scratch model that matches scikit-learn's predictions exactly on a real dataset.

## Sources

- A. Géron, *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow*: the `tools_numpy` notebook and chapter 3 (classification).
- A. Ng, *Machine Learning Specialization* (DeepLearning.AI): labs on vectorization, broadcasting and train/cross-validation/test splits.
- E. Fix, J. Hodges (1951), *Discriminatory Analysis. Nonparametric Discrimination: Consistency Properties*; T. Cover, P. Hart (1967), *Nearest Neighbor Pattern Classification*.
- K. Beyer et al. (1999), *When Is "Nearest Neighbor" Meaningful?*
- scikit-learn: `euclidean_distances`; datasets `make_moons` and `load_digits` (UCI Optical Recognition of Handwritten Digits, Alpaydin & Kaynak, 1998).

## How to run

On Google Colab: click the badge above, then *Runtime → Run all*. Everything needed is preinstalled.

Locally:

```bash
pip install -r requirements.txt
jupyter notebook 01-knn-from-scratch-numpy.ipynb
```

The notebook runs in well under a minute; the slowest cell is the nested-loop kNN used as a baseline for the timing comparison. Results are reproducible (fixed seeds); timings depend on the machine.
