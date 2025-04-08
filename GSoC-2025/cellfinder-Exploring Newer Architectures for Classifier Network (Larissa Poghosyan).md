# <p style="font-size: 22px; line-height: 1.15;"> cellfinder: Exploring Newer Architectures for Classifier Network (Larissa Poghosyan)</p>

## Personal details
- **Full name** Larissa Poghosyan
- **Email** larissa.poghosyan@gmail.com
- **GitHub username** larissapoghosyan
- **Zulip username** Larissa Poghosyan (User ID 891828)
- **Location & time-zone** London, UK (GMT+1 British Summer Time)
- **Personal website / project portfolio** https://github.com/larissapoghosyan
- **Code contribution**
    - https://github.com/aimhubio/aim/pull/3319
    - https://github.com/codezonediitj/pydatastructs/pull/595
    - https://github.com/brainglobe/cellfinder/pull/495

      This PR presents a functional proof-of-concept Vision Transformer classifier, fully compatible with existing cellfinder architecture.

- **Proposal discussion link**
    - https://github.com/brainglobe/cellfinder/pull/495

      This PR presents the PoC implementation, references to related codebases and literature, and invites the community to discussion.

## Project proposal 
- **Synopsis**

Accurate detection of labeled cells in whole-mouse-brain 3D microscopy images is essential for understanding brain-wide neural circuits. While simple thresholding can extract cell locations, it often results in a high false positive rate.<br>
To address this challenge, cellfinder first extracts candidate locations using the same approach, and then employs a 3D ResNet-based classifier to distinguish true cells from artifacts using local image cuboids.<br>
This project aims to improve detection accuracy and robustness without increasing computational cost, by upgrading cellfinder’s classifier with Vision Transformers (ViTs), drawing on recent studies that demonstrate ViTs outperform convolutional networks in biomedical image classification tasks.


