# ethology: Support for Any-Point Tracking (Richard Dushime Mudahera)

## Personal Details
- **Full name:** Richard Dushime Mudahera
- **Email:** mudaherarich@gmail.com
- **GitHub username:** richarddushime
- **Zulip username:** Richard Dushime
- **Location & time-zone:** Italy, GMT+1
- **Personal website / project portfolio:** [Personal Website](https://richarddushime.netlify.app/)
- **Code contribution:** 
    - [Add basic setup for documentation #56](https://github.com/neuroinformatics-unit/ethology/pull/56)
    - [Set up dependabot to check for updates in GH actions PR #64](https://github.com/neuroinformatics-unit/ethology/pull/64)
    - [supporting image registration with Elastix #66 --In progress](https://github.com/neuroinformatics-unit/ethology/pull/66)
    - [Automate collection of papers citing BrainGlobe tools #295](https://github.com/brainglobe/brainglobe.github.io/pull/295)  
    - [Pin setuptools lower bound to >v64 #141](https://github.com/neuroinformatics-unit/python-cookiecutter/pull/141)
    - [Deploy on: main branch pushes OR tags OR manual trigger #140](https://github.com/neuroinformatics-unit/python-cookiecutter/pull/140)
    - [Add website #134](https://github.com/neuroinformatics-unit/python-cookiecutter/pull/134)
    - [Retrieve version in docs [In ref to PR #75 ] #76](https://github.com/neuroinformatics-unit/ethology/pull/76)
    
- **Proposal discussion link:** [Discussion PR #12 ](https://github.com/neuroinformatics-unit/gsoc/pull/12)

## Project Proposal

### Synopsis
Animal behavior research increasingly relies on computer vision, yet advanced tools like any-point tracking—which tracks arbitrary points in videos—remain underutilized due to accessibility gaps. While pose estimation focuses on predefined anatomical keypoints, any-point tracking offers dynamic, flexible analysis, enabling researchers to study novel behaviors, environmental interactions, or ad-hoc body parts. 

This project integrates any-point tracking—a computer vision (CV) technique that tracks arbitrary points in videos—into Ethology, an open-source framework for analyzing animal behavior. Unlike traditional pose estimation (which tracks fixed anatomical keypoints), any-point tracking allows researchers to dynamically select points (e.g., limbs, environmental objects) and trace their motion across video frames.

### Why is it important?

- **Flexibility**:
  Any-point tracking lets scientists choose any point in a video instead of being limited to fixed body parts. For example:
    - **A moving animal recorded with a non-static camera**: Researchers can track background points to estimate camera motion and then subtract it, isolating the animal’s true motion.
    - **Deformable surfaces**: using a grid of points, scientists can measure subtle changes in an animal’s face or track the flexible body of a cuttlefish.
    - **Tool use or social interactions**: Points can be placed on tools or in social scenes, allowing researchers to study how these elements move and interact over time.

- **Accessibility**:
    The tool will be designed with a simple graphical interface (using [Napari](https://napari.org/stable/index.html)) so that even those with little or no coding experience can use advanced computer vision techniques. Clear documentation and step-by-step tutorials will guide users through video loading, point selection, and analysis.

- **Efficiency**:
    Advanced models like [TAPIR](https://deepmind-tapir.github.io/) can predict the paths of selected points automatically. This speeds up the labeling process because:

    - The tool can suggest trajectories for points of interest.
    - Users can review and correct these suggestions where needed, with a built-in confidence score highlighting sections that may need closer checking.
    - This reduces the time and effort needed for manual annotation, which is particularly useful in long-term or large-scale studies.

- **Interoperability**:
    The tracking outputs will be saved like [movement datasets](https://movement.neuroinformatics.dev/user_guide/movement_dataset.html), This makes it easy to integrate with other analysis tools and tasks—such as object detection—and allows, for a seamless flow of data between different NIU tools. It means that the results can be used for further and analysis,

### Goals

- **User Interface:** Develop a user-friendly Napari widget that allows video loading, point selection, and visualizes tracking results.
- **Back-End Integration:** Connect the widget to pre-trained any-point tracking models (e.g., TAPIR, CoTracker3) and convert their outputs into datasets format  like [movement datasets](https://movement.neuroinformatics.dev/user_guide/movement_dataset.html).

- **Data Analysis:** Enable analysis and export of trajectories in common formats (NIU tools formats) for further research.
- **Extended Functionality (Stretch Goal):**  
  - Allow model inference to be run directly from the Napari GUI.
  - Implement manual trajectory correction tools.

### Deliverables

1. Napari Widget Prototype:
   - Load video files (MP4, AVI).  
   - Simple interface to select and manage query points.  
   - Overlay of tracked trajectories on the video.

2. Back-End Functionality:
   - Integrate pre-trained models like [TAPIR](https://deepmind-tapir.github.io/) and [CoTracker3](https://cotracker3.github.io/).  
   - Convert raw tracking outputs into Ethology-compatible datasets.

3. Data Analysis Tools:
   - Export trajectories in CSV/HDF5 formats.  
   - Basic visualization and statistics (e.g., velocity, heatmaps).

4. Documentation & Testing:  
   - Detailed user guides and API documentation.  
   - Automated tests with GitHub Actions.

5. **Stretch Goals:**  
   - Run model inference from within Napari.  
   - Add tools for manual trajectory correction.

## Implementation Timeline

#### Minimal Deliverables

1. Core Napari Widget
    - Load MP4/AVI/TIFF videos.
    - Select points via:
      - Interactive GUI (click/drag).
      - CSV file upload (columns: frame, x, y).
    - Grid generation (user-defined rows/columns).
    - Integration with Movement:
        - Store query points as xarray.DataArray with coordinates (time, space, keypoints, individuals).

2. Backend Integration
  - Python API to run TAPIR/CoTracker on videos (CPU/GPU).
  - Convert raw trajectories to `movement.PoseTracks` format:

##### Stretch Goals
1. Manual Trajectory Correction:
    - GUI tools to drag-and-adjust points; updates propagate to ds.position.
2. Multi-Model Support:
    - Integrate CoTracker for comparison; allow model switching via API/GUI.
3. Batch Processing:
    - Process multiple videos in parallel; output concatenated xarray.Dataset.
4. Benchmarking Suite: Compare model accuracy on animal datasets.
  - Metrics:
      - Tracking Accuracy (TA): Euclidean distance (px) from ground truth.
      - Occlusion Robustness (OR): Accuracy after synthetic occlusion.
      - FPS: Processing speed on GPU/CPU.
---

| **Week** | **Tasks** | **Deliverables** | **Hours** |  
|----------|-----------|------------------|-----------|  
| **Community Bonding**    | Engage in discussions on Zulip and GitHub, contribute minor bug fixes, and review napari plugins and documentations (including cotracker3 and TAPIR). |  |  
| **1**    | **Backend Setup** <br> - Integrate TAPIR API. <br> - Handle video I/O (MP4/AVI/TIFF). | Python function to run TAPIR on a video. | 30 |  
| **2**    | **Data Conversion** <br> - Map TAPIR outputs to `movement.PoseTracks`. <br> - Add timestamps and confidence scores. | Trajectories compatible with `movement.io.read_poses()`. | 30 |  
| **3**    | **Point Selection API** <br> - Implement CSV/grid point loading. <br> - Unit tests for data validation. | Users can load points programmatically. | 30 |  
| **4**    | **Napari Widget Core** <br> - Video loading + frame navigation. <br> - Basic point selection UI. | Widget prototype (no tracking). | 30 |  
| **5**    | **Model Integration** <br> - Connect widget to TAPIR backend. <br> - Add progress bars. | End-to-end tracking in Napari. | 30 |  
| **6**    | **Mid-Term Review** <br> - Optimize GPU batch processing. <br> - Demo: Zebrafish tracking case study. | 50% code coverage, 2x speedup on GPU. | 30 |  
| **7**    | **Export & Analysis** <br> - CSV/HDF5 export. <br> - Integrate with `movement.kinematics.compute_velocity()`. | Trajectories work in Ethology tutorials. | 30 |  
| **8**    | **Documentation** <br> - Write user guides. <br> - Create video tutorials. | Docs cover loading, tracking, export. | 30 |  
| **9**    | **Stretch: CoTracker Integration** <br> - Add model switching. <br> - Benchmark vs. TAPIR (accuracy/FPS). | CoTracker support in API + widget. | 30 |  
| **10**   | **Stretch: Trajectory Correction** <br> - GUI tools to edit points. <br> - Undo/redo functionality. | Users can fix tracking errors in Napari. | 30 |  
| **11**   | **Edge Cases & Testing** <br> - Handle occlusions (linear interpolation). <br> - Stress-test . | Beta version with bug fixes. | 30 |  
| **12**   | **Finalization** <br> - CI/CD (GitHub Actions). <br> - Final touches and presentation. <br> - Final Blogpost | Code merged, full test coverage. | 30 |  
| **Continued Community Engagement**   |  - Stay active as a community contributor by addressing bugs, offering support, and enhancing features as needed.<br> - Provide assistance through forums, Zulip, and GitHub for users adopting the tool.<br> - Monitor feedback and plan follow-up in agreement with mentors.<br> - Act as a resource for new contributors and maintain a connection with mentors. | 30 |  

---

### Key Milestones

1. Backend Integration & Movement Dataset Compliance
    - Trajectories from TAPIR successfully converted to movement.PoseTracks format.
2. Tracking in Napari
    - Users can load videos, select points, and visualize trajectories directly in Napari.
   - First user-facing prototype validates core functionality and usability.
3. Final Delivery with Full Test Coverage

### Acknowledgment

While the timeline above outlines an ideal progression, I recognize that unforeseen challenges or complexities may require adjustments along the way. **I am fully committed to delivering all core deliverables and stretch goals outlined in this proposal**. If delays arise, I will proactively compensate by:
- Prioritizing critical tasks 
- Adjusting time allocation 
- Communicating early with mentors to collaboratively resolve blockers.

### Communication Plan
- **Mentor Meetings:** Hold weekly video or voice calls to discuss progress, challenges, and next steps.
- **Daily standups** to share the progress and challenges 
- **Daily/Weekly Updates/Devlogs:** Share progress and ask quick questions on Zulip.
- **Documentation & Issue Tracking:** Use GitHub Issues and project boards to track tasks and milestones.
- **Code Reviews:** Submit regular or weekly pull requests to ensure the project stays on track and meets community standards.

## Personal Statement

### Past Experience
I have built a good foundation in Python and computer vision by contributing on different open source projects as shown [here](https://github.com/richarddushime) . My contributions to NIU repositories show that I can work well with open source communities(listed above). While I am still learning machine learning and using PyTorch [eg: EDA and Prediction on GDS Energy ](https://www.kaggle.com/code/dushimerichard/eda-and-prediction-on-gds-energy), and I am eager to learn more. I have worked on projects that required both research-level and production-quality code. and Now, as a Master’s student in Data Science at the University of Messina, I focus on machine learning and research software engineering. I have also contributed to several open-source projects, including a Flask web app for WEHI’s Research Software Engineer Internship program [link](https://wehi-researchcomputing.github.io/). In addition, I have taken part in initiatives like [FORRT (Framework for Open and Reproducible Research Training)](https://forrt.org/), and [Open Life Science as a mentee in OLS7](https://www.linkedin.com/pulse/transformative-insights-my-journey-through-ols-program-richard/?trackingId=LyfPkgj%2BQyeuTyusLADSLA%3D%3D) and facilitator OLS cohort 8. Attending events like the [Collaborations Workshop 2024(see this post)](https://www.linkedin.com/posts/richard-dushime_collabw24-cw25-organizers-activity-7191877793553534976-r-M1?utm_source=share&utm_medium=member_desktop&rcm=ACoAADCUoxQBnuteBtFFiwZDz_mJXZ_HkdVBe7g) and serving as [Secretary for RSE Asia & Australia](https://rseaa.org/RSEAA24) which has deepened my interest in software sustainability and research projects and tools.


### Motivation: Why This Project?
Animal behavior research often uses tools that focus on a fixed set of keypoints. For example, DeepLabCut and SLEAP work well for model organisms like mice, rats, and fruit flies where the anatomy is relatively consistent. However, these tools may struggle with flexible animals such as octopuses or cuttlefish, which can change shape dramatically, or with species like snakes and certain birds that have unusual body structures.

Any-point tracking offers a more flexible alternative. Instead of being limited to fixed body parts, it allows researchers to choose and track any point in a video. This capability can be especially valuable when:
- Studying animals in natural settings: For example, when an animal is recorded with a moving camera, tracking points in both the animal and the background helps separate camera motion from the animal’s motion.
- Analyzing deformable subjects: By tracking a grid of points, researchers can measure subtle changes in an animal's face or the flexible body of species like cuttlefish.
- Exploring new research questions: The flexibility to select any point opens up possibilities to investigate behaviors or interactions that were previously hard to quantify with fixed-keypoint methods.

Ethology’s goal of unifying different computer vision tasks under one easy-to-use interface aligns with my belief that accessible, adaptable tools can greatly enhance scientific discovery. I am excited about this project because it will enable researchers to ask new questions and gain deeper insights into animal behavior by leveraging the advanced capabilities of any-point tracking.

### Match: Why Me?
I am eager to learn and  learning more about machine learning and data visualization through hands on experiences. and I have solid skills in Python, which I have developed through open source contributions, formal coursework, and personal learning projects (see my Past Experience section for more details). My experience in writing clear and useful code, both for research and for production, makes me a good fit for this project. I am eager to learn more and learn about the napari ecosystem and to use my skills to build high-quality software that meets the needs of animal behavior research. I believe my background and passion for open-source development will help me make a positive contribution to this project.Additionally, my ongoing studies in data science supported by both academic coursework and hands-on projects, further strengthen my technical foundation. 

### Availability
- Full-time Commitment: 30+ hrs/week, with no vacations/conflicts.
- Contingency Plan: Buffer hours into weekends to accommodate unexpected delays.

## GSoC

### GSoC Experience
I view GSoC as a unique opportunity to enhance my skills and contribute to a project that bridges cutting-edge research with practical applications. I am eager to collaborate with  mentors and the open source community, learn from their experience, and contribute to a tool that can make a real difference in the field of animal behavior research.

### Applying to Other Projects
I am applying to this project only under the Neuroinformatics Unit:
- Ethology (any-point tracking integration).

Due to the direct alignments with my skills and interests and passion for making advanced analysis tools accessible to researchers.
