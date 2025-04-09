# Neuroinformatics Unit: Movement
# Personal Details

- **Full name:** Shigraf Salik
- **Email:** salikshigraf@gmail.com
- **GitHub username:** ShigrafS
- **Zulip username:** ShigrafS (User ID 882394 )
- **Location & time-zone:** Kolkata, India. IST.
- **Code contribution:**
    
    https://github.com/neuroinformatics-unit/movement/pull/480

- **Proposal discussion link:**

    https://github.com/neuroinformatics-unit/gsoc/pull/72
    

# Project Proposal 

## *Synopsis*

The goal of this project is to add Kalman filter support to the movement Python library to enhance its capabilities for cleaning and filtering pose estimation data. Kalman filters are powerful tools for smoothing noisy time-series data and estimating latent states such as velocity and acceleration. This project will provide a modular, extensible Kalman filter implementation that can be used to post-process tracking data, improving data quality for downstream behavioral analysis.

Initially, the Kalman filter will be used to smooth position, velocity, and acceleration time series. As a stretch goal, the implementation may also be extended to help resolve identity switches in multi-animal tracking scenarios—a common challenge in pose estimation pipelines. The project will include robust testing, thorough documentation, and example use cases to ensure usability and reproducibility. The implementation may be developed from scratch or built by wrapping an existing Python library, depending on design discussions with mentors. Overall, this project aims to make movement more powerful, flexible, and user-friendly for researchers and practitioners working with animal tracking data.


### ✅ **Core Deliverables**

1. **Python implementation of Kalman Filter for time-series smoothing**
   - Smoothing of **position**, **velocity**, and **acceleration** data.
   - Configurable parameters: initial state, process/measurement noise.
   - Optional: user-selectable motion models (e.g., constant velocity/acceleration).

2. **Modular API integrated into `movement`**
   - Easy-to-use functions or class-based interface.
   - Compatible with existing `movement` data structures (ideally supporting `xarray`).

3. **Unit tests covering new functionality**
   - Tests for correct filtering on synthetic and sample datasets.
   - Tests for edge cases and numerical stability.

4. **Documentation**
   - Docstrings for all new classes/functions.
   - Usage guide and explanation of Kalman filter parameters.
   - Integration with `movement`'s existing documentation.

5. **Example use case in movement gallery**
   - Demonstration notebook or script using real or synthetic pose data.
   - Before/after comparison with and without filtering.

---

### 🎯 **Stretch Deliverable (Optional: Only if the above list is completed before deadline)**

6. **Kalman filter for identity switch correction**
   - Detect and correct identity mismatches in multi-animal tracking.
   - Use temporal coherence to maintain identity over time.
   - Basic working prototype is sufficient for this goal.


#### Implementation Timeline
**Duration:** ~175 hours (12 weeks, 14.5 hours/week approx, late May to mid-August 2025)  

---

### Pre-GSoC Preparation (April–May 2025)
- **Goal:** Build foundational knowledge and setup.
- **Tasks:**
  - Explore `movement` codebase, mission, roadmap, and contributing guide.
  - Study Kalman filter theory (e.g., KalmanFilter.NET, linear dynamical systems).
  - Review Python libraries (`pykalman`, `dynamax`, `darts`) for potential reuse.
  - Experiment with pose estimation data (e.g., DeepLabCut, SLEAP formats).
  - Install development tools (Python, NumPy, pandas, xarray, pytest).
- **Time Estimate:** Self-paced, ~15–20 hours before GSoC.

---

### Community Bonding Period (Late May 2025, ~2 weeks)
- **Goal:** Align with mentors and finalize design.
- **Tasks:**
  - Engage with `movement` community and mentors (@niksirbi, @sfmig).
  - Decide on implementation approach (from scratch vs. wrapping).
  - Design API (e.g., class-based `KalmanSmoother`, xarray integration).
  - Generate or source synthetic datasets for testing.
  - Draft detailed milestones with mentor input.
- **Time Estimate:** 30 hours (15 hours/week over 2 weeks).

---

### Coding Phase: Week 1–2 (June 2–15, 2025)
- **Goal:** Develop core Kalman filter for time-series smoothing.
- **Tasks:**
  - Implement Kalman filter algorithm:
    - Smooth position, velocity, acceleration time-series.
    - Configurable parameters (initial state, noise covariances).
    - Support multiple motion models (constant velocity, constant acceleration).
  - Use NumPy for efficient computation.
  - Create synthetic datasets (e.g., noisy 2D trajectories).
  - Write initial `pytest` unit tests (filter accuracy, parameter tuning).
