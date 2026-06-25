# 🛍️ VisionCart-AI : A Multimodal Product Intelligence System

A CLIP-based multimodal AI system that addresses three common e-commerce challenges:

* Smart Product Recommendation
* Unique Product Catalog Creation
* Reverse Product Search

The project uses a single CLIP embedding pipeline and reuses the generated embeddings across all tasks, making the system efficient and scalable.

---

## Overview

This project demonstrates how multimodal embeddings can be leveraged to solve multiple product intelligence problems within an e-commerce environment.

Using CLIP (Contrastive Language-Image Pretraining), images and text are mapped into a shared embedding space, enabling semantic understanding across modalities.

---

## Features

### Smart Product Recommendation Engine

Unlike traditional recommendation systems that suggest visually similar products, this system recommends complementary products.

**Example**

Input:

* Formal Shirt

Output:

* Formal Trousers
* Leather Belt
* Dress Shoes
* Tie

---

### Unique Product Catalog Creation

Duplicate and near-duplicate products are identified using CLIP embeddings and similarity-based clustering.

Benefits:

* Reduced catalog redundancy
* Cleaner inventory management
* Improved search quality

---

### Reverse Product Search

Users can search products using natural language descriptions.

**Example Queries**

* "blue casual shirt"
* "women's red dress"
* "black running shoes"

The system retrieves the most semantically relevant products using CLIP text-image similarity.

---

## System Architecture

```text
Product Images
       │
       ▼
   CLIP Model
       │
       ▼
 Image Embeddings
       │
 ┌─────┼─────┐
 │     │     │
 ▼     ▼     ▼

Task 1  Task 2  Task 3
Recommendation
Deduplication
Reverse Search
```

---

## Tech Stack

* Python
* PyTorch
* OpenAI CLIP (ViT-B/32)
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn

---

## Methodology

### Embedding Generation

Product images are processed using CLIP to generate semantic embeddings.

### Task 1: Recommendation Engine

* Define complementary product categories
* Filter candidate products
* Rank recommendations using CLIP similarity

### Task 2: Duplicate Detection

* Generate image embeddings
* Apply similarity-based clustering
* Identify duplicate product groups

### Task 3: Reverse Product Search

* Convert text query into CLIP embedding
* Compare against image embeddings
* Retrieve top matching products

---

## Results

### Smart Product Recommendation

Generated category-aware recommendations instead of same-category suggestions.

### Duplicate Product Detection

Successfully grouped visually similar products and reduced catalog redundancy.

### Reverse Product Search

Retrieved relevant products for natural language queries without task-specific training.

---

## Project Structure

```text
multimodal-product-intelligence/
│
├── notebook/
│   └── Multimodal_Product_Intelligence.ipynb
│
├── report/
│   └── Project_Report.pdf
│
├── assets/
│   ├── recommendation_output.png
│   ├── duplicate_detection.png
│   ├── unique_catalog.png
│   └── reverse_search.png
│
└── README.md
```

---

## Future Improvements

* Fashion-specific CLIP fine-tuning
* Real-time recommendation APIs
* Vector database integration
* Streamlit-based interface
* Personalized recommendations using user behavior

---

## Dataset

Fashion Product Images Small Dataset

https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-small

---

## Author

**Nishita P**

Built as part of the AlgoUniversity GenAI Bootcamp.
