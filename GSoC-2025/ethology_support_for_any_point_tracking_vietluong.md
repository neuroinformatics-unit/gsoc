

## ethology: Support for Any-Point Tracking (Viet Luong)

## Personal details

- **Full name**: Viet Luong
- **Email**: vietintern@gmail.com
- **GitHub username**:vietluong2110
- **Zulip username**: Viet Luong
- **Location & time-zone**: Chicago, GMT-5
- **Personal website / project portfolio**
- **Code contribution**

    - [add tapir option to tap models api #73 - In Review](https://github.com/neuroinformatics-unit/ethology/pull/73)
    - [video-utilities - In Review](https://github.com/neuroinformatics-unit/ethology/pull/68)
    - [JAX-SimpleTM](https://github.com/vietluong2110/jax_simpletm)    

- **Proposal discussion link**
    [PR Link](https://github.com/neuroinformatics-unit/gsoc/pull/24)

## Project proposal 
_Length: max 1 page_

- **Synopsis**

This project integrates advanced any-point tracking methods like cotracker3 and TAPIR into the ethology framework, aiding animal behavior research. It will develop a napari plugin for video loading, point selection, automated tracking, and trajectory visualization. Deliverables include a napari widget prototype, back-end tracking integration, and front-end visualization. The open-source community benefits from improved accessibility to advanced computer vision tools, enhancing research efficiency.

- **Implementation timeline**

**Minimal Set of Deliverables:**
- Functional napari widget prototype for loading videos and selecting query points.
- Back-end integration with cotracker3 or TAPIR for running any-point tracking inference.
- Capability to generate and export trajectory data.
- Visualization overlay of trajectories within the napari interface.
- Documentation for plugin usage and codebase.
- Integration of additional any-point tracking models.


 **Stretch Goals (If time allows)**:
- Advanced visualization features (trajectory filtering, custom annotations).


**Community Bonding Period (Prep work)**:
- Familiarize thoroughly with napari plugin documentation and development process.
- Set up the development environment.
- Discuss implementation details and milestones with mentors.
- Familiarising further with the ethology codebase 
- Discussing package roadmap with the community 
- Participating in relevant community meetings

# Weekly Timeline

- **Week 1: Refined Backend Integration & PR Feedback (30 hours)**
  - **Review and Incorporate PR Feedback:** Address changes requested in the open ethology PR.
  - **Code Refactoring & Modularization:** Improve error handling and modularity based on initial work.
  - **Enhanced Testing Setup:** Develop targeted unit and integration tests for updated components.
  - **Create Initial Documentation:** Document initial setup and installation steps (starting documentation from scratch).

- **Week 2: Backend Inference Pipeline Development (30 hours)**
  - **Implement Inference Pipeline:** Write backend code to run any-point tracking.
  - **Generate Trajectory Data:** Produce basic trajectory data (coordinates across frames).
  - **Initial Validation:** Conduct preliminary validations of the generated trajectories.
  - **Documentation:** Document the backend inference pipeline.

- **Week 3: Backend Refinement & Debugging (30 hours)**
  - **Debug and Refine:** Improve the inference pipeline through debugging.
  - **Enhance Robustness:** Improve error handling.
  - **Stable Integration:** Ensure stable integration of cotracker3/TAPIR inference.
  - **Unit Testing:** Create additional backend unit tests.

- **Week 4: Trajectory Data Export Functionality (30 hours)**
  - **Develop Export Methods:** Create methods to export trajectory data in CSV and JSON formats.
  - **Validation:** Validate data export formats and consistency.
  - **Integration:** Integrate export functionality into the backend system.
  - **Documentation:** Document the export process clearly.

- **Week 5: Frontend – Initial Napari Widget Setup (30 hours)**
  - **Plugin Design:** Design a basic napari plugin structure.
  - **Video Loading:** Implement a video loading interface.
  - **Query Point Selection:** Develop query point selection and storage functionality.
  - **Documentation:** Document widget installation and basic usage.

- **Week 6: Frontend-Backend Integration & Mid-term Report (30 hours)**
  - **Connect Components:** Link the napari frontend widget with the backend inference system.
  - **End-to-End Testing:** Verify successful end-to-end tracking from the widget interface.
  - **Mid-term Report:** Write and submit a mid-term progress report.

- **Week 7: Trajectory Visualization Overlays within Napari (30 hours)**
  - **Overlay Implementation:** Implement visualization overlays of trajectories onto loaded videos.
  - **Mapping Accuracy:**  
  Ensure that the coordinates output by the tracking system correctly correspond to the actual positions in the video frames. This means verifying that the transformation from the model’s coordinate system to the video’s pixel space is accurate, so that when overlays are drawn, they line up with the intended features
  - **Validate Visualization Correctness:**
    - **Quantitative Assessment:** Compute the mean pixel error between overlayed tracked points and manually annotated ground truth on a set of test frames.
    - **Qualitative Assessment:** Conduct systematic visual inspections across diverse video segments (e.g., varying lighting, movement speed) to confirm alignment.
    - **User Validation**: Solicit feedback from targeted users (or team members) to identify any discrepancies in the overlays.

- **Week 8: Visualization Interactivity Improvements (30 hours)**
  - **UI Enhancement:** Enhance the user interface for responsiveness.
  - **User Testing & Feedback Collection:**
    - **Task Assignment:** Ask users to load a sample video, select query points, and use interactive features.
    - **Feedback Collection:** Gather feedback on usability, visual accuracy, and responsiveness.
    - **Observation & Documentation**: Observe users during testing to note any difficulties, then compile feedback to guide iterative improvements.

- **Week 9: Optimization, Performance Testing & Bug Fixing (30 hours)**
  - **Performance Optimization:** Optimize inference speed and resource usage.
  - **Benchmarking:**
    - **Task Definition:**  
        - Define standard tasks, such as loading a sample video and processing a fixed number of frames to generate trajectory data.
    - **Metrics:**  
        - **Inference Speed:** Measure processing time per frame or calculate frames per second.  
        - **Resource Utilization:** Monitor CPU/GPU usage and memory consumption during the inference process.  
        - **Accuracy Metrics (if applicable):** For example, compute the mean pixel error by comparing outputs against ground truth annotations.
    - **Comparison:**  
        - Compare these metrics against baseline values or previous iterations to evaluate performance improvements or regressions.  
  - **Bottleneck Resolution:** Address identified performance bottlenecks.
  - **Bug Fixing:** Fix any remaining frontend/backend bugs.

- **Week 10: Detailed Documentation and User Guide Preparation (30 hours)**
  - **Documentation:** Complete comprehensive backend and frontend documentation.
  - **User Guides:** Write detailed user guides, tutorials, and usage examples.

- **Week 11: Code Freeze, Final Testing, and Submission Preparation (30 hours)**
  - **Final Testing:** Conduct comprehensive final tests.
  - **Bug Resolution:** Address any critical bugs or performance issues.
  - **Submission Prep:** Begin preparation of final submission materials.

- **Week 12: Final Feedback Incorporation & Project Submission (30 hours)**
  - **Finalization:** Finalize and polish all documentation and system components.
  - **Submission:** Submit final deliverables and project materials.



**Total Project Duration:** 12 weeks × 30 hours/week = **~360 hours**

**Note:** No vacations or major commitments planned; weekly hours and tasks may adjust slightly based on mentor feedback and project progress.   

- **Communication plan**

- **Frequency:** Weekly stand-up meetings for updates and progress reviews; additional brief daily or bi-weekly check-ins via chat as needed.
- **Channels:** Regular video calls (Zoom/Google Meet) for weekly discussions; continuous communication and quick queries via Zulip or GitHub issues.
- **Documents**: Track the status of the project by using devlog, or sprint backlog
## Personal statement

_Length: max 0.75 page_

- **Past experienc.** 

I have a robust background in programming, open-source development, and research, highlighted by my ongoing roles as a Research Assistant at Yin Li’s Lab and Vikas Singh’s Lab at the University of Wisconsin-Madison. At Yin Li’s Lab, I designed and implemented algorithms to generate precise region prompts (simulating the idea of RPN) for the MedSAM model, enhancing localization in medical X-ray images. Additionally, I successfully applied CLIPSelf (Knowledge Distillation) to improve dense feature representation, significantly boosting the model's accuracy in region classification task.

At Vikas Singh’s Lab, the SimpleTM model focused on tackling the challenges of multivariate time-series forecasting. This task involves predicting future values based on historical data from multiple, potentially heterogeneous sources—such as traffic data (PEMS) or sensor measurements (M4). The SimpleTM model was designed as a lightweight, specialized solution that leverages classical signal processing techniques (like wavelet-based tokenization) and a modified attention mechanism (using geometric product attention) to effectively capture both short-term fluctuations and long-term dependencies.

In addition to optimizing model efficiency—improving speed per iteration by sixfold using frameworks like JAX and Triton—my research also involved: 
- **Computational Efficiency:** Assessing model speed, memory usage, and parameter counts.
- **Robustness Across Datasets:** Testing on diverse, publicly available benchmarks (e.g., ETT, Weather, Solar-Energy, Traffic, and PEMS) to ensure that SimpleTM performs competitively in different scenarios.
- **Scalability and Generalization:** Verifying that even a shallow (single- or two-layer) architecture can capture complex inter-channel relationships, providing a strong baseline against more complex models.


- **Motivation: why this project?**

My interest in this project is driven by a deep enthusiasm for computer vision and its applications in scientific research. The intersection of advanced tracking technologies and practical usability resonates strongly with my career aspirations and research interests. Specifically, integrating tools such as cotracker3 or TAPIR into user-friendly frameworks like napari offers tremendous potential to advance research efficiency in ethology and broader scientific communities. The project’s goal of making sophisticated computer vision tools accessible aligns closely with my motivation to contribute meaningful, practical solutions to the open-source ecosystem.
- **Match: why you?**

I am particularly well-suited for this project due to my extensive background in developing, optimizing, and deploying sophisticated computer vision and machine learning models. My technical proficiency in Python, PyTorch, JAX, and advanced GPU programming directly complements the project's requirements. Furthermore, my practical experience implementing complex algorithms, as demonstrated in my research roles, equips me with the technical and collaborative skills essential for successfully integrating cotracker3 and TAPIR with the napari interface. My strong record of research publication and teamwork ensures that I can effectively collaborate with mentors and positively impact the open-source community.
- **Availability**

I am fully available during the GSOC project so I can commit up to 30 hours per week.

## GSoC

_Length: max 0.25 page_

- **GSoC experience**

I expect structured mentorship, practical experience with advanced computer vision methods, and opportunities to actively contribute to open-source development. Through regular feedback and community engagement, I aim to refine my technical skills and enhance my professional growth.


- **Are you also applying to projects with other organisations in GSoC 2025?**

 No I am not