- **Implementation timeline**

    - Implement ViT in Keras, while keeping the classifier network abstractions compatible
    - Full-scale training, and quantitative comparison with current ResNet classifier
    - Performance testing on CPUs and GPUs
    - Add changes to relevant BrainGlobe repos (e.g., [brainglobe-workflows](https://github.com/brainglobe/brainglobe-workflows/blob/main/brainglobe_workflows/brainmapper/main.py)) to integrate the new functionality into full the workflow.
    - Add support of loading and fine-tuning pretrained backbone models
    - Add unit tests to cover all the changes
    - Add documentation
    - Write a blogpost

- **Stretch goal:**
    - Add support for 2D ViT, if the necessary framework and data adjustments for 2D cell detection are completed in time.

    ---

| **Week**      | **Dates**         | **Deliverables**   |
|---------------|-------------------|--------------------|
| **Week 0** <br>COMMUNITY BONDING | May 8 - Jun 1 | - Refine the existing ViT implementation (current PR).<br>- Start testing on large-scale data.<br>- Finalize benchmarking plan and GPU setup.<br>- Monitor upstream PRs (e.g. #493) for compatibility. |
| **Week 1**    | Jun 2 - Jun 9     | - Add ViT model configs to the training pipeline.<br>- Set up experiment tracking (e.g. with Weights & Biases) and create a public project board. <br>- Launch full-scale training runs on GPU. <br>- Implement changes in [cellfinder_train CLI](https://github.com/brainglobe/cellfinder/blob/main/cellfinder/core/train/train_yaml.py) to enable the ViT classifier.|
| **Week 2**    | Jun 10 - Jun 16   | - Begin performance analysis on CPU vs GPU.<br>- Collect accuracy, loss, and training speed metrics.<br>- Compare with current ResNet model.<br>- Log results to experiment tracker. |
| **Week 3**    | Jun 17 - Jun 23   | - Add support for loading pretrained 3D ViT backbones.<br>- Implement fine-tuning mechanism.<br>- Test with public pretrained ViTs (if available). |
| **Week 4**    | Jun 24 - Jun 30   | - Ensure compatibility of external repositories (cellfinder_download, brainmapper) with the new changes. <br>- Modularize architecture selection and Python API. <br>- Continue benchmarking on multiple datasets.<br>- Polish training scripts/configs. |
| **Week 5** <br>PRE-MIDTERM PREP | Jul 1 - Jul 7    | - Finalize and analyze benchmarking results (ViT vs ResNet).<br>- Sync with mentors for midterm prep.<br>- Address any issues in API/plugin integration. |
| **Week 6** <br>MIDTERM         | Jul 8 - Jul 14   | - Submit midterm evaluation.<br>- Share benchmarking summary and gather feedback.<br>- Plan next steps with mentor input. |
| **Week 7**    | Jul 15 - Jul 21   | - Write unit tests for ViT classifier pipeline.<br>- Ensure compatibility with data loader refactor (`#493`).<br>- Begin writing user/developer documentation. |
| **Week 8**    | Jul 22 - Jul 28   | - Finalize documentation (training, fine-tuning, CLI usage).<br>- Add lightweight support for 2D classification mode (Stretch Goal)<br> - Implement necessary changes in the Napari plugin to support ViT classifier. |
| **Week 9**    | Jul 29 - Aug 4    | - Add support for advanced ViT variants (DeiT, DINO, Swin).<br>- Integrate backbone selection cleanly into training pipeline.<br>- Run test training on at least one variant. <br> - Validate on small 2D image slices (Stretch Goal) |
| **Week 10**   | Aug 5 - Aug 11    | - Complete variant model testing and collect comparison results.<br>- Final cleanup of codebase, refactor and organize files.<br>- Validate full test coverage and model switching. |
| **Week 11**   | Aug 12 - Aug 18   | - **Code freeze**: finalize codebase for submission.<br>- Write and publish final blog post summarizing work, results, and next steps. |
| **Week 12** <br>FINAL WEEK      | Aug 19 - Sep 1   | - Submit final GSoC report and code.<br>- Review and respond to mentor feedback.<br>- Ensure documentation is contributor-friendly and future-ready. |
- **Communication plan**
  
   I’d prefer **weekly video calls (around 20-30 minutes)** with my mentors to discuss progress and plan next steps. For quick feedback, I’ll stay active on **Zulip**. I plan to work **4-5 hours daily** (around **25-35 hours per week**), to meet the project time requirements.
---
## Personal statement
- **Past experience**
  
  **Academic Experience:** I hold a degree in Data Science, with a focus on mathematics, machine learning, and data analytics. My thesis explored the use of Natural Language Processing (NLP) and Machine Learning, specifically analyzing the effectiveness of pre-trained models in real-world applications. Additionally, I was part of the founding cohort of a Data Science club at my university, where we collaborated on projects that benefited both the university and the wider community.

  **Technical Experience:** During my studies, I interned at Metric as an ML/AI intern, where I developed NLP solutions for text classification and sentiment analysis using Python, scikit-learn, Keras, PyTorch and TensorFlow. I collaborated on data preprocessing, feature engineering, and model optimization to enhance text processing efficiency. After that, I joined VXsoft as a junior developer, working on government projects to develop a secure document management system. I collaborated with senior developers on database design and user interface development, improving document storage, retrieval, and user controls. This experience strengthened my skills in communication, project management, and secure software development while giving me hands-on exposure to the full application lifecycle.

- **Motivation: why this project?**

    The BrainGlobe initiative and Cellfinder caught my attention for their contributions to neuroinformatics and ML-driven research automation. I’m passionate about neuroinformatics and excited to apply my skills to this impactful project. Having worked with transformers, I’m eager to help optimize the current implementation and develop scalable, reliable solutions for researchers. I also value the open-source nature of the initiative, aligning with my desire to collaborate and create tools that benefit the scientific community.

- **Match: why you?**
  
    With a strong foundation in **machine learning**, **algorithms**, and **software development**, I have hands-on experience with frameworks like **PyTorch**, **TensorFlow**, and **Keras**. I prioritize writing **clean, maintainable code** and quickly adapt to new technologies to solve complex problems. Recently, I implemented the **proof-of-concept implementation** of a **Vision Transformer (ViT)** model for cell classification in **Cellfinder**, ensuring backward compatibility with the existing codebase. This project aligns with my passion for applying ML to advance scientific research, and I am excited to collaborate, contribute my expertise, and make a meaningful impact while continuing to grow professionally. 

- **Availability**
  
  I am available from **May 1 to October 1**, with no academic or professional commitments. I plan to dedicate **25–35 hours per week** to meet the project requirement, and I’m flexible to put in extra hours as needed to meet deadlines or refine deliverables.

## GSoC
- **GSoC experience**
  
    I’m excited about GSoC as a way to contribute to meaningful **open-source work** and become part of a **global community**. Working on **Cellfinder** will allow me to collaborate closely with mentors and researchers, while learning how software can drive scientific discovery.

- **Are you also applying to projects with other organisations in GSoC 2025?**
  
    I initially considered several organizations and explored PyDataStructs by Open Science Labs, where I authored a pull request and made some changes. However, I ultimately decided to focus solely on the Cellfinder project to ensure I have meaningful contributions and a strong proof of concept before applying.
    I will not be applying elsewhere within GSoC program this year.
