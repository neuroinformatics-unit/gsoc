## movement: Calibrating Confidence Scores in movement (Mahima Sahu)


## Personal details
- **Full name** : Mahima Sahu
- **Email** : mahimasahoo0@gmail.com
- **GitHub username** : [Mahi7828](https://github.com/Mahi7828)
- **Zulip username** : Mahima Sahu
- **Location & time-zone** : Mumbai, India, Indian Standard Time (GMT+5:30)
- **Code contribution**
    1. [Adding Upsampled data for all frames](https://github.com/neuroinformatics-unit/movement/pull/502)
    2. [Adding support for optical marker-based motion capture data](https://github.com/neuroinformatics-unit/movement/pull/530)
    3. [Splitting Individuals and DLC Format](https://github.com/neuroinformatics-unit/movement/pull/529)
    

- **Proposal discussion link**
    THe current PR being viewed


## Project proposal 

- **Synopsis**:
  
    The project aims to calibrate the confidence scores produced by pose estimation frameworks (e.g., DeepLabCut, SLEAP) in the movement ecosystem so that they better reflect the actual     probability of a keypoint being correctly detected. Implementing methods for improving confidence calibration will improve result reliability, model comparison, and overall         
   interpretability for research and other purposes.

- **Implementation timeline**
    - **Minimal Deliverables**
        - Implement a calibration method for confidence scores in at least one supported pose estimation framework (e.g., DeepLabCut or SLEAP), comparing multiple approaches such as logistic or log-log regression.

        - Evaluate calibration performance using reliability diagrams and metrics such as Expected Calibration Error (ECE), and assess its effect on downstream tasks like behavioral classification.

        - Develop unit tests to ensure correctness and stability of the implemented calibration methods.

        - Create user-facing documentation and example notebooks to guide users and also work on a blog post summarizing the project journey, implementation details and key takeaways.

    - **Stretch Goals (If time allows)**
        - Multi-Framework Support: Extend calibration methods to multiple pose estimation frameworks with a unified interface.

        - Interactive Calibration Widget: Create a user-friendly widget (via Napari or Jupyter) for visualizing and adjusting calibration curves interactively.

        - Semi-Supervised Calibration: Use high-confidence predictions as pseudo-labels to improve calibration when ground truth is limited.

        - Behavior-Based Filtering Tool: Develop a utility that filters or weights keypoints using calibrated scores to enhance behavior classification performance.


## 🗓️ Weekly Timeline
| **Week & Dates**                         | **Tasks & Deliverables**                                                                                                                                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Community Bonding (May 8 – June 1)**   | <ul><li>Explore pose estimation tools (DLC/SLEAP) and understand the movement’s tracking/confidence structure.</li><li>Review calibration techniques like log-log regression, binning, and temperature scaling.</li><li>Finalize datasets and evaluation metrics (ECE, Brier Score, Accuracy).</li><li>Plan implementation pipeline.</li></ul> |
| **Week 1–2 (June 2 – June 15)**          | <ul><li>Preprocess data: normalize confidence scores and align keypoints with ground truth.</li><li>Implement log-log regression calibration and validate using movement datasets.</li><li>Generate histograms and KDE plots to visualize score spread and model uncertainty.</li><li>Compute Expected Calibration Error (ECE) and plot reliability diagrams to assess score alignment with accuracy.</li></ul> |
| **Week 3–4 (June 16 – June 29)**         | <ul><li>Add histogram binning and temperature scaling calibration methods.</li><li>Benchmark methods using ECE and confidence histograms.</li><li>Begin integration of these techniques into Movement’s workflow.</li></ul> |
| **Week 5–6 (June 30 – July 13) : Midterm Evaluation**         | <ul><li>Compare calibration methods on quality, keypoint accuracy, and behavior classification.</li><li>Finalize the best-performing method.</li><li>Add unit tests and docstrings.</li><li>Submit midterm evaluation and draft technical blog post.</li></ul> |
| **Week 7–8 (July 14 – July 27)**         | <ul><li>Integrate the final calibration method into Movement with batch processing.</li><li>Test across diverse datasets (multi-animal, EPM) and under varied conditions.</li><li>Add Gaussian noise and mask keypoints to test calibration under occlusion & noise.</li><li>Apply min-max and z-score scaling to assess sensitivity to confidence score ranges and check robustness using ECE, MCE, and reliability diagrams.</li></ul> |
| **Week 9 (July 28 – August 3)**          | <ul><li>Use a buffer week to fix edge cases and incorporate mentor feedback.</li><li>Stabilize calibration logic and begin behavior-based filtering using calibrated scores to enhance downstream classification tasks.</li></ul> |
| **Week 10–11 (August 4 – August 17)**    | <ul><li>Develop an interactive calibration visualization tool (Napari or Jupyter widget).</li><li>Analyze confidence distributions and reliability diagrams.</li><li>Extend pipeline to support both DLC and SLEAP via a unified API.</li><li>Finalize modular code and write additional test cases.</li></ul> |
| **Week 12 (August 18 – August 25)**      | <ul><li>Freeze codebase, Finalize documentation, notebooks, and tutorials.</li><li>Write and publish the final blog post summarizing project outcomes, key learnings, and future potential.</li><li>Submit final evaluation.</li></ul> |
| **Post-GSoC**                            | <ul><li>Maintain and improve features.</li><li>Explore semi-supervised calibration with pseudo-labels.</li><li>Continue contributing to the Movement’s ecosystem and pose estimation tools.</li></ul> |


---
        

- **Communication plan** : 
    I will maintain regular contact with mentors via daily Zulip updates, bi-weekly community calls for planning and feedback. Additional Zoom meetings will be arranged when deeper discussions are needed.
    

## Personal statement

- **Past experience.** 

    I've worked extensively on deep learning and model calibration across multiple modalities. During Seasons of Code with the Coding Club, IIT Bombay, I fine-tuned BERT and LLaMA using LoRA and QLoRA, and integrated RAG for better contextual accuracy in language tasks like Q&A and summarization [LLM_Enhancements](https://github.com/Mahi7828/Contextual_LLM_Enhancements). As part of the Analytics Club, I built a [real-time face mask detection](https://github.com/Mahi7828/Active_Face_Mask_Detection) system using CNNs and OpenCV. As my Course Team Project, I’ve also developed a [CNN-based model](https://github.com/https-kanika/Audio-Genre-Classification-DS203-E7-Project-24/tree/main) to classify MFCC audio features into genres and genders, applying calibration-aware metrics like ROC curves and confidence thresholds for evaluation.

- **Motivation: why this project?**

    This project uniquely blends trustworthy AI with real-world application in neuroscience and behavior analysis. I’m particularly excited by the idea of working with real-world outputs from pose estimation models and calibrating them to ensure more reliable decision-making.The project's emphasis on metrics like Expected Calibration Error (ECE), Maximum Calibration Error, and per-keypoint confidence evaluation resonates strongly with the kind of analytical and model evaluation work I’ve done in the past.


- **Match: why you?**

    My background spans NLP, vision, and audio classification, with hands-on experience in model calibration, evaluation metrics, and performance visualization. I’ve worked in team-based open-source environments and enjoy writing clean,w testable code. I believe my prior experience makes me well-suited to contribute effectively and efficiently to this project.

- **Availability** : 
    I will be fully available throughout the GSoC period, as I have my summer break, with no conflicting commitments, and can dedicate 25+ hours per week to this project.
    
## GSoC

- **GSoC experience**
    This is going to be my first GSOC project. 

    Through GSoC, I hope to work closely with experienced mentors, contribute to real-world open-source development, and deepen my understanding of model calibration in pose estimation. I'm excited about the opportunity to write production-level code, receive valuable feedback, and be part of a global community working on impactful technology

- **Are you also applying to projects with other organisations in GSoC 2025?**
  
    I am not applying to any other organizations, as I am genuinely interested in contributing to this project's goals and see strong alignment with my skills and long-term interests. 

