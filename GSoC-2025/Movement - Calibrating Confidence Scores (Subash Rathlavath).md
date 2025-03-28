# Movement: Calibrating Confidence Scores (Subash Rathlavath)

## **Personal Details**  
- **Name:** Subash Rathlavath  
- **Email:** subashrathlavath@gmail.com  
- **GitHub:** [subashrathlavath](https://github.com/subashrathlavath)  
- **Zulip:** subashrathlavath  
- **Location & Time Zone:** Hyderabad, India (GMT+5:30)  
- **Proposal discussion link:** [Calibrating Confidence Scores PR](https://github.com/neuroinformatics-unit/movement/pull/508)  

---

## **Project Proposal**  

### **Synopsis**  
Pose estimation models provide confidence scores for predicted keypoints, but these scores are often **uncalibrated**, leading to unreliable confidence values. This project aims to **improve the reliability of confidence scores** in Movement by implementing **Log-Log Regression Calibration, Binning-Based Calibration, and Temperature Scaling**.  

### **Goals & Deliverables:**  
- A Python implementation of a method to **calibrate the confidence scores** provided by at least one of the pose estimation frameworks supported in movement (DeepLabCut, SLEAP, LightningPose, anipose).
- Tests to cover any added functionality.
- Documentation for the new functionality.
- An example use case in the movement gallery. 

### **Why is this important?**  
- Enhances **trust** in confidence scores from pose estimation models  
- Enables **fair comparisons** across different frameworks  
- Helps in **filtering high/low confidence keypoints** for better analysis  

---

## **Implementation Timeline**  

### **Minimal Deliverables:**  
- Implement **Log-Log Regression Calibration (Keypoint-Moseq style)**  
- Implement **Binning-Based Calibration**  
- Implement **Temperature Scaling**  
- Develop **Reliability Diagrams** for visualization  
- Compute **Expected Calibration Error (ECE)**  
- Provide **calibration utilities and notebooks**  

### **Stretch Goals:**  
- Optimize calibration methods for **speed and accuracy**  
- Compare different calibration techniques using **benchmark datasets**  

#### Weekly timeline  
| **Week**  | **Tasks**  |
|-----------|-----------|
| **Community bonding**  | Study existing confidence score calibration techniques and Movement’s framework. Discuss approaches with the mentor.  |
| **Week 1-2**  | Implement temperature scaling for confidence scores and test initial results.  |
| **Week 2-3**  | Implement log log regression (keypoint-moseq style) for confidence score calibration.  |
| **Week 3-4**  | Research and implement histogram binning for calibration.  |
| **Week 4-5**  | Validate and compare calibration techniques on Movement’s sample data.  |
| **Week 5-6**  | Integrate the best-performing calibration approach into Movement.  |
| **Week 6-7 (Mid-term)**  | Document findings, code structure, and initial results.  |
| **Week 7-8**  | Improve implementation efficiency and test on diverse datasets.  |
| **Week 8-9**  | Develop visualization tools for calibration assessment.  |
| **Week 9-10**  | Finalize implementation and address mentor feedback.  |
| **Week 10-11**  | Conduct extensive testing and refine calibration methods.  |
| **Week 11-12**  | Freeze code, complete documentation, and write a tutorial.  |
| **Week 12-13**  | Submit final report and prepare for project submission.  |

---

## **Communication Plan**  
 **Weekly check-ins** with mentors via **Zulip** and GitHub discussions.  
 Regular updates via **GitHub issues & PRs**.  
 Virtual meetings as needed for feedback and discussions.  

---

## **Personal Statement**  

### **Past Experience**  
I have experience in **Python, NumPy, pandas, and machine learning**. I have worked on pose estimation, data analysis, and model calibration techniques. My open-source journey has started with **Movement**, and I am actively contributing to its calibration module.  

### **Motivation: Why this project?**  
I am passionate about **pose estimation and model calibration**. This project aligns with my interests in **computer vision, AI, and uncertainty quantification**. Ensuring that confidence scores are **trustworthy and interpretable** is crucial for real-world applications.  

### **Match: Why me?**  
- Strong background in **Python & ML**  
- Experience with **DeepLabCut & pose estimation**  
- Active contributor to Movement  
- Excited about solving real-world problems in **confidence calibration**  

### **Availability**  
I have **no major commitments** during the GSoC period and can dedicate **20+ hours per week** to this project.

---

## **GSoC**  

### **GSoC Experience**  
I expect to **learn, contribute, and grow** in the open-source community, gaining experience in **ML, calibration techniques, and real-world software development**. 

### **Are you applying to other GSoC projects?**  
No, **this is my only application**, and I am fully committed to working with **Movement & NIU**.And eager to continue advancing **NIU**’s vision through sustained collaboration and technical growth post-GSoC  

---

**Looking forward to making confidence scores more reliable in Movement!** 
