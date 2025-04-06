# Movement: Support For Kalman Filters (Deepak Goel)

## Personal Details
- **Full Name:** Deepak Goel  
- **Email:** [deepak.goel.pro@gmail.com](mailto:deepak.goel.pro@gmail.com)  
- **GitHub Username:** [deepakpro190](https://github.com/deepakpro190)  
- **Zulip Username:** Deepak Goel  
- **Location & Time-zone:** Delhi, India (IST, UTC+5:30)  
- **Personal Website / Project Portfolio:** deepakpro190  
- **Proposal Discussion Link:** [GitHub PR](https://github.com/neuroinformatics-unit/gsoc/pull/47/files)  
- **Code Contribution**: While I haven’t submitted a PR yet, I’ve actively studied the codebase, set up the development environment, and followed project discussions to understand the workflow and contribution guidelines. I’ve also explored potential areas to contribute and worked on ideas locally. I’m confident in my understanding of the project and ready to make meaningful contributions once the program begins.
---

## Project Proposal

### **Synopsis**
This project aims to enhance the Movement library by integrating an optimized multi-object tracking system that ensures accurate position, velocity, and acceleration smoothing while effectively handling identity switches in Multi-Animal Tracking.

At its core, the system will utilize an advanced **Kalman Filter framework**, rigorously benchmarked to select the most efficient configuration for the Movement dataset. The implementation will incorporate state-of-the-art identity association techniques, including:

- **Mahalanobis Distance & Hungarian Algorithm** for optimal detection-to-track assignment, minimizing incorrect identity associations.
- **Joint Probabilistic Data Association (JPDA)** to enhance stability in complex scenarios, where multiple animals interact or occlusions occur.
- **Re-Identification (Re-ID) with Deep Learning** to extract deep feature embeddings from animal appearances, ensuring long-term identity tracking.

To further improve decision-making, the tracking pipeline will compute a **dynamic confidence score** for each frame, integrating:
- **Motion Consistency Score**, derived from Kalman Filter-based trajectory predictions.
- **Appearance Similarity Score**, leveraging deep CNN feature embeddings for Re-ID.
- **Final Fusion Score**, a weighted combination of motion and appearance cues for robust identity resolution.

By the project's completion, the **Movement library** will feature a highly accurate, AI-powered multi-animal tracking pipeline capable of handling occlusions, identity switches, and non-linear motion.

---

## **Implementation Timeline**

### **Deliverables**
-  **Integration of a Kalman Filter** for position, velocity, and acceleration smoothing.
-  **Identity switch correction** using Mahalanobis Distance & Hungarian Algorithm.
-  **Joint Probabilistic Data Association (JPDA)** for complex tracking scenarios.
-  **Re-Identification (Re-ID) Module** with deep learning-based feature extraction.
-  **Benchmarking & testing** of tracking algorithms on real & synthetic datasets.
-  **Comprehensive documentation** with integration guides & example use cases.
-  **Unit tests** to ensure correctness and stability.

### **Stretch Goals**
-  Extending the Kalman Filter to support **automatic parameter tuning** (e.g., Expectation-Maximization or Adaptive Noise Expectation).
-  Implementing **additional identity correction heuristics**, if needed.

---

##  **Weeks & Phase Distribution (12 Weeks)**

### **Pre-GSoC Phase 1 (March 24 – April 8)**
- Submit final GSoC proposal.
- Explore Movement codebase & documentation.
- Fix minor bugs & implement test cases.

### **Pre-GSoC Phase 2 (April 9 – May 8)**
- Compare **Kalman Filter** (KF) implementations: PyKalman, NFoursid, Dynamax, MovingPandas.
- Implement & evaluate basic KF on synthetic noisy data.
- Select the best approach based on experiments.

### **Community Bonding Period (May 8 – June 1)**
- Finalize KF approach with mentors.
- Research identity switch correction techniques.
- Plan integration of confidence scores for re-identification.

---

## 🔹 **Coding Phase 1: Kalman Filtering for Multi-Entity Motion Tracking**

### **Week 1 (June 2 – June 8)**
- Implement **basic Kalman Filter** for position smoothing.
- Generate synthetic position data and evaluate filtering accuracy.
-	Fix initial bugs and ensure seamless integration with Movement datasets.

### **Week 2 (June 9 – June 15)**
- Extend KF to smooth **velocity & acceleration data**.
- Validate on **Movement datasets** & optimize performance.

### **Week 3 (June 16 – June 22)**
- Implement **Expectation-Maximization (EM)** for parameter tuning.
- Conduct thorough review & integrate mentor feedback.
- Develop **unit tests** for Kalman Filter smoothing.

### **Week 4 (June 23 – June 29)**
- Write detailed **documentation & docstrings** for the KF module.
- Create **example use cases** for Movement’s gallery.

### **Week 5 (June 30 – July 6)**
- Final optimizations to Kalman Filter implementation.
- Prepare for **mid-term evaluations** & submit reports.

---

## 🔹 **Coding Phase 2: Identity Association & Re-Identification**

### **Week 6 (July 7 – July 13) — Mid-Term Evaluation**
- Submit mid-term evaluation.
- Conduct final testing & performance evaluation for Kalman Filter.

### **Week 7 (July 14 – July 20)**
- Research & experiment with **Hungarian Algorithm & Mahalanobis Distance**.
- Gather relevant datasets & discuss **Re-ID** approach.

### **Week 8 (July 21 – July 27)**
- Implement **identity switch correction** using Hungarian Algorithm & Mahalanobis Distance.
- Validate with test cases & refine.

### **Week 9 (July 28 – August 3)**
- Improve identity tracking for **occlusions & path crossings**.
- Introduce **confidence scores** for re-identification.

### **Week 10 (August 4 – August 10)**
- Develop **unit tests** for identity switch correction.
- Integrate correction module into Movement’s **tracking pipeline**.

---

## 🔹 **Final Weeks**
### **Week 11 (August 11 – August 17)**
- Implement **Joint Probabilistic Data Association (JPDA)** for complex tracking cases.
- Create **detailed use case examples** for identity switch correction and re-identification.
- Write **documentation & integration guide** for movement users.

### **Final Week (August 18 – September 1)**
- Codebase freeze & **final performance evaluation**.
- Conduct extensive **testing & mentor reviews**.
- Submit **final GSoC report**.

---

## **Communication Plan with Mentors**
- **Weekly Meetings**: Sync-up meetings for progress discussions with mentors to discuss progress and resolve issues.
- **GitHub Discussions**: Use issues & PRs for code reviews.
- **Google Docs**: Collaborative documentation & mentor feedback.


# Personal Information

## Past Experience

### Vehicle & License Plate Recognition (YOLO & OCR)
- Developed a real-time vehicle tracking system using YOLOv8-L, achieving 99.47% mAP@50.
- Integrated OCR for license plate text extraction in images and videos.
- Relevance: Experience with tracking, identity re-identification (Re-ID), Hungarian algorithm-based assignment, and Kalman filters.

---

### Sentiment Analyzer
- Fine-tuned RoBERTa achieving 94.04% accuracy and optimized LSTM for sentiment classification.
- Relevance: Hands-on experience with sequence modeling and state estimation, useful for Kalman filtering & tracking optimizations.

---

### RAG-based Financial Chatbot
- Built a multi-agent system for query routing, improving efficiency by 50%.
- Relevance: Experience with multi-agent coordination, useful for identity tracking & confidence-based Re-ID.

---

### Internship at NSUT (BiasFinder Project)
- Worked with large datasets (IMDb: 50K, Twitter: 1.6M), gaining expertise in data processing and model evaluation.
- Relevance: Handling noisy real-world data, essential for identity tracking challenges.

---

## Relevant Coursework
- Design & Analysis of Algorithms
- Optimization Techniques
- Machine Learning
- Computer Vision  
Strengthens expertise in tracking, filtering, and optimization for this project.

---

## Motivation
- Fascinated by multi-object tracking challenges and improving motion estimation in real-world scenarios.
- Passionate about probabilistic filtering techniques to enhance tracking accuracy & stability.
- Drawn to open-source collaboration, seeing it as an opportunity to contribute meaningfully while learning from mentors.
- Excited to work on a project that blends algorithmic efficiency with practical impact, particularly in identity assignment & re-identification.

---

## Why Me?
- Background in data-driven model optimization, including filtering methods & structured tracking pipelines.
- Comfortable with experimenting & iterating on tracking solutions, balancing theory with practical implementation.
- Experience with object recognition & feature matching, aligning with identity tracking challenges.
- Detail-oriented in testing & documentation, ensuring clarity & usability in implementations.
- Committed to open-source development, eager to engage with the community and refine solutions through collaboration.

---

## Availability
- Committed to 200+ hours for this project with no planned vacations or travel.
- My working hours (UTC +5:30) are:  

### Weekday Availability (5-6 hours/day)
- 11:00 – 18:00 IST

### Weekend Availability (4-5 hours/day)
- 11:00 – 16:00 IST

Flexible and willing to adjust & re-plan my schedule based on project requirements & mentor feedback.

---

## GSoC Experience
- First-time GSoC applicant, enthusiastic about the chance to contribute to an open-source initiative.
- Actively explored past GSoC projects, discussions & best practices.
- Looking forward to collaborating with mentors & making a meaningful impact.
- Studied previous GSoC contributions to understand the workflow & expectations.

---

## Applying to Other Orgs?
- No, this is my sole application.  
- My full attention & dedication is directed toward this project.  
- Committed to ensuring its successful execution.  
