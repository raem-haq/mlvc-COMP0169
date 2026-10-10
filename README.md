# Visual Computing Experiments

Five in-progress notebooks collect visual-computing experiments. The eventual project direction is still open; these are focused explorations rather than a finished application.

## Experiments

1. [Linear fitting](notebooks/linear-fitting.ipynb): a small supporting least-squares demonstration.
2. [Image retrieval](notebooks/image-retrieval.ipynb): feature extraction and nearest-neighbour ranking; the extractors and ranker still need implementation.
3. [Image denoising](notebooks/denoising.ipynb): Gaussian filtering and a learned convolutional denoiser.
4. [Texture synthesis](notebooks/texture-synthesis.ipynb): feature statistics and pixel optimization.
5. [Neural implicit representation](notebooks/implicit-representation.ipynb): MLPs for image and short-sequence representation.

## From-Scratch Context

The original exercises restricted convenience APIs: `numpy.polyfit`, `numpy.linalg.solve`, scikit-learn's `linear_model` and `decomposition` modules, Torch's PCA/SVD helpers (`torch.pca_lowrank`, `torch.svd`, `torch.linalg.svd`), and OpenCV denoising functions. This explains the original “from scratch” constraint; it is not a claim that the experiments are complete.

## Data and Setup

All image inputs are stored under `data/`. The denoising notebook reads its paired images and filtering examples locally; image retrieval uses the bundled query and database images. The texture reference image is local, and its regular pattern and the implicit-representation sequence are generated in their notebooks.

The texture notebook uses torchvision's pretrained VGG19 features. On first use, torchvision may download the model weights if they are not already cached. Install Python packages in an environment that includes PyTorch, torchvision, NumPy, Matplotlib, Pillow, scikit-image, scikit-learn, tqdm, and imageio.

Some model, training, and comparison cells are unfinished.
