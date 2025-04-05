# cellfinder: Implementing a New Deep Learning Architecture (Adithya Sau)

---

## **Personal Details**

- **Full Name:** Adithya Sau  
- **Email:** adithyasau@gmail.com  
- **GitHub Username:** https://github.com/Adisauz  
- **Zulip Username:** https://neuroinformatics.zulipchat.com/#recent_topics  
- **Location & Time Zone:** Pune, India (UTC+5:30)  

---

## **Code Contribution**

https://github.com/brainglobe/brainglobe.github.io/pull/314
-Added an Examples of brainreder in sphinx documentation
https://github.com/neuroinformatics-unit/ethology/pull/82
-Added a python program that can extract evenly spaced frames over a specified interval.
https://github.com/neuroinformatics-unit/ethology/pull/81
-Added a python program and can track object(cars) when user selects on the detected object
---


## **Project Proposal**

### **Synopsis**

Cellfinder is a BrainGlobe tool used to detect cells in large whole-brain images. It currently uses a Residual Neural Network (ResNet) to classify cell candidates into cells and non-cells. However, deep learning architectures have significantly advanced since ResNet's introduction. This project aims to explore and implement newer architectures, such as Vision Transformers (ViT) or hybrid models, as alternatives to ResNet.

This project aims to improve classification accuracy, speed, and efficiency for 3D brain image analysis. By integrating modern deep learning techniques, we aim to enhance cellfinder's ability to process complex brain imaging data while maintaining compatibility with its existing workflows.

### **Deliverables**
1. A Python implementation of at least one new deep learning architecture integrated into cellfinder.
2. Quantitative comparisons between the current ResNet architecture and the new architecture.
3. Tests to ensure the functionality of the new implementation.
4. Comprehensive documentation explaining the new architecture and its integration into cellfinder.
5. A blog post detailing the improvements, challenges, and insights gained during the project.
# Pipeline Overview

### 1. Data Preparation
**Input:** Whole-brain 3D image data (signal and background channels).

**Process:**
- Extract 3D patches from the images.
- Apply preprocessing techniques (normalization, augmentation, noise addition).

**Output:** Preprocessed 3D patches ready for training.


### 2. Model Architecture
**Hybrid Model:** Combines ResNet for local feature extraction and Vision Transformer (ViT) for global attention.

#### Components:
- **ResNet backbone** for spatial feature extraction.
- **ViT module** for attention-based global context understanding.
- **Cross-attention layer** to fuse ResNet and ViT features.



### 3. Training Pipeline
#### Steps:
1. Initialize weights using pre-trained models (ImageNet).
2. Train using Adam optimizer with cosine learning rate decay.
3. Apply data augmentation and batch normalization during training.



### 4. Optimization
- Quantize the trained model to reduce memory usage and improve inference speed.
- Use mixed precision training for faster computation.



### 5. Integration with cellfinder
- Modify the classifier module to support the new architecture.
- Ensure compatibility with existing preprocessing pipelines and napari visualization tools.


### 6. Validation & Testing
- Compare performance metrics (F1-score, inference speed, GPU memory usage) between ResNet and the new hybrid model.
- Perform unit tests to ensure robustness.

### Summary of Process

| Step             | Description                                                      |
|-----------------|------------------------------------------------------------------|
| **Data Preparation** | Extract patches and preprocess them for training.              |
| **Model Design**    | Develop ResNet-ViT hybrid architecture for cell classification. |
| **Training**        | Train the model with augmented data and optimized hyperparameters. |
| **Optimization**    | Quantize the model for efficient deployment in large-scale datasets. |
| **Integration**     | Incorporate the new classifier into cellfinder's ecosystem.    |
| **Validation**      | Test accuracy, speed, and memory usage compared to ResNet baseline. |

---

### **Implementation Timeline**

| Week | Tasks | Hours/Week |
|------|-------|------------|
| **Community Bonding** | Finalize architecture design, set up test environments, and familiarize with cellfinder's codebase. | 20 |
| **Week 1–2** | Implement a prototype of the Vision Transformer (ViT) model for 3D classification tasks. | 35 |
| **Week 3–4** | Integrate the ViT model with cellfinder's preprocessing pipeline and test on sample datasets. | 35 |
| **Week 5–6** | Develop an active learning framework to reduce manual annotation requirements by enabling uncertainty-based sampling. | 35 |
| **Week 7–8** | Optimize the model using quantization techniques (e.g., 8-bit models) and add multi-GPU support for large datasets. | 35 |
| **Week 9–10** | Extend the Napari plugin to enable interactive training/validation workflows using the new model. | 35 |
| **Week 11–12** | Finalize testing, benchmarking, documentation, and write a blog post summarizing results and challenges. | 35 |

---

### **Communication Plan**

- **Daily Updates:** Share progress updates in the BrainGlobe Zulip stream.
- **Weekly Meetings:** Schedule video calls with mentors (@IgorTatarnikov and @alessandrofelder) to discuss progress, blockers, and next steps.
- **PR Reviews:** Submit code regularly via GitHub pull requests for mentor feedback.
- **Emergency Communication:** Direct messaging via Zulip or email.

---

## **Personal Statement**

I am a third-year undergraduate at BITS Pilani, KK Birla Goa Campus, pursuing a Bachelor's degree in Electronics and Electrical Engineering. With a strong foundation in software engineering, I specialize in Python, machine learning, and building scalable systems.I am a software engineer with expertise in Python, machine learning, and scalable systems. Currently, I am working on a research paper titled "Cognitive Neuroscape: Gamified Frameworks for Multi-Dimensional Cognitive Assessment in Neurodegeneration". This project focuses on designing goal-based games to evaluate cognitive performance across age groups, leveraging machine learning to identify early biomarkers for neurodegenerative diseases.

This aligns closely with the cellfinder project, as both involve applying advanced computational methods to neuroscience challenges. My experience developing scalable AI solutions, such as a multilingual speech recognition app using AWS services and StickerForecast—a market forecasting model ranked in the global top 500—has equipped me with the skills to implement and optimize new architectures for cellfinder. By contributing to this project, I aim to advance open-source tools that empower researchers in neuroscience.
---

## **Availability**

I am fully available during the GSoC period (25 hours/week). I have no conflicting commitments such as school or work during this time. I may have an mandatory internship from mid-August from my college but I will find 3 hours/day for GSOC work and get the rest of the work done over the weekend.

---

## **GSoC Details**

### What do you expect from the program?
I hope to gain hands-on experience contributing to an impactful open-source project while enhancing my skills in deep learning for neuroscience applications.  

### Are you also applying to projects with other organizations?
No, I am exclusively applying to BrainGlobe projects as they align perfectly with my interests and career goals.

---
## **GSOC Experiences** ##
This is my first time applying for GSOC :)

---
