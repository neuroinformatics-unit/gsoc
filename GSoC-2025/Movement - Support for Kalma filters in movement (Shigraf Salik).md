# Personal Details

- **Full name:** Shigraf Salik
- **Email:** salikshigraf@gmail.com
- **GitHub username:** ShigrafS
- **Zulip username:** ShigrafS (User ID )
- **Location & time-zone:** Kolkata, India. IST.
- **Code contribution:**
    
    https://github.com/neuroinformatics-unit/movement/pull/480

- **Proposal discussion link:**

    https://github.com/neuroinformatics-unit/gsoc/pull/
    

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
**Duration:** ~360 hours (12 weeks, 30 hours/week, late May to mid-August 2025)  

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

### Community Bonding Period (Late May 2025, ~2 weeks, 30 hours)
- **Goal:** Align with mentors and finalize design.
- **Tasks:**
  - Engage with `movement` community and mentors (@niksirbi, @sfmig).
  - Decide on implementation approach (from scratch vs. wrapping).
  - Design API (e.g., class-based `KalmanSmoother`, xarray integration).
  - Generate or source synthetic datasets for testing.
  - Draft detailed milestones with mentor input.
- **Time Estimate:** 30 hours (15 hours/week over 2 weeks).

---

### Coding Phase: Week 1–2 (June 2–15, 2025, 60 hours)
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
- **Time Estimate:** 60 hours (30 hours/week).

---

### Coding Phase: Week 3–4 (June 16–29, 2025, 60 hours)
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
- **Time Estimate:** 60 hours.

---

### Coding Phase: Week 5–6 (June 30–July 13, 2025, 60 hours)
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
- **Time Estimate:** 60 hours.

---

### Coding Phase: Week 7–8 (July 14–27, 2025, 60 hours)
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
- **Time Estimate:** 60 hours.

---

### Coding Phase: Week 9–10 (July 28–August 10, 2025, 60 hours)
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
- **Time Estimate:** 60 hours.

---

### Coding Phase: Week 11–12 (August 11–24, 2025, 60 hours)
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
- **Time Estimate:** 60 hours.

---

### Total Time Breakdown
- **Pre-GSoC Prep:** ~15–20 hours (self-paced, not counted in GSoC).
- **Community Bonding:** 30 hours.
- **Core Deliverables (Weeks 1–6):** 180 hours.
- **Stretch Goal (Weeks 7–10):** 120 hours.
- **Final Polish (Weeks 11–12):** 60 hours.
- **Grand Total (GSoC Period):** 360 hours (30 hours/week × 12 weeks).

---

### Notes
- **Buffer Time:** With 360 hours vs. the 175-hour baseline, I have ~185 extra hours. This is allocated to:
  - Deeper stretch goal development (identity switches).
  - Additional polish (optimization, edge cases, documentation).
  - Learning curve or unexpected challenges (e.g., xarray integration).
- **Weekly Commitment:** 30 hours/week is evenly distributed, with flexibility to shift hours (e.g., 25 one week, 35 the next) if needed.
- **Mentor Sync:** Plan for 1–2-hour weekly check-ins with @niksirbi and @sfmig.
