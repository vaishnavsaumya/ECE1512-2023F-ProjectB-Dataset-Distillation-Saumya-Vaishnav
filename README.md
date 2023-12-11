# Towards Lossless Dataset Distillation via Difficulty-Aligned Trajectory Matching

## [Project Page](https://gzyaftermath.github.io/DATM/) | [Paper](https://arxiv.org/abs/2310.05773) | [Distilled Datasets](https://drive.google.com/drive/folders/1kZlYgiVrmFEz0OUyxnww3II7FBPQe7W0)


The code in this repository is taken from the official repository at:
https://github.com/GzyAftermath/DATM

The code files were modified to load the MNIST dataset and get the distilled dataset with 10 images per class using training parameters similar to those in task 1.

The huge ".pt" model files have not been pushed to this repository due to size limits.
<!-- To achieve lossless dataset distillation, an intuitive idea is to increase the size of the synthetic dataset.
However, previous dataset distillation methods tend to perform worse than random selection as IPC (i.e., data keep ratio) increases.

To address this issue, we find the difficulty of the generated patterns should be aligned with the size of the synthetic dataset
(avoid generating patterns that are too easy or too difficult).

By doing so, our method remains effective in high IPC cases and achieves lossless dataset distillation for the very first time.
![image](figures/comparison.png)
What do easy patterns and hard patterns look like?

![image](figures/visualization.png)


![image](figures/visualization_ipc.png)

## Getting Started
1. Create environment as follows
```
conda env create -f environment.yaml
conda activate distillation
```
2. Generate expert trajectories
```
cd buffer
python buffer_FTD.py --dataset=CIFAR10 --model=ConvNet --train_epochs=100 --num_experts=100 --zca --buffer_path=../buffer_storage/ --data_path=../dataset/ --rho_max=0.01 --rho_min=0.01 --alpha=0.3 --lr_teacher=0.01 --mom=0. --batch_train=256
```
3. Perform the distillation
```
cd distill
python DATM.py --cfg ../configs/xxxx.yaml
```
## Evaluation
We provide a simple script for evaluating the distilled datasets.
```
cd distill
python evaluation.py --lr_dir=path_to_lr --data_dir=path_to_images --label_dir=path_to_labels --zca
```
## Acknowledgement
Our code is built upon [MTT](https://github.com/GeorgeCazenavette/mtt-distillation) and [FTD](https://github.com/AngusDujw/FTD-distillation).
## Citation
If you find our code useful for your research, please cite our paper.
```
@misc{guo2023lossless,
      title={Towards Lossless Dataset Distillation via Difficulty-Aligned Trajectory Matching}, 
      author={Ziyao Guo and Kai Wang and George Cazenavette and Hui Li and Kaipeng Zhang and Yang You},
      year={2023},
      eprint={2310.05773},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
``` -->
