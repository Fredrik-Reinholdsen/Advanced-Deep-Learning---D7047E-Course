## Advanced-Deep-Learning---D7047E-Course

# Exercise 1: Setting up and using DeepDIVA
1. Download and prepare the CIFAR10 dataset, command: python util/data/get_a_dataset.py --dataset CIFAR-10 --output-folder toy_datasets

2. Run Image Classification with seed 42, command: python template/RunMe.py --dataset-folder toy_datasets/CIFAR10 --seed42 --ignoregit --no-cuda. Resulting Accuracy: 23.11 %

3. Run previous exercise with Adam optimizer, command: python template/RunMe.py --dataset-folder toy_datasets/CIFAR10 --seed42 --ignoregit --no-cuda --optimizer-name Adam. Resulting Accuracy: 60.45 %

4. Run previous exercise with Adam optimizer, command: python template/RunMe.py --dataset-folder toy_datasets/CIFAR10 --seed42 --ignoregit --no-cuda --optimizer-name Adam --model-name CNN_basic_copy. Resulting Accuracy: 52.94 %
