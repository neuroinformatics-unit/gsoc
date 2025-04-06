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

---

### Implementation Plan

#### Overview
The goal of this GSoC project is to enhance the `movement` library by:
- Adding a Python implementation of a Kalman filter to smooth position, velocity, and acceleration time-series data, integrating seamlessly with `movement`’s existing data structures (e.g., xarray).
- Optionally extending the Kalman filter to address identity switches in multi-animal tracking data as a stretch goal.
- Providing comprehensive tests, documentation, and an example use case to ensure usability and adoption by the `movement` community.

This plan details the steps to achieve these objectives, including specific code changes, testing strategies, documentation updates, and a timeline with milestones, leveraging my commitment of 30 hours per week over the 12-week GSoC period (late May to mid-August 2025).

---

#### Step 1: Understand the Current Structure
The `movement` codebase is assumed to include:
- A core module for data handling (e.g., pose estimation time-series data, possibly as xarray datasets).
- Utilities for data processing and filtering.
- A test suite (likely using `pytest`) to validate functionality.
- Documentation and a gallery of example use cases.

**Approach:**
- Review the `movement` mission, roadmap, and contributing guide to understand its architecture.
- Identify entry points for integrating Kalman filters (e.g., data ingestion, processing pipelines).
- Study existing data formats (e.g., xarray datasets with position/velocity/acceleration time-series).
- Experiment with sample pose data to understand typical workflows.

**Details:**
- Focus on compatibility with xarray, NumPy, and pandas, as specified in the project requirements.
- Time: Pre-GSoC (15–20 hours self-paced) + Community Bonding (30 hours, late May 2025).

---

#### Step 2: Design and Implement Core Kalman Filter
**Objective:** Create a reusable Kalman filter for smoothing time-series data (position, velocity, acceleration).

**Approach:**
- Implement a new module (e.g., `movement/filters/kalman.py`) with a `KalmanSmoother` class:
  - Attributes: initial state, process noise covariance, measurement noise covariance.
  - Methods: `fit()` (predict/update cycle), `smooth()` (return smoothed time-series).
- Support multiple motion models (e.g., constant velocity, constant acceleration) using state-space representations.
- Use NumPy for efficient matrix operations (e.g., prediction, covariance updates).

**Notes:**
- Configurable parameters will be exposed to users for tuning (e.g., noise levels).
- Initial implementation will be tested with synthetic data (e.g., noisy 2D trajectories).

**Details:**
- Code changes: Add `kalman.py` with core algorithm based on standard Kalman filter equations.
- Time: Weeks 1–2 (June 2–15, 2025, 60 hours).

---

#### Step 3: Integrate Kalman Filter into Movement
**Objective:** Seamlessly integrate the Kalman filter with `movement`’s data pipeline.

**Approach:**
- Extend `movement`’s API:
  - Add a function or method (e.g., `movement.smooth_with_kalman(data, **params)`) that accepts xarray datasets.
  - Ensure input/output compatibility with existing data structures (e.g., xarray.DataArray with time, position dims).
- Handle edge cases (e.g., missing data, irregular time steps) with interpolation or warnings.

**Notes:**
- The API will be modular, allowing future extensions (e.g., other filters).
- Backward compatibility with existing workflows is ensured by making the Kalman filter optional.

**Details:**
- Code changes: Modify `movement`’s core module (e.g., `movement/core.py`) to include the new smoothing function.
- Time: Weeks 3–4 (June 16–29, 2025, 60 hours).

---

#### Step 4: Develop Unit Tests for Core Functionality
**Objective:** Verify the Kalman filter works correctly and integrates with `movement`.

**Approach:**
- Add tests in `movement/tests/` using `pytest`:
  - Test smoothing accuracy on synthetic data (e.g., compare to ground truth).
  - Test edge cases (e.g., missing values, noisy inputs).
  - Test integration with xarray datasets (e.g., correct dims/coords preserved).
- Create utility functions to generate synthetic pose data (e.g., noisy sinusoidal motion).

**Notes:**
- Tests will cover numerical stability (e.g., covariance matrix conditioning) and parameter sensitivity.

**Details:**
- Code changes: Add `test_kalman.py` with test cases.
- Time: Weeks 3–6 (June 16–July 13, 2025, included in 120 hours total).

---

#### Step 5: Document Core Functionality
**Objective:** Provide clear documentation for users and developers.

**Approach:**
- Write docstrings for `KalmanSmoother` and API functions (e.g., parameters, usage).
- Create a usage guide:
  - Explain Kalman filter parameters (e.g., process noise, measurement noise).
  - Provide examples with synthetic/real data.
