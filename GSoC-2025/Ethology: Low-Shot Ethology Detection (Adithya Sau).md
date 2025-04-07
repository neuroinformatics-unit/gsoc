# Ethology: Low-Shot Ethology Detection (Adithya Sau)

## **Personal Details**

- **Full Name:** Adithya Sau  
- **Email:** adithyasau@gmail.com  
- **GitHub Username:** https://github.com/Adisauz  
- **Zulip Username:** https://neuroinformatics.zulipchat.com/#user/882256  
- **Location & Time Zone:** Pune, India (UTC+5:30)  

---

## **Code Contribution**

- [brainglobe.github.io#314](https://github.com/brainglobe/brainglobe.github.io/pull/314)  
  Added an example of `brainrender` usage in the Sphinx documentation to improve clarity and usability for new users.

- [ethology#82](https://github.com/neuroinformatics-unit/ethology/pull/82)  
  Developed a Python script to extract evenly spaced frames from a video within a specified interval, useful for data preprocessing and annotation.

- [ethology#81](https://github.com/neuroinformatics-unit/ethology/pull/81)  
  Implemented a Python tool that enables object tracking (e.g., cars) based on user selection of a detected object, enhancing manual control during analysis.

---
- **Proposal discussion link:** https://github.com/neuroinformatics-unit/gsoc/pull/51

## Project proposal 

### Synopsis
This project aims to integrate low-shot detection models (GeCo and CountGD) into a unified ethology detection tool with a napari-based GUI. The project involves developing API adapters for these models, creating an interactive napari widget for annotation, and optimizing model inference for performance. Deliverables include a working napari plugin, batch-processing support, and benchmarked performance metrics.

### **Implementation Timeline**

#### **Minimal Deliverables**
- Develop adapter classes for **GeCo** and **CountGD**, ensuring compatibility with their respective PyTorch implementations.
- Implement **unified input/output handling**, including:
  - Bounding box format conversion (COCO ↔ model-specific formats).
  - Prompt embedding extraction for text-based detection (for CountGD).
  - Multi-frame consistency checks to ensure detection stability across frames.
- Design and implement an **API** to handle model inference and store annotations in a structured format.
- Develop a **basic Napari widget** that enables:
  - Loading and displaying video frame sequences.
  - Manual annotation via bounding boxes.
- Implement a **model configuration panel** allowing users to select models, set parameters, and adjust **confidence sliders**.
- Enable **CSV/JSON import-export** functionality to allow saving and loading annotations efficiently.

#### **Stretch Goals**
- Add **interactive correction tools** (brush/eraser) for refining annotations directly in the UI.
- Implement **multi-scale inference support** to improve detection accuracy on different zoom levels.
- Integrate **CLIP-based text prompts** for CountGD to allow text-based detections.

#### **Weekly Timeline**

| Week | Deliverables |
|------|------------|
| 1-2  | Implement GeCo model adapter: load pretrained weights, preprocess input data, and return predictions in a standardized format. Set up a basic API structure for calling the model. |
| 3-4  | Develop CountGD model adapter: extract text prompt embeddings, support hybrid visual+text inputs, and unify its output format with GeCo. Implement bounding box conversion between COCO and model-specific formats. |
| 5-6  | Build the initial Napari widget with a frame sequence loader, thumbnail previews, and manual annotation support using bounding boxes. Allow saving/loading annotations in JSON format. |
| 7-8  | Implement model configuration panel, allowing users to select between models and adjust confidence thresholds. Add support for CSV export/import of annotations. |
| 9-10 | Optimize performance with caching (using zarr arrays for frame storage), batch processing, and multi-scale inference for improved detection accuracy. Conduct profiling using PyTorch's `torch.utils.bottleneck`. |
| 11   | Benchmark model performance on public ethology datasets (BeeTL, AntTrack) using metrics like mAP@0.5:0.95 and false positive rate. Fine-tune model parameters for optimal accuracy. |
| 12   | Finalize documentation, conduct end-to-end testing with synthetic and real datasets, fix bugs, and ensure plugin stability before submission. |


#### Work Commitment
- **Hours per week:** ~25-35
- **Planned vacation:** May 15 - June 1

### Communication Plan
- **Mentor Meetings:** Weekly video calls
- **Asynchronous Communication:** Zulip chat for discussions, GitHub for PR reviews
- **Documentation & Reports:** Weekly progress updates on GitHub Issues

## Personal statement

I am a third-year undergraduate at BITS Pilani, KK Birla Goa Campus, pursuing a Bachelor's degree in Electronics and Electrical Engineering. With a strong foundation in software engineering, I specialize in Python, machine learning, and building scalable systems. My current research, "Cognitive Neuroscape: Gamified Frameworks for Multi-Dimensional Cognitive Assessment in Neurodegeneration," explores the use of goal-oriented games to evaluate cognitive performance across age groups. We leverage machine learning to identify early biomarkers of neurodegenerative diseases.

This work closely aligns with the Ethology project, as both involve applying computational techniques to neuroscience challenges. My experience building scalable AI solutions, such as a multilingual speech recognition app using AWS, and StickerForecast, a market forecasting model ranked in the global top 500 out of 10,000, has equipped me to implement and optimize novel architectures for platforms like cellfinder. I’m eager to contribute to open-source tools that advance neuroscience research and accessibility.
### Past Experience
I have experience in Python, machine learning, and scalable systems, with prior work in deep learning-based detection models. Familiar with PyTorch, OpenCV, and napari, I have built ML-based tools for real-world applications, including annotation pipelines.

### Motivation
I'm passionate about computer vision and ethology. This project excites me because it bridges ML with behavioral analysis, enabling researchers to extract insights from animal studies efficiently.

### Match
With expertise in deep learning, experience in API design, and familiarity with napari, I am well-suited for this project. My past work on ML-driven object detection and optimization aligns with the project's goals.

### Availability
I have no conflicting commitments until mid-August, so I’ll be able to fully focus on GSoC during the community bonding and early coding period. From mid-August onward, I may have a mandatory internship as part of my college curriculum. However, I’ve planned my schedule to ensure I can dedicate at least 3 hours per day on weekdays and more time over weekends to continue making consistent progress on the project.

## GSoC

### GSoC Experience
I expect to gain hands-on experience in open-source collaboration, learning best practices for scalable ML model deployment, and GUI integration.

### Other Applications
I am only trying to apply to this organisation.
