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


## **Project Proposal**

### **Synopsis**  
This project aims to calibrate confidence scores produced by pose estimation frameworks. Accurate confidence calibration ensures fair comparisons between frameworks and improves downstream tasks that rely on confidence scores, such as filtering low-confidence predictions.

### **Why Is It Important?**  
- **Fair Evaluation:** Enables objective benchmarking across different pose estimation frameworks.  
- **Improved Performance:** Enhances confidence-based decision-making for better downstream task outcomes.  
- **Open-Source Impact:** Provides reproducible tools and standardized evaluation practices, benefiting the open-source community.  

### **Goals**  
Implement a Python function for calibrating confidence scores produced by various pose estimation frameworks. The function will allow users to specify calibration schemes via parameters and will be accompanied by a benchmark to assess the effectiveness of the calibration methods.

### **Deliverables**  

**Minimum:**  
- Implement the method proposed in keypoint-moseq, fitting a regression line to the log(confidence) vs. log(error) pairs obtained from annotations.  
- Implement functionality to directly fit ground truth keypoint datasets and corresponding confidence scores.  
- Implement a calibration scheme based on error distance thresholds to determine prediction success for confidence calculation.
- Implement a calibration scheme based on error to compute new confidence scores (and experiment with multiple error-to-confidence mapping functions).
- Test all added functionalities and write documentation for the new features.  
- Provide an example use case document from a sample dataset.

**Extended:**  
- Design a benchmark function that uses basic datasets and existing confidence-based functionalities to evaluate the quality of confidence calibration methods based on the performance of downstream tasks.   
- Conduct experiments based on the benchmark function to identify the optimal new confidence calibration scheme or highlight the strengths and weaknesses of each method. 

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

    I hope to engage in computational neuroscience research in the future and apply my data science skills to this field. During my undergraduate laboratory internship, I was involved in studies related to brain science and animal behavior. I believe that the *movement* project is very helpful for such research.
- **Match: why you?**

    There is currently no widely accepted best method for calibrating confidence scores in regression models. I hope to leverage my data analysis skills to design a benchmark that evaluates the strengths and weaknesses of the various calibration methods we will implement, aiming to identify an optimal approach or provide simple guidelines for selecting the appropriate method. I have won awards (Top 1-2%) in mathematical modeling competitions such as MCM/ICM and CUMCM, which makes me particularly skilled in this type of work.
- **Availability**

    From June to September, I have no scheduled coursework, allowing me to dedicate ample time to successfully complete the project with high quality.

## GSoC

- **GSoC experience**

    I hope to gain experience in open-source collaboration, understand the development workflow, and deepen my knowledge in the relevant field.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am solely focused on the movement project and am not applying to any other organizations for GSoC 2025.
