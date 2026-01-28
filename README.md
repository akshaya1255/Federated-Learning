# Federated-Learning
Privacy-preserving Image Classification using Flower and PyTorch
This project implements a Federated Learning (FL) framework to train a deep learning model on the CIFAR-10 dataset without centralizing user data. By utilizing the Flower (flwr) framework and PyTorch, I simulated a distributed environment where data remains on local "edge nodes," directly addressing privacy and security concerns in modern AI.

Key Features
Distributed Training: Orchestrated 3 virtual clients using Ray to simulate decentralized data silos on a single machine.

Non-IID Data Handling: Artificially partitioned the dataset by labels to simulate real-world "data skew," where different nodes possess different data distributions.

Optimization with FedProx: Implemented the FedProx strategy to maintain global model stability and prevent weight divergence caused by non-uniform local data.

Performance Monitoring: Tracked global accuracy and loss across communication rounds to ensure convergence in a decentralized setting.

Results
Under a highly biased (Non-IID) configuration, the global model successfully aggregated knowledge from all nodes:

Starting Accuracy: ~41.1%

Final Accuracy (Round 5): ~57.0%

Convergence: The model demonstrated a consistent downward trend in loss, proving that the FedProx strategy effectively balanced local updates with the global goal.

Tech Stack
Language: Python

Frameworks: Flower (flwr), PyTorch

Engine: Ray (Simulation Engine)

Visualization: Matplotlib
