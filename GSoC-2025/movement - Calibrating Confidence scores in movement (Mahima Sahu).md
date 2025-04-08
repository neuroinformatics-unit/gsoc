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
    [PR](https://github.com/neuroinformatics-unit/gsoc/pull/70/files)


## Project proposal 

- **Synopsis**:
  
    The project aims to calibrate the confidence scores produced by pose estimation frameworks (e.g., DeepLabCut, SLEAP) in the movement ecosystem so that they better reflect the actual probability of a keypoint being correctly detected. Implementing methods for improving confidence calibration will improve result reliability, model comparison, and overall         
   interpretability for research and other purposes.

- **Implementation timeline**
    - **Minimal Deliverables**
        - Implement a calibration method for confidence scores in supported pose estimate framework using log-log regression, Histogram binning, Temperature sensing, or isotonic regressions

        - Evaluate calibration performance using reliability diagrams (predicted confidence vs. true accuracy) and metrics such as Expected Calibration Error, and its effect on downstream tasks like behavioral classification.

        - Develop unit tests to ensure correctness and stability of the implemented calibration methods.

        - Create user-facing documentation and example notebooks to guide users and also work on a blog post summarizing the project journey, implementation details and key takeaways.

    - **Stretch Goals (If time allows)**
        - Multi-Framework Support: Extend calibration methods to multiple pose estimation frameworks with a unified interface.

        - Interactive Calibration Widget: Create a user-friendly widget (via Napari or Jupyter) for visualizing and adjusting calibration curves interactively.

        - Semi-Supervised Calibration: Use high-confidence predictions as pseudo-labels to improve calibration when ground truth is limited.

        - Develop a Behavior-Based Filtering Tool that weights keypoints using calibrated scores to enhance behavior classification performance (based on Random Forest/LSTM and evaluated through metrics like F1 score and ECE) 



## 🗓️ Weekly Timeline

| **Week & Dates**                         | **Tasks & Deliverables** |
|------------------------------------------|---------------------------|
| **Community Bonding (May 8 – June 1)**   | - Explore pose estimation tools (DLC/SLEAP) and understand Movement’s tracking/confidence structure. <br> - Review calibration techniques like log-log regression, binning, and temperature scaling. <br> - Start working with datasets and evaluation metrics (ECE, Brier Score) and plan the implementation pipeline. |
| **Week 1–2 (June 2 – June 15)**          | - Normalize confidence scores and align keypoints with available ground truth; annotate a small, diverse subset if not available. <br> - Implement log-log regression and validate calibration on Movement datasets. <br> - Visualize confidence distributions using histograms and KDE plots. <br> - Perform initial calibration evaluation using ECE and reliability diagrams. |
| **Week 3–4 (June 16 – June 29)**         | - Add histogram binning and temperature scaling calibration methods. <br> - Benchmark methods using ECE and confidence histograms. <br> - Begin integration of these techniques into Movement’s workflow. |
| **Week 5–6 (June 30 – July 13)** <br> *Midterm Evaluation* | - Compare calibration methods on quality, keypoint accuracy, and behavior classification. <br> - Finalize the best-performing method. <br> - Add unit tests and docstrings. <br> - Submit midterm evaluation and draft technical blog post. |
| **Week 7–8 (July 14 – July 27)**         | - Integrate the final calibration method with support for batch processing. <br> - Evaluate robustness across varied datasets (multi-animal, EPM) and under occlusion/noise (Gaussian noise, masked keypoints). <br> - Apply min-max and z-score scaling to assess sensitivity to confidence score ranges. <br> - Summarize results using ECE, MCE, and reliability diagrams. |
| **Week 9 (July 28 – August 3)**          | - Use a buffer week to fix edge cases and incorporate mentor feedback. <br> - Ensure calibration methods generalize across datasets. <br> - Begin behavior-based filtering using calibrated scores to improve downstream classification. |
| **Week 10–11 (August 4 – August 17)**    | - Develop an interactive calibration visualization tool (Napari or Jupyter widget). <br> - Analyze confidence distributions and reliability diagrams. <br> - Extend pipeline to support both DLC and SLEAP via a unified API. <br> - Finalize modular code and write additional test cases. |
| **Week 12 (August 18 – August 25)**      | - Freeze codebase and finalize documentation, notebooks, and tutorials. <br> - Write and publish final blog post summarizing outcomes, learnings, and future potential. <br> - Submit final evaluation. |
| **Post-GSoC**                            | - Maintain and improve features. <br> - Explore semi-supervised calibration with pseudo-labels. <br> - Continue contributing to Movement and pose estimation tools. |


---
        

- **Communication plan** : 
    I will maintain regular contact with mentors via daily Zulip updates, bi-weekly community calls for planning and feedback. Additional Zoom meetings will be arranged when deeper discussions are needed.
    

## Personal statement

- **Past experience.** 

    I've worked extensively on deep learning and model calibration across multiple modalities. During Seasons of Code with the Coding Club, IIT Bombay, I fine-tuned BERT and LLaMA using LoRA and QLoRA, and integrated RAG for better contextual accuracy in language tasks like Q&A and summarization [LLM_Enhancements](https://github.com/Mahi7828/Contextual_LLM_Enhancements). As part of the Analytics Club, I built a [real-time face mask detection](https://github.com/Mahi7828/Active_Face_Mask_Detection) system using CNNs and OpenCV. As my Course Team Project, I’ve also developed a [CNN-based model](https://github.com/https-kanika/Audio-Genre-Classification-DS203-E7-Project-24/tree/main) to classify MFCC audio features into genres and genders, applying calibration-aware metrics like ROC curves and confidence thresholds for evaluation.

- **Motivation: why this project?**

    This project uniquely blends trustworthy AI with real-world application in neuroscience and behavior analysis. I’m particularly excited by the idea of working with real-world outputs from pose estimation models and calibrating them to ensure more reliable decision-making.The project's emphasis on metrics like Expected Calibration Error (ECE), Maximum Calibration Error, and per-keypoint confidence evaluation resonates strongly with the kind of analytical and model evaluation work I’ve done in the past.


- **Match: why you?**

    My background spans NLP, vision, and audio classification, with hands-on experience in model calibration, evaluation metrics, and performance visualization. I’ve worked on projects like [CNN-based model](https://github.com/https-kanika/Audio-Genre-Classification-DS203-E7-Project-24/tree/main), [RL_Quant](https://github.com/Mahi7828/RL_Agent_Quant) and [LLM_Enhancements](https://github.com/Mahi7828/Contextual_LLM_Enhancements) etc. I have also worked as a *Web Coordinator* for Mood Indigo 2024, contributing in the development of different webpages for fest. I  enjoy writing clean, testable code. I believe my prior experience makes me well-suited to contribute effectively and efficiently to this project.

- **Availability** : 
    I will be fully available throughout the GSoC period, as I have my summer break, with no conflicting commitments, and can dedicate 25+ hours per week to this project.
    
## GSoC

- **GSoC experience**
    This is going to be my first GSOC project. 

    Through GSoC, I hope to work closely with experienced mentors, contribute to real-world open-source development, and deepen my understanding of model calibration in pose estimation. I'm excited about the opportunity to write production-level code, receive valuable feedback, and be part of a global community working on impactful technology

- **Are you also applying to projects with other organisations in GSoC 2025?**
  
    I am not applying to any other organizations, as I am genuinely interested in contributing to this project's goals and see strong alignment with my skills and long-term interests. 

