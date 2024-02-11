# Model Compression with Separation Index

This repository contains an algorithm for model compression using the Separation Index (SI) as described in the paper "Evaluation of dataflow through layers of deep neural networks in classification and regression problems" by Kalhor, Ahmad, et al. [arXiv:1906.05156](https://arxiv.org/abs/1906.05156) (2019).

## Algorithm Steps

The compression algorithm is outlined as follows:

1. Calculate the SI for each layer of the feature extraction part of the network and remove the layers that do not significantly increase this index.
2. Then, in the final layer of the feature extraction part, select the best features of the obtained model using the SI index. In other words, find the features that do not significantly increase the SI metric and remove them.
3. Redesign the classification section based on the dimensions of the last layer in the feature extraction part of the final model.
4. Train the obtained model only for the classification section.

## Usage

To use this algorithm, follow these steps:

1. Clone the repository.
2. Ensure you have the necessary dependencies installed.
3. Use the provided algorithm to compress your model based on the Separation Index method.

Feel free to contribute to this repository by improving the algorithm or providing additional features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
