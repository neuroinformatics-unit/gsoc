# movement: Behavioral Event Detection Module (Krutika Diwathe)

## Personal details
**Full name:** Krutika Bhushan Diwathe  
**Email:** krutika.diwathe16@gmail.com  
**GitHub username:** krutikadiwathe  
**Zulip username:** [krutika diwathe](https://neuroinformatics.zulipchat.com/#user/897183)  
**Location & time-zone:** Cleveland, OH, USA (EST / UTC -5)  
**Personal website / project portfolio:** [Portfolio](https://krutikadiwathe.github.io/portfolio/) | [GitHub](https://github.com/krutikadiwathe)

## Code contribution
[GitHub Repo – movement-freezing-detection](https://github.com/krutikadiwathe/movement-freezing-detection)

This repo contains my GSoC code contribution for a heuristic-based freezing behavior detection module for the movement project. The detection logic identifies periods of low centroid velocity over time and is designed to support user-defined thresholds for velocity and duration. A unit test is included to validate functionality using synthetic motion data, and it passes successfully with pytest.

## Project proposal

### Synopsis
This project aims to develop a behavioral event detection module for the `movement` Python package, designed to identify complex animal behaviors (e.g., freezing, grooming, rearing) from pose estimation data. Currently, many researchers rely on manual annotations, which are time-consuming and inconsistent. This project will address this gap by implementing automated, customizable tools based on heuristics and machine learning models, enhancing reproducibility and efficiency in behavioral science. Deliverables include core detection modules, visualization, and integration within the movement ecosystem.

### Implementation timeline

**Minimal deliverables:**
- Heuristic-based detection logic for freezing and other predefined behaviors
- ML-based classifier using pose-derived features
- Integrated trajectory/behavior visualization support
- Core module integration, configuration settings, unit tests, and documentation

**Stretch goals (if time allows):**
- GUI to help users define behaviors or adjust thresholds
- Real-time event detection pipeline for pre-recorded data
- Expand framework to allow user-defined/custom behaviors

| Week | Timeline | Deliverables |
|------|----------|--------------|
| Community Bonding | April 20 - May 19 | Final proposal review, setup dev environment, connect with mentors and community, study behavior classification literature |
| Week 1 | May 20 - May 26 | Initial behavior detection framework, freezing detection implementation |
| Week 2 | May 27 - June 2 | Add visualization of behavior events (highlighted trajectories) |
| Week 3 | June 3 - June 9 | Implement velocity & posture-based feature extraction |
| Week 4 | June 10 - June 16 | ML classifier for grooming/rearing, early testing |
| Week 5 | June 17 - June 23 | Integrate ML predictions with movement data structures |
| Week 6 (Midterm) | June 24 - June 30 | Evaluation and documentation of modules completed |
| Week 7 | July 1 - July 7 | Extend support for parameter tuning and user configs |
| Week 8 | July 8 - July 14 | Begin optional GUI or real-time processing |
| Week 9 | July 15 - July 21 | Wrap up enhancements and refine GUI or stretch features |
| Week 10 | July 22 - July 28 | Testing, polishing, bug fixing, freeze feature scope |
| Week 11 | July 29 - August 4 | Final documentation, tutorials, and integration checks |
| Week 12 | August 5 - August 11 | Deliver presentation, review feedback, finalize PR for community use |

**Hours/week:** 35-40 hrs

## Communication plan
- Weekly asynchronous updates over GitHub or Zulip
- Bi-weekly live check-ins with mentors via Google Meet
- Use GitHub Issues/PRs for code discussions
- Zulip stream for community feedback and updates

## Personal statement

### Past experience
I am a Master’s student in Computer Science at Cleveland State University, graduating in May 2025. I have worked on numerous Python-based projects in computer vision, pose detection, IoT, and real-time data analysis. My technical foundation includes OpenCV, NumPy, and Django/Flask for backend development. I have also worked with multithreaded systems and developed a motion detection project using sensor feeds in my undergraduate IoT coursework. My GitHub includes several mini-projects that reflect both my interest in automation and practical behavioral analysis.

### Motivation: why this project?
I am passionate about building tools that solve real-world problems in science and medicine. Detecting behaviors from movement is fascinating because it merges signal processing, data analysis, and machine learning in a meaningful context. Automating this process can save researchers hours of work and increase reproducibility in behavioral research. I find it very rewarding to contribute to tools that empower the open science community.

### Match: why you?
I bring a unique combination of analytical thinking, Python fluency, and enthusiasm for behavioral science. I have hands-on experience building sensor-driven motion analysis systems and am comfortable designing full data pipelines. I’m organized, responsive to feedback, and deeply committed to collaborative open-source work. I’ve also handled live coding presentations and documentation, which will help me communicate progress effectively.

### Availability
I will be on my OPT period after graduating in May 2025 and will not have any job conflicts. I am taking one summer course (4–5 hrs/week), which will not interfere with my planned GSoC commitment of 35–40 hours per week. I will be fully available for mentoring, community discussions, and feedback.

## GSoC

### GSoC experience
I expect to gain real-world open source development experience, especially in building tools used by the scientific community. I’m excited to collaborate, learn how to write production-grade code, and become part of an impactful ecosystem. This will strengthen both my software development and research skills.

### Other applications
I am applying only to the NIU organization and am not submitting proposals to any other organizations. This project is my top choice, and I am fully committed to it if selected.

