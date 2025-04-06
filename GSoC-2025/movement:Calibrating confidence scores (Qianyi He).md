## Movement: Calibrating Confidence Scores (Qianyi He)

## Personal details
- **Full name**: Qianyi He
- **Email**: heqianyi926@uchicago.edu
- **GitHub username**: Angelneer926
- **Zulip username**: Qianyi He
- **Location & time-zone**: Chicago, UTC-6
- **Personal website / project portfolio**: Data Interaction https://github.com/Angelneer926/Data_interaction; Generative Model for Synthetic Histopathological Data Augmentation https://github.com/Angelneer926/Machine_Learning2/tree/main/Project
- **Code contribution**
https://github.com/neuroinformatics-unit/movement/pull/507

- **Proposal discussion link**
https://github.com/neuroinformatics-unit/gsoc/pull/14

## **Project Proposal**

### **Synopsis**  
This project aims to calibrate confidence scores produced by pose estimation frameworks. Accurate confidence calibration ensures fair comparisons between frameworks and improves downstream tasks that rely on confidence scores, such as filtering low-confidence predictions.

### **Why Is It Important?**  
- **Fair Evaluation:** Enables objective benchmarking across different pose estimation frameworks.  
- **Improved Performance:** Enhances confidence-based decision-making for better downstream task outcomes.  
- **Open-Source Impact:** Provides reproducible tools and standardized evaluation practices, benefiting the open-source community.  

### **Goals**  
Develop a flexible calibration module for confidence scores from pose estimation models, supporting multiple calibration techniques configurable by the user.
Additionally, create a benchmarking framework to evaluate and compare these methods, aiming to offer practical guidance on choosing the right calibration strategy.

**Minimum:**

**Regression-based Calibration:**  
Fit a regression line between log(confidence) and log(error) using ground truth keypoints, following the keypoint-moseq approach.

**Direct Ground Truth Input:**  
Support calibration using raw keypoint data (e.g. from sensors), eliminating the need for manual annotation.

**Threshold-based Classification:**  
Define prediction success by error thresholds and calibrate confidence as the probability of success.

**Error-to-Confidence Mapping:**  
Apply functions (e.g. inverse, exponential, ReLU) to map error distances to calibrated confidence scores in [0,1].

**Tests & Example:**  
Test all methods, document them, and provide a sample use case.

**Benchmarking Framework:**  
Build a benchmark to evaluate calibration quality across methods using standard metrics and downstream task performance.

**Extended:**

**Experimental Comparison:**  
Run experiments to identify the most effective calibration strategies and summarize trade-offs.

### **Implementation Timeline**  
(*~25-30 hours per week*)  

| **Week**         | **Tasks**                                           |
|------------------|----------------------------------------------------|
| **Community Bonding** | Review existing confidence-related functions and datasets, design benchmark criteria, and explore error-to-confidence mapping methods. |
| **Week 1-2**      | Implement and validate the log-log fitting method from keypoint-moseq. |
| **Week 3**        | Extend to support ground-truth datasets with confidence scores. |
| **Week 4-6**      | Implement a calibration method based on error distance thresholds and test all the implemented functionalities. |
| **Week 7-8**      | Implement and evaluate multiple error-to-confidence mapping methods. |
| **Week 9-10**     | Design and implement the benchmark function for evaluation. |
| **Week 11**       | Conduct benchmark experiments and analyze calibration performance. |
| **Week 12-13**    | Summarize results, finalize documentation, and prepare the final report. |

### **Communication Plan**  
I will communicate with my mentor via Zulip chat for daily questions and discussions, with weekly Zoom meetings for progress updates and addressing challenges.

## Personal statement

- **Past experienc.** 

    I am currently a Master's student in Data Science at the University of Chicago. Previously, I worked at ByteDance as a data analyst, where I gained experience in machine learning and data processing. I have also studied data interaction techniques and developed several web pages to better present data. Additionally, I have conducted research on *real-time spatial positioning and attitude recognition based on Kalman filtering*, giving me a certain level of understanding of pose estimation frameworks. Although I have extensive programming experience, I am new to open source. The *movement* project is my first participation in the open-source community, where I submitted a pull request to implement a feature requested in an issue.
- **Motivation: why this project?**

    I hope to engage in computational neuroscience research in the future and apply my data science skills to this field. During my undergraduate laboratory internship, I was involved in studies related to brain science and animal behavior. I am mainly involved in some research exploring the connection between neural activity and animal behavior. I think the movement library can help us get more accurate animal behavior data and help this kind of research.
- **Match: why you?**

    There is currently no widely accepted best method for calibrating confidence scores in regression models. I hope to leverage my data analysis skills to design a benchmark that evaluates the strengths and weaknesses of the various calibration methods we will implement, aiming to identify an optimal approach or provide simple guidelines for selecting the appropriate method. I have won awards (Top 1-2%) in mathematical modeling competitions such as MCM/ICM and CUMCM, which makes me particularly skilled in this type of work.
- **Availability**

    From June to September, I have no scheduled coursework, allowing me to dedicate ample time to successfully complete the project with high quality.

## GSoC

- **GSoC experience**

    I hope to gain experience in open-source collaboration, understand the development workflow, and deepen my knowledge in the relevant field.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am solely focused on the movement project and am not applying to any other organizations for GSoC 2025.