- **Deliverables by End of Week 2:**
  - Functional Kalman filter prototype.
  - Basic tests passing on synthetic data.

---

### Coding Phase: Week 3–4 (June 16–29, 2025)
- **Goal:** Integrate into `movement` and enhance functionality.
- **Tasks:**
  - Build modular API (e.g., `KalmanSmoother` class).
  - Ensure compatibility with `movement`’s xarray-based data structures.
  - Add edge-case handling (e.g., missing data, outliers).
  - Expand test suite:
    - Integration tests with `movement` data.
    - Numerical stability and edge-case tests.
  - Draft comprehensive docstrings and usage guide.
- **Deliverables by End of Week 4:**
  - Fully integrated Kalman filter in `movement`.
  - Robust test coverage.
  - Preliminary documentation.

---

### Coding Phase: Week 5–6 (June 30–July 13, 2025)
- **Goal:** Finalize core deliverables and prepare mid-term evaluation.
- **Tasks:**
  - Optimize performance (e.g., vectorization, profiling).
  - Complete unit tests for all core features.
  - Finalize documentation:
    - Detailed parameter explanations.
    - Integration into `movement` docs.
  - Develop gallery example:
    - Notebook/script with pose data (real or synthetic).
    - Visualizations (before/after smoothing).
  - Submit mid-term progress for mentor review.
- **Deliverables by End of Week 6:**
  - Polished core implementation (smoothing, tests, docs, example).
  - Mid-term evaluation submission.

---

### Coding Phase: Week 7–8 (July 14–27, 2025)
- **Goal:** Begin stretch goal—Kalman filter for identity switches.
- **Tasks:**
  - Research identity switch issues in multi-animal tracking.
  - Design solution:
    - Use Kalman filter to predict trajectories and correct swaps.
    - Handle multi-object state estimation.
  - Implement prototype:
    - Test on synthetic multi-animal data (e.g., two animals crossing paths).
    - Integrate with `movement` data pipeline.
  - Write initial tests for identity switch correction.
- **Deliverables by End of Week 8:**
  - Working prototype for identity switch fixing.
  - Basic tests for stretch goal.

---

### Coding Phase: Week 9–10 (July 28–August 10, 2025)
- **Goal:** Complete stretch goal and refine all deliverables.
- **Tasks:**
  - Polish identity switch implementation:
    - Optimize for real-world data (e.g., from SLEAP or idtracker).
    - Add configurable parameters (e.g., swap detection threshold).
  - Expand test suite for stretch goal (accuracy, robustness).
  - Document stretch goal:
    - Docstrings and usage guide.
    - Add to `movement` docs.
  - Enhance gallery example:
    - Include identity switch demo (e.g., before/after tracking fix).
- **Deliverables by End of Week 10:**
  - Fully functional stretch goal implementation.
  - Complete tests and docs for identity switches.
  - Updated gallery with dual examples (smoothing + identity fix).

---

### Coding Phase: Week 11–12 (August 11–24, 2025)
- **Goal:** Final polish and submission.
- **Tasks:**
  - Address all mentor feedback from prior weeks.
  - Conduct thorough code review and refactoring.
  - Ensure all tests pass and meet `movement` standards.
  - Finalize documentation and gallery examples.
  - Prepare GSoC submission:
    - Summary of core and stretch goal work.
    - Links to code, tests, docs, and gallery.
  - Submit final work to GSoC platform and mentors.
- **Deliverables by End of Week 12:**
  - All deliverables (core + stretch) completed and submitted.
  - Final project submission.

---

### Total Time Breakdown
- **Pre-GSoC Prep:** ~15–20 hours (self-paced, not counted in GSoC).
- **Community Bonding:** 30 hours.
- **Grand Total (GSoC Period):** 175 hours.

---

### Notes
- **Mentor Sync:** Plan for 1–2-hour weekly check-ins with @niksirbi and @sfmig.

---

### Implementation Plan

This project will implement a Kalman filter in movement via a KalmanSmoother class for smoothing time-series data, integrated as a modular API (e.g., movement.smooth_with_kalman()), with pytest-based tests, documentation, and a gallery example. A stretch goal will extend it to a KalmanTracker for identity switch correction in multi-animal tracking. 
Testing will be obsessive - I learned the hard way during refactoring how pose data can break in edge cases.
For full technical details, see: https://gist.github.com/ShigrafS/10ecbf75efcbe3f57672527be004d995 

