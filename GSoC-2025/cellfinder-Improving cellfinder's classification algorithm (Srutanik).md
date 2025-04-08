# cellfinder: Improving cellfinder's classification algorithm (Srutanik Bhaduri)

## Personal details
- **Full name:** Srutanik Bhaduri
- **Email:** srutanik.bhaduri02@gmail.com
- **GitHub username:** srutanik
- **Zulip username:** Srutanik Bhaduri
- **Location & time-zone:** Bhopal, Madhya Pradesh, India (UTC+5:30)
- **Personal website / project portfolio:** 
  * GitHub: [srutanik](https://github.com/srutanik)
  * LinkedIn: [Srutanik Bhaduri](https://www.linkedin.com/in/srutanik-bhaduri-3a9a691b9/)

- **Code contribution:**
    [https://github.com/brainglobe/cellfinder/pull/513](https://github.com/brainglobe/cellfinder/pull/513)
    This pull request addresses the issue of clarifying and refactoring of the API of the detect and classify module of cellfinder. This is not a final PR since it has a couple of breaking changes that need to be adressed in future commits.
- **Proposal discussion link:**
    https://github.com/neuroinformatics-unit/gsoc/pull/83

## Project proposal

### Synopsis

1. **What is the project about?** 
   
   This project is about improving `cellfinder`'s old 3D ResNet-50 based classification algorithm to solve the binary classification problem of "cell" or "no cell" from all the detected artefacts within the 3D Volume of the Mouse Brain. It involves replacing/augmenting the current model with modern deep learning architectures.

2. **Why is it important and how would the Open-Source Community benefit from this project?** 
   
   From my limited knowledge about neuroscience, I realize that manual  cell labelling is a very hectic task from a scientists’    perspective. So automatic and accurate detection and  classification using Deep Learning based systems become   important so that more time can be devoted to post analysis.

3. **What are the deliverables?** 
   
   Considering this as a large (350hr) project, the following are the main deliverables:

   1. **Models:** Python implementations integrated within the `cellfinder` framework:
      * **3D CNN + Attention Gate:** Implementation of a modern 3D CNN backbone (e.g., EfficientNet3D) combined with an Attention Gate mechanism. The goal is to enhance relevant spatial feature extraction for potentially improved classification accuracy compared to the baseline ResNet-50. ([Ref Paper Link](https://arxiv.org/abs/1808.08114))
      * **3D WaveMix Adaptation:** Implementation adapting the WaveMix concept, using 3D Discrete Wavelet Transforms (DWT) for multi-scale context modeling as a potentially more computationally efficient alternative to dense attention mechanisms. ([Ref Paper Link](https://arxiv.org/abs/2205.14375))
      * **(Stretch Goal) 3D PIP-Net Adaptation:** Implementation adapting the Patch-based Intuitive Prototypes Network (PIP-Net) for 3D volumetric data. This aims to provide interpretable classification by learning representative 3D prototypical patches and utilizing a sparse scoring-sheet reasoning mechanism. ([Ref Paper Link](https://openaccess.thecvf.com/content/CVPR2023/papers/Nauta_PIP-Net_Patch-Based_Intuitive_Prototypes_for_Interpretable_Image_Classification_CVPR_2023_paper.pdf))
      * **(Stretch Goal) Ensemble Model:** Implementation of an ensemble method (e.g., weighted averaging of predictions) combining the outputs of the best-performing newly implemented models (e.g., Attention-based + WaveMix) to potentially maximize overall classification accuracy and robustness.

   2. **Analysis, Documentation, and Tests:**
      * **Comparative Analysis:** Analysis of the implemented architectures against the ResNet-50 baseline, using standard classification metrics (F1 score, sensitivity/recall, specificity, accuracy, AUC, loss curves) and computational performance metrics (inference time, training time, GPU memory usage in flops).
      * **Explainable Model Outputs:** Implementation of Grad-CAM and Guided Grad-CAM techniques to provide visual explanations of model decisions, highlighting regions in the 3D volumes that contributed most to classification outcomes with the help of saliency maps.
      ([Ref Paper Link](https://arxiv.org/abs/1610.02391))
      * **Documentation & Blog Post:** Comprehensive documentation integrated into `cellfinder`'s existing documentation, detailing the new architectures, the rationale for their use, instructions for usage (training, inference), configuration options, and a summary of the comparative analysis findings including advantages and disadvantages of each technique in the `cellfinder` context. A blog post will be written to communicate the project's goals, methods, and key results.
      * **Testing:** Robust test suite including unit tests for core functions within the new model implementations (e.g., custom layers, loss functions) and integration tests to ensure the new models integrate correctly with `cellfinder`'s existing data loading, preprocessing, training, and inference pipelines.

### Implementation Timeline

* **Minimal Set of Deliverables:**
  1. Model Implementations: **3D CNN + Attention Gate** and **3D WaveMix Adaptation** (first two bullet points under deliverable 1).
  2. Analysis, Documentation, and Tests: All items under deliverable 2 covering the implemented models and baseline, including Grad-CAM/Guided Grad-CAM implementations.

* **Stretch Goals:**
  1. Model Implementation: **3D PIP-Net Adaptation** (third bullet point under deliverable 1).
  2. Model Implementation: **Ensemble Model** (fourth bullet point under deliverable 1).

* **Weekly Timeline** (Approx. 25-30 hours/week)

| **Dates** | **GSoC Phase** | **Key Tasks & Milestones** |
|-----------|----------------|----------------------------|
| May 8 – June 1 | **Community Bonding** | - Perfrom  trials with architecture types  (backbones, attention type, WaveMix specifics) after discussion with mentors.<br>- Deep dive into `cellfinder` classification codebase & data handling.<br>- Set up environment & baseline ResNet benchmarking framework. |
| June 2 – June 22 | **Weeks 1-3** | - Implement **3D CNN + Attention Gate** model.<br>- Integrate into `cellfinder`.<br>- Develop/adapt training script. Unit tests. Initial training/debugging. |
| June 23 – July 6 | **Weeks 4-5** | - Tune & rigorously train Attention model.<br>- **Benchmark #1:** Compare Attention based CNN vs. ResNet-50 (all metrics).<br>- Begin implementing Grad-CAM and Guided Grad-CAM visualization techniques.<br>- Analyze results, start documentation/blog draft. |
| July 7 – July 13 | **Week 6** | - Finalize Attention model benchmarking & analysis.<br>- Complete Grad-CAM implementation for the Attention model .<br>- Plan detailed implementation for 3D WaveMix adaptation. |
| July 14 – July 18 | **Midterm Evaluation** | - Submit evaluation. Discuss progress & WaveMix plan. |
| July 19 – Aug 10 | **Weeks 7-9** | - Implement **3D WaveMix adaptation**.<br>- Integrate into `cellfinder`. Unit tests. Initial training/debugging.<br>- Extend Grad-CAM implementation to work with WaveMix architecture. |
| Aug 11 – Aug 24 | **Weeks 10-11** | - Tune & rigorously train/evaluate WaveMix.<br>- **Benchmark #2:** Compare WaveMix vs. ResNet and Attention based CNN.<br>- Finalize Guided Grad-CAM implementation for all models.<br>- **Begin Stretch Goals:** Start PIP-Net/Ensemble (more focus on Ensemble Techniques) if time permits.<br>- Write integration tests for both models. |
| Aug 25 – Sep 1 | **Week 12 (Final)** | - **Finalize Minimal Deliverables:** Complete code, benchmarks, tests, documentation, blog post for Attention & WaveMix models and explainability techniques.<br>- Finalize stretch goals if undertaken. Prepare code PRs. Submit final work. |

### Project Length
Large (350 hours)

*(Justification: Implementing and thoroughly evaluating two distinct and potentially complex deep learning architectures (Attention-based and WaveMix-based) in 3D, including necessary adaptations, training, rigorous benchmarking against a baseline, plus explainability techniques, documentation and testing, requires a significant time investment suitable for a large project.)*

### Communication plan
I plan to dedicate approximately **25-30 hours per week** to this project (as stated in Availability). My communication strategy involves:
* Frequent asynchronous updates (aiming for daily or every other day) on progress, blockers, and findings via the BrainGlobe Zulip channel and relevant GitHub issues/PRs.
* Weekly video calls (e.g., Zoom/Google Meet) with mentors (@IgorTatarnikov, @alessandrofelder) for in-depth discussion, feedback, and planning.
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
I am ready to devote 25-30 hours a week during my GSoC period. I am not taking part in any other internships or projects during this period.

## GSoC

### GSoC experience
From the program, I expect to build meaningful connections with researchers and developers from across the globe. I also aim to learn more deeply about different state-of-the-art architectures for image classification while building the new classification pipeline.

### Are you also applying to projects with other organisations in GSoC 2025?
No, I am applying only to this project.

***

## Mini-proposal for working on API of the detect and classify module

Apart from the work plan in the proposal described above, I would like to take on an additional work during this period of time. That includes finishing up my work on refactoring and clarifying the API as stated in my PR (in **Code Contribution**).

That seems like a very interesting problem from a software point-of-view and as suggested by @alessandrofelder in his review, I would love to devote some time to this as well. 
