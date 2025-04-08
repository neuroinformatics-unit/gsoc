# cellfinder: Improving cellfinder's classification algorithm (Srutanik Bhaduri)

## Personal details
- **Full name:** Srutanik Bhaduri
- **Email:** srutanik.bhaduri02@gmail.com
- **GitHub username:** srutanik
- **Zulip username:** Srutanik Bhaduri
- **Location & time-zone:** Bhopal, Madhya Pradesh, India (UTC+5:30)
- **Personal website / project portfolio:** 
- **Code contribution:**
    [https://github.com/brainglobe/cellfinder/pull/513](https://github.com/brainglobe/cellfinder/pull/513)
    *Brief description of your contribution(s).*

- **Proposal discussion link:**
    <!-- Link to the PR where this proposal is being discussed (this PR!) -->
    [Link to the Pull Request for this proposal]

## Project proposal

### Synopsis

1. **What is the project about?** 
   
   This project is about improving `cellfinder`'s old 3D ResNet-50 based classification algorithm to solve the binary classification problem of "cell" or "no cell" from all the detected artefacts within the 3D Volume of the Mouse Brain. It involves replacing/augmenting the current model with modern deep learning architectures.

2. **Why is it important and how would the Open-Source Community benefit from this project?** 
   
   Manual cell labelling is a significant bottleneck in neuroscience research. Providing a more accurate, efficient, and potentially interpretable automated classification system within the open-source `cellfinder` tool is crucial. This benefits the BrainGlobe community and neuroscience researchers by saving valuable time, enabling larger-scale analyses, increasing reproducibility, and allowing focus to shift towards scientific interpretation rather than manual annotation.

3. **What are the deliverables?** 
   
   Considering this as a large (350hr) project, the following are the main deliverables:

   1. **Models:** Python implementations integrated within the `cellfinder` framework:
      * **3D CNN + Attention Gate:** Implementation of a modern 3D CNN backbone (e.g., EfficientNet3D) combined with an Attention Gate mechanism. The goal is to enhance relevant spatial feature extraction for potentially improved classification accuracy compared to the baseline ResNet-50. ([Ref Paper Link](https://arxiv.org/abs/1808.08114))
      * **3D PIP-Net Adaptation:** Implementation adapting the Patch-based Intuitive Prototypes Network (PIP-Net) for 3D volumetric data. This aims to provide interpretable classification by learning representative 3D prototypical patches and utilizing a sparse scoring-sheet reasoning mechanism. ([Ref Paper Link](https://openaccess.thecvf.com/content/CVPR2023/papers/Nauta_PIP-Net_Patch-Based_Intuitive_Prototypes_for_Interpretable_Image_Classification_CVPR_2023_paper.pdf))
      * **(Stretch Goal) 3D WaveMix Adaptation:** Implementation adapting the WaveMix concept, using 3D Discrete Wavelet Transforms (DWT) for multi-scale context modeling as a potentially more computationally efficient alternative to dense attention mechanisms. ([Ref Paper Link](https://arxiv.org/abs/2205.14375))
      * **(Stretch Goal) Ensemble Model:** Implementation of an ensemble method (e.g., weighted averaging of predictions) combining the outputs of the best-performing newly implemented models (e.g., Attention-based + PIP-Net) to potentially maximize overall classification accuracy and robustness.

   2. **Analysis, Documentation, and Tests:**
      * **Comparative Analysis:** Deep comparative analysis of the implemented architectures against the ResNet-50 baseline, using standard classification metrics (F1 score, sensitivity/recall, specificity, accuracy, AUC, loss curves) and computational performance metrics (inference time, training time, GPU memory usage). Results will be presented clearly, likely with tables and plots.
      * **Documentation & Blog Post:** Comprehensive documentation integrated into `cellfinder`'s existing documentation, detailing the new architectures, the rationale for their use, instructions for usage (training, inference), configuration options, and a summary of the comparative analysis findings including advantages and disadvantages of each technique in the `cellfinder` context. A blog post will be written to communicate the project's goals, methods, and key results to the broader community.
      * **Testing:** Robust test suite including unit tests for core functions within the new model implementations (e.g., custom layers, loss functions) and integration tests to ensure the new models integrate correctly with `cellfinder`'s existing data loading, preprocessing, training, and inference pipelines.

### Implementation Timeline

* **Minimal Set of Deliverables:**
  1. Model Implementations: **3D CNN + Attention Gate** and **3D PIP-Net Adaptation** (first two bullet points under deliverable 1).
  2. Analysis, Documentation, and Tests: All items under deliverable 2 covering the implemented models and baseline.

* **Stretch Goals:**
  1. Model Implementation: **3D WaveMix Adaptation** (third bullet point under deliverable 1).
  2. Model Implementation: **Ensemble Model** (fourth bullet point under deliverable 1).
  3. Exploration of **Self-Supervised Pre-training** for model backbones.

* **Weekly Timeline** (Approx. 40 hours/week; Aligned with GSoC 2025 Dates)

| **Dates** | **GSoC Phase** | **Key Tasks & Milestones** |
|-----------|----------------|----------------------------|
| May 8 – June 1 | **Community Bonding** | - Finalize architecture details (backbones, attention type, PIP-Net specifics) with mentors.<br>- Deep dive into `cellfinder` classification codebase & data handling.<br>- Set up environment & baseline ResNet benchmarking framework. |
| June 2 – June 22 | **Weeks 1-3** | - Implement **3D CNN + Attention Gate** model.<br>- Integrate into `cellfinder`.<br>- Develop/adapt training script. Unit tests. Initial training/debugging. |
| June 23 – July 6 | **Weeks 4-5** | - Tune & rigorously train Attention model.<br>- **Benchmark #1:** Compare Attention vs. ResNet-50 (Accuracy, Speed etc.).<br>- Analyze results, start documentation/blog draft. |
| July 7 – July 13 | **Week 6** | - Finalize Attention model benchmarking & analysis.<br>- Prepare Midterm Evaluation materials.<br>- Plan detailed implementation for 3D PIP-Net adaptation. |
| July 14 – July 18 | **Midterm Evaluation** | - Submit evaluation. Discuss progress & PIP-Net plan. |
| July 19 – Aug 10 | **Weeks 7-9** | - Implement **3D PIP-Net adaptation** (architecture, 3D losses, 2-phase training).<br>- Integrate into `cellfinder`. Unit tests. Initial training/debugging (both phases). |
| Aug 11 – Aug 24 | **Weeks 10-11** | - Tune & rigorously train/evaluate PIP-Net.<br>- **Benchmark #2:** Compare PIP-Net vs. ResNet/Attention.<br>- **Begin Stretch Goals:** Start WaveMix/Ensemble if time permits.<br>- Write integration tests for both models. |
| Aug 25 – Sep 1 | **Week 12 (Final)** | - **Finalize Minimal Deliverables:** Complete code, benchmarks, tests, documentation, blog post for Attention & PIP-Net models.<br>- Finalize stretch goals if undertaken. Prepare code PRs. Submit final work. |
| Sep 1 – Sep 8 | **Mentor Evaluation** | - Address final feedback. Ensure smooth handover. |

### Project Length
Large (350 hours)

*(Justification: Implementing and thoroughly evaluating two distinct and potentially complex deep learning architectures (Attention-based and Prototype-based) in 3D, including necessary adaptations, training, rigorous benchmarking against a baseline, plus documentation and testing, requires a significant time investment suitable for a large project.)*

### Communication plan
I plan to dedicate approximately **40 hours per week** to this project (as stated in Availability). My communication strategy involves:
* Frequent asynchronous updates (aiming for daily or every other day) on progress, blockers, and findings via the BrainGlobe Zulip channel (`#cellfinder` stream) and relevant GitHub issues/PRs.
* Weekly synchronous video calls (e.g., Zoom/Google Meet) with mentors (@IgorTatarnikov, @alessandrofelder) for in-depth discussion, feedback, and planning.
* Prompt responses to mentor feedback and community questions.
* Maintaining clear commit messages and PR descriptions documenting changes.

## Personal statement

### Past experience
Talking about my past experience with open-source and programming, I have previously been a GSoC contributor for gprMax in 2023, where I developed a custom kernel to run gprMax on Jupyter notebooks, which previously only ran on the terminal. Following that, I was selected for the prestigious MITACS Globalink Research Internship, during which I worked on developing mentor mentee recommendation system for OSS. I was also a part of developing a custom RAG based LLM for our university, IISER Bhopal to ease access of information for the students. This is currently hosted at ask.iiserb.ac.in. Currently, I am working on developing state-of-the-art methods for detection and classification of Intracranial Hemorrhage (ICH) from Brain CT Scans. I'm also a recipient of a Student Innovation Grant (SiG) from our university to turn this project into a startup and currently we are at TRL 4 of the process.

### Motivation: why this project?
While looking for project that might interest me, I came across cellfinder's project of improving their classification algorithm. This project very closely aligns with the project that I am currently working on for my BS Thesis. In my project, I am working on Human Brain CT Volumes and in this project I'll be working on Mouse Brain 3D Volumes. So, it wouldn't be too difficult for me to adapt my thinking for this problem statement. Moreover, I realise how difficult and laborious of a process manual annotation is, be it for identifying hemorrhages in Brain CT, or detecting and classifying cells in a Mouse Brain Volume. Hence, I want to contribute in this project to fasten that process with my knowledge of classification based vision systems.

### Match: why you?
I believe my expertise in classification based models which I have learnt while working on my BS Thesis, makes me a good fit for this particular project. I also have Open Source Contribution experience during my last stint as a GSoC contributor in 2023. Both of these make me confident that I would be able to contribute greatly to a project of such importance.

### Availability
I am ready to devote 40 hours a week during my GSoC period. I am not taking part in any other internships or projects during this period.

## GSoC

### GSoC experience
From the program, I expect to build meaningful connections with researchers and developers from across the globe. I also aim to learn more deeply about different state-of-the-art architectures for image classification while building the new classification pipeline.

### Are you also applying to projects with other organisations in GSoC 2025?
No, I am applying only to this project.