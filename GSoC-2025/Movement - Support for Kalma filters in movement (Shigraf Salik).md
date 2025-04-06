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
