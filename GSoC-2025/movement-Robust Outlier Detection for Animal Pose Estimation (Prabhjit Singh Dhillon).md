# movement:Robust Outlier Detection for Animal Pose Estimation (Prabhjit Singh Dhillon)

## Personal details
- **Full name**: Prabhjit Singh Dhillon
- **Email**: dhillonprabhjitsingh@gmail.com
- **GitHub username**: demoncoder-crypto
- **Zulip username**: Prabhjit Singh Dhilon
- **Location & time-zone**: UTC+5:30 (IST)
- **Contact**: +91‑9056431046
- **Code contribution**:
  - [Add support for downloading publicly available datasets](https://github.com/neuroinformatics-unit/movement/pull/515)
  - [Add trajectory complexity measures - implement straightness index](https://github.com/neuroinformatics-unit/movement/pull/514)
  - [Check log messages in tests](https://github.com/neuroinformatics-unit/movement/pull/512)
  - [Improve point trajectory estimation by aggregating across sources](https://github.com/neuroinformatics-unit/movement/pull/511)
    -[Add bidirectional option to filter_by_displacement](https://github.com/neuroinformatics-unit/movement/pull/531)
## Project proposal

### Synopsis
Animal pose estimation frameworks have advanced the study of animal behavior, yet their outputs can be marred by occasional inaccuracies such as keypoints that "jump" to implausible locations. This project proposes the design and implementation of a comprehensive outlier detection module for the movement package. By integrating methods based on temporal smoothness, pose plausibility, and multi-view consistency, this solution aims to automatically flag a high percentage of faulty keypoint predictions while maintaining low false positive rates, thereby significantly improving the quality control process in animal behavior research.

### Implementation timeline

#### Minimal set of deliverables:
- Temporal smoothness-based outlier detection algorithm:
    - Implement a two-stage approach for improved robustness:
        - **Stage 1 (Single-frame detection):** Implement *bidirectional* displacement analysis (checking t-1 <-> t and t <-> t+1). Utilize *adaptive thresholding* (e.g., based on Median Absolute Deviation - MAD) instead of fixed values. Offer both uni-directional and bi-directional checks as options.
        - **Stage 2 (Cluster/Oscillation detection):** Develop methods to identify continuous segments of errors and specialized patterns like *high-frequency oscillations* (position swaps).
    - Explore Procrustes analysis (`scipy.spatial.procrustes`) for supplementary shape consistency checks.
- Pose plausibility checks using hybrid data-driven and anatomical constraints:
    - Implement *adaptive PCA manifold learning*, potentially including *incremental updates* to allow model adaptation over time and exploring *behavior-specific subspaces*.
    - Integrate *kinematic chain validation* using species-specific constraints on joint angles and relative bone lengths.
- Multi-view consistency verification for setups with multiple camera views:
    - Implement robust geometric checks based on *epipolar geometry*, potentially using *RANSAC* for outlier rejection during fundamental matrix estimation.
    - Incorporate *uncertainty estimation* (e.g., weighting reprojection errors based on prediction confidence or calibration uncertainty).
    - Explore integrating temporal information via *temporal-spatial consistency filters* (e.g., Kalman filters combined with reprojection).
- Comprehensive API for integration with existing pose estimation workflows.
- Test suite using both synthetic and real-world datasets:
    - Include *synthetic error injection* (e.g., noise, jumps, swaps) for controlled evaluation.
    - Measure performance using standard metrics (*Precision, Recall, F1-score*).
- Documentation and examples demonstrating the module's usage.

#### Stretch goals:
- Adaptive thresholding mechanism that calibrates to different animal species
- Integration with the movement gallery for before-and-after trajectory visualization

#### Weekly timeline:
| Week | Tasks | Hours |
|------|-------|-------|
| Community Bonding | Literature review of current approaches, familiarization with movement codebase | 30 |
| 1 | Survey current pose estimation workflows, identify common outlier patterns | 30 |
| 2 | Design module architecture, finalize heuristics and integration points | 35 |
| 3 | Implement Stage 1 temporal filtering (bidirectional checks with adaptive MAD thresholds) | 35 |
| 4 | Test and document Stage 1 temporal filtering, implement oscillation detection, create sample data | 35 |
| 5 | Implement Stage 2 temporal filtering (cluster detection), refine based on tests | 35 |
| 6 | Implement PCA-based plausibility checks: <br> - Preprocess, train incremental/adaptive PCA model. <br> - Define plausibility score. <br> - Integrate kinematic constraints (joint angles, bone lengths). | 35 |
| 7 | Test and document PCA-based checks: <br> - Create/adapt sample data with plausible/implausible poses. <br> - Evaluate scoring mechanism. <br> - Write tests and documentation. | 30 |
| 8 | Implement multi-view consistency checks: <br> - Implement RANSAC-based 3D triangulation/epipolar validation. <br> - Incorporate uncertainty weighting. <br> - Define consistency threshold. | 30 |
| 9 | Test and document multi-view checks: <br> - Create/adapt multi-view sample data. <br> - Evaluate consistency thresholds. <br> - Write tests and documentation. | 30 |
| 10 | Complete API development integrating all heuristics, optimize based on benchmarks | 30 |
| 11 | Refine algorithms based on feedback, finalize user guides and API documentation | 25 |
| 12 | Package the module, create example notebooks, final testing and polishing | 25 |

### Anticipated Challenges and Proposed Solutions
Based on preliminary analysis and common issues in pose estimation, we anticipate the following challenges and propose corresponding mitigation strategies:
1.  **Adaptive Threshold Calibration:** Outlier thresholds may need adjustment based on behavior, species, or experimental conditions. 
    *   **Solution:** Implement session-specific baseline calculations (e.g., using MAD) and potentially explore velocity-dependent adjustments to automatically tune thresholds.
2.  **Novel Behavior Handling:** Pre-trained PCA models might incorrectly flag poses from behaviors not seen during training.
    *   **Solution:** Maintain behavior-specific PCA subspaces where feasible. Implement mechanisms for handling 'Unknown' poses, possibly queuing them for manual review or using active learning loops to update models.
3.  **Calibration Error Mitigation:** Inaccurate camera calibration can degrade multi-view consistency checks.
    *   **Solution:** While robust calibration is external, the multi-view checks will incorporate uncertainty. Explore possibilities for online calibration refinement (e.g., bundle adjustment using detected keypoints) as a potential extension if initial checks prove too sensitive to minor calibration drift.

### Communication plan
I plan to communicate with my mentors (@niksirbi and @sfmig) through:
- Weekly video calls to discuss progress and address challenges
- Regular updates on the Zulip chat for day-to-day questions
- GitHub PR reviews for code feedback
- Asynchronous communication through email when needed

## Personal statement

### Past experience
I hold a Bachelor's degree with a dual major in Computer Science and Applied Mathematics (CGPA: 3.7/4.0) from San Jose State University. I've worked as a Machine Learning Engineer until December 2024, where I built scalable machine learning models. I have extensive experience in Python, C++, JavaScript, and deep learning frameworks (PyTorch, TensorFlow). I've contributed to high-impact open-source projects such as Google DeepMind OpenSpiel, DeepMind Torax, DeepMind Mujoco, google generative ai js/python and fortran libraries, and  most recently to the movement package through several pull requests.

(https://github.com/demoncoder-crypto/Deeplense_gravitational-Images)
My Highlight project - Deeplense Gravitational Imaging - This project implements and evaluates deep learning models for classifying simulated gravitational lensing images into three categories: no substructure (no_sub), Cold Dark Matter substructure (cdm), and Axion vortex substructure (axion). The core methodology involves comparing a standard deep learning architecture (ResNet-18) against a custom Convolutional Neural Network (CNN) whose architecture is specifically inspired by gravitational lensing physics.

- Key Components: Data Handling: A robust pipeline loads and preprocesses .npy image data (64x64 pixels), handling the unique data structure of the 'axion' class. Data is split into training, validation, and test sets (80:10:10), with standard augmentations (rotations, flips) and normalization applied. PyTorch Datasets and DataLoaders ensure efficient batching.
- Model Architectures: Baseline Model: A ResNet-18 architecture, adapted for single-channel grayscale input, serves as a standard deep learning benchmark.
- Physics-Inspired CNN: A custom CNN architecture featuring elements chosen to potentially better capture lensing features, such as varying kernel sizes (5x5 to detect arc-like structures) and concatenated global average and max pooling to summarize spatial information effectively.
- Ensemble Model: Combines the predictions (probabilities) of the ResNet and Physics-Inspired CNN, weighted potentially by their validation performance, aiming for improved accuracy and robustness.
- Training: Models are trained using a standard supervised learning procedure with the Adam optimizer, Cross-Entropy loss, and a learning rate scheduler (ReduceLROnPlateau) based on validation accuracy. The best performing model weights during training (based on validation accuracy) are saved.

### Motivation: why this project?
Animal behavior research increasingly depends on accurate pose estimation, yet current frameworks often produce inaccuracies that can lead to erroneous conclusions or require labor-intensive manual corrections. I'm motivated to tackle this challenge because it combines my technical expertise in machine learning and signal processing with a meaningful application in scientific research. Developing a robust outlier detection system will significantly enhance data quality and research reproducibility by automating the identification of errors, which is especially critical for large-scale studies.

In addition to addressing these technical challenges, I have a keen interest in neuroscience. I aspire to pursue higher education and eventually work in an AI biology lab (hopefully this), and this project represents a unique opportunity to bridge my current skills with my long-term career goals. By working on this project, I will gain hands-on experience with advanced computational techniques, explore innovative approaches to biological data analysis, and establish a solid foundation for future studies in neuroscience. This integration of technical and scientific inquiry not only advances animal behavior research but also sets a clear path for my future endeavors in AI-driven biological research.

### Match: why you?
My unique combination of academic background, industry experience, and open-source contributions makes me well-suited for this project. My dual major in Computer Science and Applied Mathematics provides the theoretical foundation needed for implementing statistical methods like PCA and Kalman filters. My experience as a Machine Learning Engineer has equipped me with practical skills in developing scalable, production-quality code. Additionally, my prior contributions to the movement package demonstrate my familiarity with the codebase and my ability to implement features that meet the project's standards.

### Availability
I will be dedicating 30-35 hours per week to this project throughout the GSoC period, for a total of approximately 350 hours. I have no conflicting commitments during this time and have arranged my schedule to ensure full availability for this project.

## GSoC

### GSoC experience
From the GSoC program, I expect to gain valuable experience in collaborative open-source development, working with domain experts, and creating software that has a real impact on scientific research. I look forward to improving my skills in Python, testing methodologies, and documentation practices while contributing to the neuroinformatics community.

### Are you also applying to projects with other organisations in GSoC 2025?
No, this is the only project I am applying to.