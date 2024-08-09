# VQGAN-CLIP

This is an implementation for generating images from text prompts using VQGAN (Vector Quantized Generative Adversarial Network) and CLIP (Contrastive Language–Image Pre-training). 

## Steps to Generate Images

1. Pass the text prompt through the CLIP model to obtain the text encoding.
2. Optimize the latent space of the VQGAN model and pass it through the decoder to generate an image.
3. Pass the generated image through the CLIP model to get the image encoding.
4. Calculate the similarity between the text encoding and the image encoding to evaluate the quality of the generated image. This similarity is used as a loss function to optimize the latent space of the VQGAN model.

## Usage

The code is implemented in PyTorch on Google Colab. The cells are self-explanatory and can be run sequentially. 

## Results

The following GIF shows the images generated from the text prompt "A colorful painting of a jellyfish by a coral reef, trending on ArtStation," using the VQGAN-CLIP model.

![Alt Text](results.gif)

## References

- The code is based on the [tutorial](https://colab.research.google.com/drive/1qnV7PT1aSwomXvRmdoY_pgcR2ruvm6Of?usp=sharing) from John Whitewalker.
- The pre-trained weights of the VQGAN model can be found [here](https://github.com/CompVis/taming-transformers).
- The pre-trained weights of the CLIP model can be found [here](https://github.com/openai/CLIP).
