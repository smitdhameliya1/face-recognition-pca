# Face Recognition with PCA (Eigenfaces)

A face recognition system built from scratch with Principal Component Analysis. Face images are projected into a low-dimensional "face space" spanned by the eigenfaces, and a test face is identified by its nearest neighbour in that space.

Based on Turk & Pentland, [*Eigenfaces for Recognition*](https://sites.cs.ucsb.edu/~mturk/Papers/mturk-CVPR91.pdf).

## What it does
- Loads the AT&T face dataset and splits it 90/10 into train/test sets
- Implements PCA from scratch (mean-centering, covariance, eigen-decomposition)
- Visualises the mean face and the top eigenfaces
- Reconstructs faces using 5 to 500 principal components
- Classifies test faces by Euclidean distance in face space
- Plots accuracy, MSE and log-MSE against the number of components

## Dataset
`ATnT/` holds the [AT&T face dataset](https://git-disl.github.io/GTDLBench/datasets/att_face_dataset/): 40 subjects (`s1` … `s40`) with 10 grayscale 92×112 images each.

## Running
```bash
pip install -r requirements.txt
jupyter notebook face_recognition.ipynb
```
Run all cells from the repository root so that `ATnT/` resolves.
