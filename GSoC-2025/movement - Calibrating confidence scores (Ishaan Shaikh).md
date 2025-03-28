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

- **Proposal discussion link**:

     

## Project proposal 

- **Synopsis**

    This project focuses on **calibrating confidence scores** in pose estimation to ensure they accurately **reflect the reliability** of detected keypoints. Currently, these confidence scores are often misleading, making it difficult to filter low-confidence predictions, and interpret results effectively. Improving confidence calibration will enhance the **usability**, and **trustworthiness** of pose estimation.

    The goal is to **implement a confidence calibration method** for frameworks like DeepLabCut, SLEAP, LightningPose, and Anipose. By improving confidence calibration, this project will help researchers and developers **compare pose estimation results** more accurately, making these frameworks more reliable and widely applicable in open-source research and real-world applications.
- **Implementation timeline**

    **Minimal Deliverables**  

    - Implement a **confidence calibration method** for at least one pose estimation framework (DeepLabCut, SLEAP, LightningPose, or Anipose).  
    - Develop **unit tests** to validate calibration performance.  
    - Create **documentation** explaining the calibration method and integration process.  
    - Provide an **example use case** in the movement gallery.  

    **Stretch Goals (If Time Allows)**  
    - Extend calibration support to **multiple** pose estimation frameworks instead of just one.   
    - Improve **efficiency and scalability** of the calibration process for larger datasets.  
    - Explore the **impact** of confidence calibration on **downstream tasks**, such as behavior analysis.

**Weekly Timeline:**  

| **Week** | **Dates** | **Tasks & Deliverables** | **Hours/Week** |
|----------|----------|-------------------------|---------------|
| **Up Till May 8** | Until May 8 | Familiarize with movement codebase, explore confidence scores in pose estimation frameworks, fix minor issues, discuss project details with mentor, and review method used in keypoint-moseq. | 10-15 |
| **Community Bonding** | May 8 – June 1 | Set up the development environment, Finalize a framework for implementing calibration, choosing between DLC or SLEAP, as they are the most widely used in the movement, research and try out existing calibration techniques, and develop a detailed implementation plan. | 10-15 |
| **Week 1 & 2** | June 2 – June 15 | Implement data preprocessing pipeline for confidence scores and keypoint errors. Start regression-based calibration and discuss evaluation metrics with mentor. | 25-30 |
| **Week 3 & 4** | June 16 – June 29 | Validate and refine regression-based calibration, implement logistic regression calibration, and develop unit tests. Begin benchmarking calibrated vs. uncalibrated confidence scores. | 25-30 |
| **Week 5 & 6 (Midterm Evaluation)** | June 30 – July 13 | Start integrating the calibration method into movement. Ensure usability and efficiency. Submit midterm evaluation by July 18. | 30-35 |
| **Week 7 & 8** | July 14 – July 27 | Implement documentation and develop an example use case for movement gallery demonstrating the impact of confidence calibration. | 30-35 |
| **Week 9 (Buffer Period)** | July 28 – Aug 3 | Address mentor feedback, fix bugs, and optimize performance to ensure a robust implementation. | 25-30 |
| **Week 10 & 11** | Aug 4 – Aug 17 | Finalize tests, ensure the code is maintainable and well-integrated, and complete any outstanding documentation or usability improvements. | 25-30 |
| **Week 12 (Final Submission)** | Aug 18 – Aug 25 | Submit final project, mentor evaluation, and write a blog post summarizing implementation and findings. | 20-25 |
| **Post GSoC** | After Aug 25 | Continue contributing to **movement**, improving calibration methods, and exploring research applications in pose estimation confidence calibration. | N/A |

- **Communication plan**

    I plan to maintain regular communication with my mentors to ensure steady progress and alignment with project goals. I will **provide weekly updates** on my progress, challenges, and next steps through **Zulip** to keep discussions documented. Additionally, in-depth feedback, troubleshooting, and planning will be discussed in the bi-weekly **community calls**. For quick questions or clarifications, I will use **Zulip** and **GitHub issues**.

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

    In the coding period, I will work for at least 4 to 5 hours or even more if required everyday until the completion of the project. I have a 2-month long vacation after May 17 and no other commitments in hand so major part of the project will be implemented in this duration.

## GSoC

- **GSoC experience**

    No, I have not participated in GSoC before. 

    Through GSoC, I hope to gain hands-on experience in open-source collaboration, refine my implementation skills, and contributing a practical, well-documented solution that benefits the community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am applying exclusively to NIU for GSoC 2025 because this project aligns closely with my interests in confidence calibration, pose estimation, and machine learning.