# Image Processing & Deep Learning – Assignment Overview

This repository contains solutions to four assignments related to image processing and deep learning.  
Each assignment is organized in a separate folder:

- `task_1`: CNN for Image Classification
- `task_2`: GAN for Face Generation
- `task_3`: Creative Image Transformation with InstructPix2Pix
- `task_4`: Semantic Image Search using CLIP


## Task 1 – CNN for Image Classification (14 points)

Train and evaluate a Convolutional Neural Network (CNN) using the CIFAR-10 dataset (60,000 32×32 color images in 10 classes).

**Main Steps:**
- Load and split CIFAR-10 dataset.
- Normalize image pixel values to [0, 1] and one-hot encode the labels.
- Design a CNN architecture with appropriate layers and activation functions.
- Train the model with suitable optimizer and loss function.
- Evaluate the model on the test set.
- Experiment with different architectures and hyperparameters.
- Document the final accuracy and architecture used.

**Tools & Libraries:** TensorFlow, Keras  
**Output:** Code, model evaluation, accuracy metrics, training visualizations, and architecture documentation.

You can find all packages necessary to run the notebook `cnn_classifier.ipynb` in the file `requirements_1&2.txt`.


## Task 2 – GAN for Face Generation (12 points)

Use a pre-trained Progressive GAN (progan-128) from TensorFlow Hub to generate and interpolate face images.

**Tasks:**
- Generate and display 4 random face images using sampled latent vectors.
- Choose two random vectors and interpolate between them (λ ∈ [0, 1], step size 0.1).
- Visualize the morphing both in latent space and image space.

**Tools & Libraries:** TensorFlow, TensorFlow Hub  
**Output:** Generated images and interpolation results.

You can find all packages necessary to run the notebook `gan_face_gen.ipynb` in the file `requirements_1&2.txt`.

## Task 3 – Creative Image Transformation (10 points)

Use the InstructPix2Pix model to perform artistic transformations on real-world images using text prompts.

### a) Theoretical Part:
- Explain how InstructPix2Pix works (Pix2Pix, cGANs, CLIP).
- Discuss its use cases in art, design, and marketing, and its advantages over traditional tools like Photoshop.

### b) Practical Part:
- Select 5 images of Brandenburg city or university campus.
- Apply creative transformations using various text prompts via the InstructPix2Pix interface.
- Document original and transformed images and reflect on the results.

**Tools:** InstructPix2Pix (Hugging Face Space)  
**Output:** Theory summary, transformed images, and qualitative evaluation.

**Image Sources:**
- [Roland](./task_3/images/roland.jpg): https://erlebnis-brandenburg.de/wissen-und-geschichten-details/donnerbart
- [WWZ](./task_3/images/wwz.jpeg): https://www.brandenburg-live.com/wp-content/uploads/2024/08/035-PM-THB_WWZ-c-Oliver-Karaschewski-1920x1280.jpeg

You can find all packages necessary to run the notebook `instruct_pix2pix.ipynb` in the file `requirements_3.txt`.

## Task 4 – Semantic Image Search with CLIP (14 points)

Develop a semantic image search system using OpenAI's CLIP model to retrieve images based on textual queries and image similarity.

### a) Text-to-Image Search:
- Load a dataset of 500 travel images.
- Perform semantic search using 5 predefined queries (e.g., “Sunflower field”, “Cows in the mountains”).
- Compute cosine similarity between text and image embeddings and retrieve top 5 matches.

### b) Custom Dataset Search:
- Create a new dataset with ~100 diverse images (e.g. from Pixabay).
- Run semantic search using well-defined custom queries.
- Evaluate performance and analyze matching quality.

### c) Image-to-Image Search:
- Choose 3 thematic reference images.
- Use CLIP to retrieve the most similar images from the custom dataset.

**Tools & Libraries:** CLIP (e.g., `openai/clip-vit-base-patch32`), PIL, cosine similarity  
**Output:** Retrieved images, similarity evaluations, and documentation of results.