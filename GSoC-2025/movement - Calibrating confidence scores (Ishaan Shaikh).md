## Project title: movement: Calibrating Confidence Scores (Ishaan Shaikh)

## Personal details
- **Full name**: Ishaan Shaikh  
- **Email**: ishaan0132@gmail.com  
- **GitHub username**: Ishaan0132  
- **Zulip username**: Ishaan Shaikh  
- **Location & time-zone**: India, Indian Standard Time (GMT+5:30)  
- **Personal website / project portfolio**: https://ishaan0132.github.io/  
- **Code contribution**:  

    1. [Ensure dataset attributes are not set to None](https://github.com/neuroinformatics-unit/movement/pull/456)  
    2. [Correct confidence_array shape in from_numpy example docstring](https://github.com/neuroinformatics-unit/movement/pull/492)  
    3. [Set print_report to False by default in filtering functions](https://github.com/neuroinformatics-unit/movement/pull/493)

- **Proposal discussion link**: https://github.com/neuroinformatics-unit/gsoc/pull/11

## Project proposal 

- **Synopsis**

    This project focuses on **calibrating confidence scores** in pose estimation to ensure they accurately **reflect the reliability** of detected keypoints. Currently, these confidence scores are often misleading, making it difficult to filter low-confidence predictions, and interpret results effectively. Improving confidence calibration will enhance the **usability**, and **trustworthiness** of pose estimation.

    The goal is to **implement a confidence calibration method** for frameworks like DeepLabCut, SLEAP, LightningPose, and Anipose. By improving confidence calibration, this project will help researchers and developers **compare pose estimation results** more accurately, making these frameworks more reliable and widely applicable in open-source research and real-world applications.
- **Implementation timeline**

    **Minimal Deliverables**  

    - Implement a **confidence calibration method** for at least one pose estimation framework (DeepLabCut, SLEAP, LightningPose, or Anipose). Since confidence score computation varies across frameworks, comparing 2-3 calibration techniques can help determine the most robust and adaptable approach.
    - Develop **unit tests** to validate calibration performance.  
    - Create **documentation** explaining the calibration method and integration process.  
    - Provide an **example use case** in the movement gallery.  
    - Write a **blog post** summarizing the implementation, challenges, and findings to engage the open-source community.  

    **Stretch Goals (If Time Allows)**  
    - Extend calibration support to **multiple** pose estimation frameworks instead of just one.   
    - Improve **efficiency and scalability** of the calibration process for larger datasets by using **parallelization** and leveraging high-confidence keypoints as pseudo-ground truth.
    - Explore the **impact** of confidence calibration on **downstream tasks** by analyzing how calibration affects subsequent processing such as smoothing movement trajectories or improving behavior segmentation and assessing performance changes like improved tracking accuracy and reduced false positives/negatives.


**Weekly Timeline:**  

| **Week & Dates** | **Tasks & Deliverables** |
|------------------|-------------------------|
| **Community Bonding (May 8 – June 1)** | Set up the development environment, finalize a framework for implementing calibration choosing between DLC or SLEAP, as they are the most widely used in movement, research and try out existing calibration techniques, and develop a detailed implementation plan. |
| **Week 1 & 2 (June 2 – June 15)** | Implement data preprocessing for confidence scores and keypoint errors. This includes cleaning raw data, normalizing and scaling confidence scores for consistency, aligning keypoint detections with ground truth labels, and applying transformations. Begin experimenting with multiple calibration techniques and discuss evaluation metrics with the mentor. |
| **Week 3 & 4 (June 16 – June 29)** | Start implementing the chosen calibration method. Evaluate its effectiveness and refine it based on initial results. Integrate unit tests to validate correctness at each step. Begin benchmarking calibrated vs. uncalibrated confidence scores. |
| **Week 5 & 6 (June 30 – July 13) (Midterm Evaluation)** | Integrate the selected calibration method into movement. For usability, write detailed documentation and implement integration tests to ensure easy adoption by other developers. For efficiency, apply batch processing where appropriate. Submit midterm evaluation by July 18. |
| **Week 7 & 8 (July 14 – July 27)** | Present side-by-side comparisons of pose outputs before and after calibration along with confidence histograms to demonstrate improvements in score distributions. Compute metrics such as Expected Calibration Error, **analyze confidence vs accuracy** to show that calibrated scores better reflect true accuracy. Ensure results are well-documented with sample code. |
| **Week 9 (July 28 – Aug 3) (Buffer Period)** | Address mentor feedback, fix bugs, and optimize performance to ensure a robust implementation. |
| **Week 10 & 11 (Aug 4 – Aug 17)** | Finalize all code, improve maintainability, and ensure proper integration into movement. Conduct additional small-scale evaluations if necessary. Complete any remaining documentation. |
| **Week 12 (Aug 18 – Aug 25) (Final Submission)** | Submit final project, mentor evaluation, and write a blog post summarizing implementation and findings. |
| **Post GSoC (After Aug 25)** | Continue contributing to **movement**, exploring broader applications in movement analysis, and engaging with the community for future development. |


- **Communication plan**

    I plan to maintain regular communication with my mentors to ensure steady progress and alignment with project goals. I will **share daily updates** on my progress, challenges, and next steps through **Zulip** to keep discussions documented. Additionally, planning will be discussed in the bi-weekly **community calls**. Separate **Zoom meetings** will be scheduled as needed for in-depth discussions and problem-solving.

## Personal statement

- **Past experience** 

    I have been actively involved in machine learning, with experience spanning computer vision, model optimization, and dataset handling. I have worked on projects requiring **fine-tuning** deep learning models, **optimizing** data pipelines, and integrating machine learning for security applications, such as **anomaly detection** in network monitoring.

    One of my projects, **Virtual Try-On**, required implementing pose detection to track body keypoints and improve alignment accuracy. This introduced me to **challenges in keypoint localization and prediction reliability**, strengthening my understanding of pose estimation techniques.

- **Motivation: why this project?**

    Pose estimation is widely used in fields like biomechanics, robotics, and behavior analysis, but uncalibrated confidence scores can lead to inaccurate interpretations. This project excites me because it tackles a fundamental challenge in pose estimation—calibrating confidence scores to better reflect actual prediction reliability. Having worked on pose estimation in my Virtual Try-On project, I have seen how inconsistent keypoint predictions impact accuracy and understood the need for more robust confidence measures.

    This project will improve confidence calibration in pose estimation, making models more reliable and easier to interpret. By enhancing movement’s capabilities, it will help researchers make better use of keypoint data while encouraging broader adoption and community contributions.

- **Match: why you?**

    I have a strong background in computer vision, pose estimation, and deep learning, with experience in Python, OpenCV, and PyTorch. My work in pose detection and keypoint tracking, particularly in my Virtual Try-On project, exposed me to uncertainties in keypoint predictions and methods to improve alignment accuracy.


- **Availability**

    In the coding period, I will work for at least 5 to 6 hours or even more if required everyday until the completion of the project. I have a 2-month long vacation after May 17 and no other commitments in hand so major part of the project will be implemented in this duration.

## GSoC

- **GSoC experience**

    No, I have not participated in GSoC before. 

    Through GSoC, I hope to gain hands-on experience in open-source collaboration, refine my implementation skills, and contributing a practical, well-documented solution that benefits the community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am applying exclusively to NIU for GSoC 2025 because this project aligns closely with my interests in pose estimation, and machine learning.