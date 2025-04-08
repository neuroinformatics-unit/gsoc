# Movement: Calibrating Confidence Scores (Subash Rathlavath)

## **Personal Details**  
- **Name:** Subash Rathlavath  
- **Email:** subashrathlavath@gmail.com  
- **GitHub:** [subashrathlavath](https://github.com/subashrathlavath)  
- **Zulip:** subashrathlavath  
- **Location & Time Zone:** Hyderabad, India (GMT+5:30)  
- **Proposal discussion link:** [Calibrating Confidence Scores Poposal](https://github.com/neuroinformatics-unit/gsoc/pull/10)  
- **Code contributions** [Draft PR](https://github.com/neuroinformatics-unit/movement/pull/508)

---

## **Project Proposal**  
### **Synopsis**  
Pose estimation models provide confidence scores for predicted keypoints, but these scores are often **uncalibrated**, leading to unreliable confidence values. This project aims to **improve the reliability of confidence scores** in Movement by implementing few of the calibration methods which are optimal.  
### **Goal:**  
Goal of this project is to implement a method to **calibrate the confidence scores** provided by at least one of the pose estimation frameworks supported in movement (DeepLabCut, SLEAP, LightningPose, anipose). This method will allow researchers to compare results across frameworks, better filter high/low confidence values, and better interpret model performance
## **Implementation Timeline** 
### **Minimal deliverables** 
- A Python implementation of methods to **calibrate the confidence scores** provided by at least one of the pose estimation frameworks supported in movement (DeepLabCut, SLEAP, LightningPose, anipose).
- Develop **Reliability Diagrams** for visualization to understand how well our confidence scores match reality. 
- Compute **Expected Calibration Error (ECE)**, a numerical measure of how well our confidence scores match reality. 
- Develop tests to cover any added functionality.
- Documentation for the new functionality.
- Provide **calibration utilities and notebooks**
- A blog post summarising the journey of this project. 

### **Stretch goals (if time allows)**  
- Extend support to all other pose estimation frameworks supported by movement.
- Optimize calibration methods for **speed and accuracy**  
- Compare different calibration techniques using **benchmark datasets**
- **Interactive Napari Plugin** Real-time visualization and interaction with calibrated confidence scores during tracking, enabling immediate validation of behavior analysis.   

#### Weekly timeline  
| **Week**  | **Tasks**  |
|-----------|-----------|
| **Community bonding**  |- Study Movement's current framework and confidence score handling<br>- Research calibration techniques from literature (log-log regression, binning, temperature scaling)<br>- Understand Movement's data structures and API patterns<br>- Plan implementation approach with mentors  |
| **Week 1-2**  | Implement log-log regression calibration as the primary method and test with Movement's pose estimation data. |
| **Week 2-3**  | Implement histogram binning for calibration.  |
| **Week 3-4**  | Research and implement temperature scaling for calibration.  |
| **Week 4-5**  | Compare calibration techniques using:<br>- Expected Calibration Error (ECE)<br>- Reliability diagrams for each method<br>- Accuracy of filtered keypoint detection<br>- Performance on DLC_single_mouse_EPM dataset<br>- Computation time and memory usage benchmarks.  |
| **Week 5-6**  | Integrate the best-performing calibration approaches into Movement.  |
| **Week 6-7 (Mid-term)**  |  - Compare calibration methods' results on Movement datasets<br>- Write technical blog post about findings and implementation<br>- Ensure all code has docstrings and unit tests<br>- Update Movement gallery with calibration example  |
| **Week 7-8**  | - Profile and optimize performance bottlenecks<br>- Test calibration on diverse Movement datasets (EPM, multi-animal, different frameworks)<br>- Validate robustness across different tracking scenarios. |
| **Week 8-9**  | Develop visualization tools: reliability diagrams for expected vs actual confidence, interactive confidence distribution plots, and calibrated confidence overlays integrated with Movement's tracking visualization.  |
| **Week 9-10**  | Complete core implementation: finalize API design, optimize performance bottlenecks, implement error handling, and integrate mentor feedback on calibration methods.  |
| **Week 10-11**  | Conduct comprehensive testing: add edge case tests, benchmark performance across datasets, validate calibration accuracy, and refine methods based on test results.  |
| **Week 11-12**  | Finalize project: freeze code, update API documentation, and create a comprehensive example notebook in Movement's gallery demonstrating calibration workflow, practical usage, and performance comparisons.  |
| **Week 12-13**  | Submit final report and prepare for project submission.  |

---

## **Communication Plan**  
**Daily Standups:** Brief Zulip updates on yesterday's work, today's tasks, and any blockers
**Weekly Check-ins:** Detailed progress reviews with mentors
**GitHub:** Regular PRs and issue updates
**Additional Meetings:** As needed for complex discussions 

---

## **Personal Statement**  

### **Past Experience**  
I have experience in Python, NumPy, pandas, and machine learning. Currently contributing to Movement's [calibration module](https://github.com/neuroinformatics-unit/movement/pull/508), implementing confidence calibration methods with 96% test coverage. Previously worked on pose estimation model calibration, improving confidence score reliability by 25% in my academic project.  

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