- Integrate into `movement`’s existing documentation (e.g., Sphinx docs).

**Notes:**
- Documentation will be beginner-friendly, targeting students and new contributors.

**Details:**
- Updates: `movement/docs/` and `movement/filters/kalman.py`.
- Time: Weeks 5–6 (June 30–July 13, 2025, 60 hours).

---

#### Step 6: Create Example Use Case for Gallery
**Objective:** Demonstrate the Kalman filter in a practical context.

**Approach:**
- Develop a Jupyter notebook or script for the `movement` gallery:
  - Input: Synthetic or real pose data (e.g., animal tracking time-series).
  - Process: Apply `smooth_with_kalman()` to noisy data.
  - Output: Visualizations (e.g., matplotlib plots of before/after smoothing).
- Test with mentors and refine based on feedback.

**Notes:**
- The example will highlight the filter’s impact (e.g., reduced noise, smoother trajectories).

**Details:**
- Code changes: Add `examples/kalman_smoothing.ipynb` to gallery.
- Time: Weeks 5–6 (June 30–July 13, 2025, included in 60 hours).

---

#### Step 7: Implement Stretch Goal—Identity Switch Correction
**Objective:** Extend the Kalman filter to fix identity switches in multi-animal tracking.

**Approach:**
- Enhance `KalmanSmoother` or create a new class (e.g., `KalmanTracker`):
  - Track multiple objects using state estimation (position, velocity).
  - Detect swaps via distance metrics or prediction errors.
  - Correct identities by reassigning based on predicted trajectories.
- Test on synthetic multi-animal data (e.g., two animals crossing paths).

**Notes:**
- Requires research into multi-object tracking (e.g., Hungarian algorithm for assignment).
- May integrate with existing pose frameworks (e.g., SLEAP outputs).

**Details:**
- Code changes: Update `movement/filters/kalman.py` or add `kalman_tracker.py`.
- Time: Weeks 7–10 (July 14–August 10, 2025, 120 hours).

---

#### Step 8: Test and Document Stretch Goal
**Objective:** Validate and explain the identity switch functionality.

**Approach:**
- Add `pytest` tests:
  - Test swap detection/correction accuracy on synthetic data.
  - Test robustness with noisy or overlapping trajectories.
- Document the feature:
  - Docstrings for new classes/methods.
  - Usage guide with multi-animal example.

**Notes:**
- Tests will simulate realistic scenarios (e.g., animals crossing in video frames).

**Details:**
- Updates: `movement/tests/test_kalman_tracker.py`, `movement/docs/`.
- Time: Weeks 9–10 (July 28–August 10, 2025, included in 120 hours).

---

#### Step 9: Final Polish and Submission
**Objective:** Ensure all deliverables are production-ready.

**Approach:**
- Refactor code for readability and performance (e.g., optimize matrix operations).
- Run full test suite to catch regressions.
- Polish documentation and gallery examples.
- Prepare GSoC submission:
  - Summary of core and stretch goal work.
  - Links to code, tests, docs, and gallery.

**Notes:**
- Extra time (from 360-hour budget) allows thorough review and mentor feedback.

**Details:**
- Updates: All affected modules, tests, and docs.
- Time: Weeks 11–12 (August 11–24, 2025, 60 hours).

---

#### Step 10: Handle Edge Cases and Performance
**Objective:** Ensure robustness and efficiency.

**Approach:**
- Test with real-world datasets (e.g., from mentors or public sources).
- Optimize for large time-series (e.g., batch processing, memory efficiency).
- Benchmark smoothing and identity correction vs. unfiltered data.

**Notes:**
- Will explore parallelization (e.g., NumPy vectorization) if needed.

**Details:**
- Time: Weeks 9–12 (July 28–August 24, 2025, included in 180 hours total).

---

### Timeline with Milestones
- **Community Bonding (Late May 2025, 30 hours):** Design finalized with mentors.
- **Weeks 1–2 (June 2–15, 60 hours):** Core Kalman filter implemented and tested.
- **Weeks 3–4 (June 16–29, 60 hours):** Integrated into `movement` with tests.
- **Weeks 5–6 (June 30–July 13, 60 hours):** Core deliverables (docs, gallery) completed, mid-term submission.
- **Weeks 7–8 (July 14–27, 60 hours):** Stretch goal prototype developed.
- **Weeks 9–10 (July 28–August 10, 60 hours):** Stretch goal finalized with tests/docs.
- **Weeks 11–12 (August 11–24, 60 hours):** Final polish and submission.
