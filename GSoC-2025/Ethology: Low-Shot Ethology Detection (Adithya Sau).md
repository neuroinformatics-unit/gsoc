# Ethology: Low-Shot Ethology Detection (Adithya Sau)

## **Personal Details**

- **Full Name:** Adithya Sau  
- **Email:** adithyasau@gmail.com  
- **GitHub Username:** https://github.com/Adisauz  
- **Zulip Username:** https://neuroinformatics.zulipchat.com/#user/882256  
- **Location & Time Zone:** Pune, India (UTC+5:30)
- **project portfolio:**
  - **[Synthia_Areete](https://github.com/Adisauz/Synthia_Areete)**:A Streamlit app for recording cow milk yield using Hindi speech input, powered by AWS services (S3, Transcribe, Translate, Polly)
  - **[Sticker_Forcasting](https://github.com/Adisauz/Sticker_Forcasting)**: A machine learning project to predict sticker demand.

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

- Develop PyTorch-compatible adapter classes for **GeCo** (tile-based processing, COCO format normalization) and **CountGD** (text-to-embedding conversion using HuggingFace `transformers`, dynamic confidence thresholds).  

- Implement bounding box format conversion (COCO ↔ YOLO ↔ PascalVOC) using OpenCV and NumPy.  

- Extract CLIP-based prompt embeddings for text-based detection.  

- Ensure multi-frame consistency with optical flow tracking (5-frame window).  

- Design inference API endpoints like `/detect` for batch processing and `/annotations` for JSON-based storage.  

- Optimize inference with mixed precision (FP16) and default frame resizing (640×640).  

- Enable video loading (MP4/AVI/TIFF) with lazy loading in a Napari widget.  

- Provide a dual-layer canvas in the widget for predictions and manual edits.  

- Include real-time FPS and GPU memory monitoring in the widget.  

- Allow model selection (GeCo/CountGD), adjustable confidence sliders (0.1–0.9), and preset modes for Speed (FP16), Accuracy (FP32), and Balanced performance in the configuration panel.  

- Support CSV format for frame-wise detections and JSON schema for metadata + annotations during import/export.  

- Implement zlib compression (level 3) for large files during import/export.  

- Achieve >15 FPS at 480p resolution, <80% GPU memory usage, and <2 false positives per frame as optimization targets.  

- Include resolution scaling sliders (360p–720p), adaptive batch sizes (1–4 frames), and optional frame skipping with optical flow validation as trade-off controls.

#### **Stretch Goals**
- Add **interactive correction tools** (brush/eraser) for refining annotations directly in the UI.
- Implement **multi-scale inference** to detect both fine details (e.g., baby bees) and broader context (e.g., hive structure), balancing improved accuracy with increased computational costs and potential duplicate detections.  
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
| 12   | Finalize submission materials by reviewing, conducting testing (also done weekly), fixing bugs, ensuring stability, and allocating buffer time for unexpected issues. |

#### Relevant Datasets and Their Annotations

- **[NEON Beetles Dataset](https://huggingface.co/datasets/imageomics/2018-NEON-beetles)**: Includes annotations such as bounding boxes, elytra measurements, and species metadata. It supports object detection and classification for biodiversity studies.

- **[Ant Detection Dataset](https://datasetninja.com/ant-2)**: Provides bounding boxes and key points for ant localization, making it ideal for object detection and behavioral analysis.

- **[Insect Detect Dataset](https://universe.roboflow.com/maximilian-sittinger/insect_detect_classification_v2)**: Features bounding boxes for various insect species (e.g., bees, flies) and is useful for real-time insect monitoring and ecological research.

- **[Leaf Beetle Image Dataset](https://images.cv/dataset/leaf-beetle-image-classification-dataset)**: Contains labeled images with bounding boxes for beetles, supporting classification tasks for species identification.

- **[BaboonLand Dataset](https://baboonland.xyz/)**: Likely includes annotations such as bounding boxes, tracking IDs, and behavior labels for baboons in their natural habitat. It is useful for studying baboon behavior, tracking movements, and analyzing group dynamics in ethology research.
#### Work Commitment
- **Hours per week:** ~25-35
- **Planned vacation:** May 15 - June 1

### Communication Plan
- **Mentor Meetings:** Weekly video calls
- **Asynchronous Communication:** Zulip chat for discussions, GitHub for PR reviews
- **Documentation & Reports:** Weekly progress updates on GitHub Issues

## Personal statement

I am a third-year undergraduate at BITS Pilani, KK Birla Goa Campus, pursuing a Bachelor's degree in Electronics and Electrical Engineering. With a strong foundation in software engineering, I specialize in Python, machine learning, and building scalable systems. 
My research, "Cognitive Neuroscape," explores gamified cognitive assessments and machine learning for early detection of neurodegenerative diseases. Guided by Dr. Veeky Baths at BITS Pilani, we are enhancing the framework with adaptive gameplay and advanced models for personalized assessments of the current research paper. [Research_Link](https://xr.jmir.org/2024/1/e59197)

This work closely aligns with the Ethology project, as both involve applying computational techniques to neuroscience challenges. My experience building scalable AI solutions, such as a multilingual speech recognition app using AWS, and StickerForecast, a market forecasting model ranked in the global top 500 out of 10,000, has equipped me to implement and optimize novel architectures for platforms like cellfinder. I’m eager to contribute to open-source tools that advance neuroscience research and accessibility.
### Past Experience
I have experience in Python, machine learning, and scalable systems, with prior work in deep learning-based detection models. Familiar with PyTorch, OpenCV, and napari, I have built ML-based tools for real-world applications, including annotation pipelines.

### Motivation
I'm passionate about computer vision and ethology. This project excites me because it bridges ML with behavioral analysis, enabling researchers to extract insights from animal studies efficiently.

### Match
With expertise in deep learning, experience in API design, and familiarity with napari, I am well-suited for this project. My past work on ML-driven object detection and optimization aligns with the project's goals. I started using napari a month ago, building a small project—Conway’s Game of Life—now on [GitHub](https://github.com/Adisauz/Napari-example/blob/main/conwayGOL.py). I’m still new but excited to learn more.

### Availability
I have no conflicting commitments until mid-August, so I’ll be able to fully focus on GSoC during the community bonding and early coding period. From mid-August onward, I may have a mandatory internship as part of my college curriculum. However, I’ve planned my schedule to ensure I can dedicate at least 3 hours per day on weekdays and more time over weekends to continue making consistent progress on the project.

## GSoC

### GSoC Experience
I expect to gain hands-on experience in open-source collaboration, learning best practices for scalable ML model deployment, and GUI integration.

### Other Applications
I am only trying to apply to this organisation.
