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

- **Proposal discussion link**: [Link to the PR where this proposal was discussed]

## Project proposal

### Synopsis
Animal pose estimation frameworks have advanced the study of animal behavior, yet their outputs can be marred by occasional inaccuracies such as keypoints that "jump" to implausible locations. This project proposes the design and implementation of a comprehensive outlier detection module for the movement package. By integrating methods based on temporal smoothness, pose plausibility, and multi-view consistency, this solution will automatically flag and help correct erroneous keypoint predictions, thereby improving the quality control process in animal behavior research.

### Implementation timeline

#### Minimal set of deliverables:
- Temporal smoothness-based outlier detection algorithm
- Pose plausibility checks using PCA-based methods
- Multi-view consistency verification for setups with multiple camera views
- Comprehensive API for integration with existing pose estimation workflows
- Test suite with synthetic and real-world datasets
- Documentation and examples demonstrating the module's usage

#### Stretch goals:
- Interactive visualization tools for inspecting and correcting outliers
- Adaptive thresholding mechanism that calibrates to different animal species
- Integration with the movement gallery for before-and-after trajectory visualization

#### Weekly timeline:
| Week | Tasks | Hours |
|------|-------|-------|
| Community Bonding | Literature review of current approaches, familiarization with movement codebase | 30 |
| 1 | Survey current pose estimation workflows, identify common outlier patterns | 30 |
| 2 | Design module architecture, finalize heuristics and integration points | 35 |
| 3 | Prototype temporal filtering component | 35 |
| 4 | Prototype PCA-based plausibility checks | 35 |
| 5 | Develop multi-view consistency checks | 35 |
| 6 | Complete API development with all three detection heuristics | 35 |
| 7 | Write comprehensive tests and create sample datasets | 30 |
| 8 | Run benchmarks on datasets, analyze detection accuracy | 30 |
| 9 | Refine algorithms based on testing feedback | 30 |
| 10 | Optimize for performance and edge cases | 30 |
| 11 | Complete user guides and API documentation | 25 |
| 12 | Package the module, create example notebooks, final testing | 25 |

### Communication plan
I plan to communicate with my mentors (@niksirbi and @sfmig) through:
- Weekly video calls to discuss progress and address challenges
- Regular updates on the Zulip chat for day-to-day questions
- GitHub PR reviews for code feedback
- Asynchronous communication through email when needed

## Personal statement

### Past experience
I hold a Bachelor's degree with a dual major in Computer Science and Applied Mathematics (CGPA: 3.7/4.0) from San Jose State University. I've worked as a Machine Learning Engineer until December 2024, where I built scalable machine learning models. I have extensive experience in Python, C++, JavaScript, and deep learning frameworks (PyTorch, TensorFlow). I've contributed to high-impact open-source projects such as DeepMind OpenSpiel and DeepMind TORAX, and most recently to the movement package through several pull requests.

### Motivation: why this project?
Animal behavior research is a critical field that increasingly relies on accurate pose estimation. The current limitations in detecting outliers can lead to erroneous conclusions or require excessive manual work. I'm motivated to tackle this challenge because it combines my technical skills in machine learning and signal processing with a meaningful application in scientific research. Creating a robust outlier detection system will significantly enhance data quality and research reproducibility in this field.

### Match: why you?
My unique combination of academic background, industry experience, and open-source contributions makes me well-suited for this project. My dual major in Computer Science and Applied Mathematics provides the theoretical foundation needed for implementing statistical methods like PCA and Kalman filters. My experience as a Machine Learning Engineer has equipped me with practical skills in developing scalable, production-quality code. Additionally, my prior contributions to the movement package demonstrate my familiarity with the codebase and my ability to implement features that meet the project's standards.

### Availability
I will be dedicating 30-35 hours per week to this project throughout the GSoC period, for a total of approximately 350 hours. I have no conflicting commitments during this time and have arranged my schedule to ensure full availability for this project.

## GSoC

### GSoC experience
From the GSoC program, I expect to gain valuable experience in collaborative open-source development, working with domain experts, and creating software that has a real impact on scientific research. I look forward to improving my skills in Python, testing methodologies, and documentation practices while contributing to the neuroinformatics community.

### Are you also applying to projects with other organisations in GSoC 2025?
No, I am solely focusing on this project with the Neuroinformatics Unit as it aligns perfectly with my skills and interests. 