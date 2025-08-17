# Price-Tagging System

Predict Yelp business price tiers (`$`, `$$`, `$$$`, `$$$$`) from user-submitted photos using a fine-tuned CNN.

---

## Overview

This project implements an end-to-end pipeline to:

1. Stream and join the Yelp Academic Dataset’s business metadata (with `RestaurantsPriceRange2`) and photo metadata.
2. Download and preprocess images (resize to 224×224, normalize).
3. Build a train/validation split with balanced classes.
4. Train a classifier on top of a frozen MobileNetV2 backbone.
5. Improve mid-tier performance via data augmentation, class-weighted loss, and fine-tuning.
6. Evaluate with precision, recall, F1, and a confusion matrix.
