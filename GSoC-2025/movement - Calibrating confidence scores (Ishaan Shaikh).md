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

    This project focuses on **calibrating confidence scores** in pose estimation to ensure they accurately **reflect the reliability** of keypoints.  Improving confidence calibration will enhance the **usability**, and help researchers to **compare pose estimation results** more accurately, making it more reliable and widely applicable in open-source research and real-world applications.
- **Implementation timeline**

    **Minimal Deliverables**  

    - Implement a **confidence calibration method** for at least one pose estimation framework. Since confidence score computation varies across frameworks, comparing 2-3 calibration techniques can help determine the most adaptable approach.
    - Develop **unit tests** and an **example use case**.  
    - Create **documentation** explaining the calibration method and integration process.  
    - Write a **blog post** summarizing the implementation, challenges, and findings.  

    **Stretch Goals (If Time Allows)**  
    - Extend calibration support to **multiple** pose estimation frameworks instead of just one.   
    - Improve **efficiency and scalability** of the calibration process for larger datasets by using **parallelization** and leveraging high-confidence keypoints as pseudo-ground truth.
    - Explore the **impact** of confidence calibration on **downstream tasks** by assessing performance changes like reduced false positives/negatives.


**Weekly Timeline:**  

| **Week & Dates** | **Tasks & Deliverables** |
|------------------|-------------------------|
| **Community Bonding (May 8 – June 1)** | Set up the development environment, finalize a framework (choosing between **DLC or SLEAP**, as they are the most widely used in movement), research and explore calibration techniques, and develop implementation plan. |
| **Week 1 & 2 (June 2 – June 15)** | Implement **preprocessing** for confidence scores and keypoint errors. This includes normalizing and scaling confidence scores for consistency, aligning keypoint detections with ground truth, and applying transformations. Experiment with calibration techniques and discuss evaluation metrics with mentors. |
| **Week 3 & 4 (June 16 – June 29)** | Implement the chosen calibration method. Evaluate its effectiveness and refine it based on initial results. Benchmark **calibrated vs. uncalibrated** confidence scores. |
| **Week 5 & 6 (June 30 – July 13) (Midterm Evaluation)** | Integrate the calibration method into movement. Write **documentation** and implement **integration tests**. For efficiency, apply batch processing where appropriate. Submit midterm evaluation by July 18. |
| **Week 7 & 8 (July 14 – July 27)** | **Compare pose outputs** before and after calibration along with confidence histograms to demonstrate improvements in score distributions. Compute metrics such as Expected Calibration Error, **analyze confidence vs accuracy** to show that calibrated scores better reflect true accuracy. |
| **Week 9 (July 28 – Aug 3)** | **(Buffer Period)** Address mentor feedback, fix bugs, and optimize performance to ensure a robust implementation. |
| **Week 10 & 11 (Aug 4 – Aug 17)** | Finalize all code, improve maintainability, and ensure **proper integration** into movement. Conduct additional **small-scale evaluations** if necessary. Complete any remaining documentation. |
| **Week 12 (Aug 18 – Aug 25)** | **(Final Submission)** Submit final project, mentor evaluation, and write a blog post summarizing implementation and findings. |
| **Post GSoC (After Aug 25)** | Continue contributing to **movement**, explore broader applications in movement, and engage with the community. |


- **Communication plan**

    I plan to maintain regular communication with my mentors to ensure steady progress. I will **share daily updates** on my progress, challenges, and next steps through **Zulip**. Additionally, planning can be discussed in the bi-weekly **community calls**. Separate **Zoom meetings** will be scheduled as needed.

## Personal statement

- **Past experience** 

    I have built a strong background in machine learning and computer vision through hands-on projects and open-source work. For example, in my Virtual Try-On project, I developed a pose detection system that aligned virtual clothing with user movements. I gained extensive experience in data preprocessing—cleaning raw data, normalizing confidence scores, and aligning keypoints with ground truth labels to ensure reliable performance. My work has been recognized in several competitions and hackathons, including securing 2nd place in Pixel Pursuit, an OpenCV competition, and 3rd place in AI vs Humans, a Turing Test-based challenge organized by COC VJTI. I was also the leader of a team that qualified for the Smart India Hackathon, largest national-level hackathon in India. I built and put into action machine learning and computer vision algorithms such as YOLO, U-Net, CNNs using Python, OpenCV, and PyTorch/Tensorflow. I have always focused on writing clear and efficient code.

- **Motivation: why this project?**

    Pose estimation is widely used in fields like biomechanics, robotics, and behavior analysis, but uncalibrated confidence scores can lead to inaccurate interpretations. This project excites me because it tackles a fundamental challenge in pose estimation—calibrating confidence scores to better reflect actual prediction reliability. Having worked on pose estimation in my Virtual Try-On project, I have seen how inconsistent keypoint predictions impact accuracy and understood the need for more robust confidence measures. This project will improve confidence calibration in pose estimation, making models more reliable and easier to interpret. By enhancing movement’s capabilities, it will help researchers make better use of keypoint data while encouraging broader adoption and community contributions.

- **Match: why you?**

    I have a solid background in computer vision and pose estimation, and my work on a Virtual Try-On project has given me practical experience with real-world challenges in detecting keypoints. I’ve built strong skills in Python, OpenCV, and PyTorch through these projects and always strive to write clear, well-documented code. I am passionate about open-source development and enjoy solving technical problems with practical solutions. I believe my experience and enthusiasm make me a great fit for this project, and I’m excited to design and refine a calibration method that improves the accuracy of pose estimation across different tools, ultimately benefiting the entire community.

- **Availability**

    In the coding period, I will work for at least 4 to 5 hours or even more if required everyday until the completion of the project as the length of the project is 175 hours. I have a 2-month long vacation after May 17 and no other commitments in hand so a major part of the project will be implemented in this duration.

## GSoC

- **GSoC experience**

    No, I have not participated in GSoC before. 

    Through GSoC, I hope to gain hands-on experience in open-source collaboration, refine my implementation skills, and contribute to a practical, well-documented solution that benefits the community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am applying exclusively to Neuroinformatics Unit for GSoC 2025 because this project aligns closely with my interests in pose estimation, and machine learning.