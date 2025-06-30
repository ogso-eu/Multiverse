# 🌌 Multiverse: A Generative Modeling Framework

<div align="center">
<img src="assets/multiverse-logo.png" height="40px" align="top"/> 
<h1>Multiverse</h1>
</div>

<div align="center">
[![Paper](https://img.shields.io/badge/Paper-📄-blue)](https://arxiv.org/abs/2506.09991) | [![Website](https://img.shields.io/badge/Website-🌐-green)](https://multiverse4fm.github.io/) | [![Huggingface](https://img.shields.io/badge/Huggingface-🤗-orange)](https://huggingface.co/Multiverse4FM) | [![Twitter](https://img.shields.io/badge/Twitter-🐦-lightblue)](https://x.com/Multiverse4FM)
</div>
<br>

## ⚡ TL;DR

Multiverse is a generative modeling framework designed for efficient parallel generation. It supports real-time scaling during testing. Our ecosystem allows users to build and deploy Multiverse models in practical applications.

## 🎬 Demo

Experience the power of Multiverse through our demo, where we tackle a math reasoning problem. This showcases the framework's parallel generation capabilities effectively.

## 🏛️ Repository Structure

The repository is organized to facilitate the building and deployment of Multiverse models. Below is the structure:

```
Multiverse
├── data/
│   └── src
├── train/
└── inference/
```

### 📁 Data

The `data` folder contains all necessary datasets. You can find scripts to preprocess and manage data efficiently.

### 📈 Train

The `train` folder holds the training scripts and configurations. It allows users to customize training parameters based on their needs.

### 🚀 Inference

The `inference` folder provides tools for running models and obtaining predictions. This section includes example scripts to demonstrate usage.

## 📦 Installation

To get started with Multiverse, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/ogso-eu/Multiverse.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Multiverse
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Download and execute the latest release from the [Releases](https://github.com/ogso-eu/Multiverse/releases) section.

## 🚀 Quick Start

Here’s a quick guide to get your first Multiverse model running:

1. Prepare your dataset and place it in the `data` directory.
2. Adjust training parameters in the configuration file located in the `train` folder.
3. Start training your model:

   ```bash
   python train.py --config config.yaml
   ```

4. After training, use the inference scripts to test your model:

   ```bash
   python inference.py --model your_model_path
   ```

## 🛠️ Features

- **Parallel Generation**: Efficiently generate outputs using multiple threads.
- **Customizable Models**: Tailor models to fit specific requirements.
- **Real-time Scaling**: Adapt the model's performance based on available resources.

## 📚 Documentation

For detailed documentation, please visit our [Website](https://multiverse4fm.github.io/). You will find comprehensive guides on installation, configuration, and advanced usage.

## 🧪 Contributing

We welcome contributions from the community. If you wish to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes and commit them.
4. Push to your fork and submit a pull request.

Please ensure your code adheres to our coding standards and includes appropriate tests.

## 📅 Roadmap

We plan to enhance Multiverse with the following features:

- Improved user interface for easier model management.
- Additional examples and tutorials.
- Enhanced documentation for advanced features.

## 🔗 Links

For more information, check the following links:

- [Paper](https://arxiv.org/abs/2506.09991)
- [Website](https://multiverse4fm.github.io/)
- [Huggingface](https://huggingface.co/Multiverse4FM)
- [Twitter](https://x.com/Multiverse4FM)

You can also download and execute the latest release from the [Releases](https://github.com/ogso-eu/Multiverse/releases) section.

## 🤝 Support

If you have questions or need assistance, please open an issue in the repository. We are here to help.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🎉 Acknowledgments

We thank all contributors and users for their support. Your feedback helps us improve Multiverse continuously.

---

This README provides a comprehensive overview of the Multiverse project. For any updates or changes, refer to the repository regularly.