### **Risk Mitigation Plan**  

The trickiest part will be avoiding numerical instability—I once crashed a filter by underestimating covariance bounds during my EEG work. I’ll use scipy.linalg’s stabilized solvers and test with intentionally noisy spirals (like kinematics.py’s worst-case examples). If this fails, pykalman’s battle-tested math can be a fallback, though I’d lose some flexibility. For identity switches, I’ll start with 2-animal crossings since PR #480’s refactor taught me how movement handles paired trajectories. If time runs short, I’ll document a ‘swap_score’ threshold for manual review

---

### Timeline with Milestones
- **Community Bonding (Late May 2025, 30 hours):** Design finalized with mentors.
- **Weeks 1–2 (June 2–15):** Core Kalman filter implemented and tested.
- **Weeks 3–4 (June 16–29):** Integrated into `movement` with tests.
- **Weeks 5–6 (June 30–July 13):** Core deliverables (docs, gallery) completed, mid-term submission.
- **Weeks 7–8 (July 14–27):** Stretch goal prototype developed.
- **Weeks 9–10 (July 28–August 10):** Stretch goal finalized with tests/docs.
- **Weeks 11–12 (August 11–24):** Final polish and submission.

---

### Communication Plan
I plan to communicate with my mentors (@niksirbi, @sfmig) through weekly synchronous check-ins via video call (Zoom or Google Meet) to discuss progress, blockers, and next steps. These meetings will be scheduled at a mutually convenient time. For daily updates and asynchronous discussions, I will use the `NIU` community’s preferred platform Zulip and email to share progress reports, ask questions, and seek feedback. I’ll provide detailed updates at least twice a week, including code snippets, test results, or documentation drafts as needed. I’ll also be responsive to mentor messages within 24 hours and remain flexible for ad-hoc discussions if urgent issues arise. My goal is to maintain clear, proactive communication to ensure alignment throughout the GSoC period.

---

### Personal Statement

#### Past Experience
I have previously interned at a medical AI startup, where I trained models to diagnose neurological disorders such as epilepsy, where I worked on large medical datasets and EEG files to train models. There I also learnt signal processing and Cloud Computing. Apart from this, I have also worked on Text-to-Speech models and OCR models for local languages. 

#### Motivation: Why This Project?
This project aligns closely with my interests in data science and signal processing. While refactoring kinematics.py (PR #480), I realised that implementing Kalman filters would greatly enhance `Movement's` capabilities as they could directly smooth such artifacts while preserving true motion patterns I've seen in real datasets. Having previously worked in similar fields, I’m motivated by the potential impact of cleaner, more reliable tracking data on scientific research, particularly in fields like neuroscience or ecology, all the while learning from my mentors. 

#### Match: Why Me?
My familiarity with machine learning in the field of neurology, combined with a proactive learning mindset, makes me confident I can deliver both the core deliverables and the stretch goal. I’ve already demonstrated my commitment through working on the movement codebase, and I’m prepared to dive deeper into pose estimation frameworks or state-space modeling as needed. My experience with neurological data at a startup ensures I can produce high-quality, maintainable contributions that align with movement’s standards.
I would also like to add, during my time at a stealth startup, I worked with biomedical signals, giving me firsthand experience with state-space filtering challenges similar to pose tracking. 

#### Availability
I have no major academic or job commitments during the GSoC period (late May to mid-August 2025) and can dedicate 175 hours per week to this project as required. I can, if required dedicate more time to ensure the projet's success. In case of minor overlaps (e.g., exams or personal events), I will plan ahead to maintain my weekly hours and inform my mentors in advance via our agreed communication channels. My schedule is flexible, allowing me to adjust work hours to accommodate mentor availability or project needs. 

---

#### GSoC Experience
Through GSoC, I hope to gain real-world experience working in a collaborative development environment, improve my design and coding skills, and contribute to an open-source ecosystem that aligns with my interests in application of machine learning and its application in neurology. I’m excited to learn from experienced mentors, refine my ability to write production-ready code, and deepen my understanding of signal processing and tracking algorithms. This project with NIU’s movement is an ideal opportunity to grow as a developer while making a tangible impact on a tool used by researchers worldwide. 

I'm applying to this project because of my passion for machine learning and neuroinformatics and to get started with Open-Source Contributions. 
