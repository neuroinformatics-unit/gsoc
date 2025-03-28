

## ethology: Support for Any-Point Tracking (Viet Luong)

## Personal details
Please include the following information:
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

    Please link to the pull request where you discussed your project proposal with the community. 

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

 **Stretch Goals (If time allows)**:
- Real-time inference directly within the napari GUI.
- Integration of additional any-point tracking models.
- Advanced visualization features (trajectory filtering, custom annotations).

**Community Bonding Period (Prep work)**:
- Familiarize thoroughly with napari plugin documentation and development process.
- Set up the development environment.
- Discuss implementation details and milestones with mentors.

**Weekly Timeline**

| Week | Tasks & Deliverables (Detailed)                                                    | Hours |
|------|------------------------------------------------------------------------------------|-------|
| 1    | **Backend setup & initial integration**                                            | 30    |
|      | - Set up development environment (Python, PyTorch, dependencies)                   |       |
|      | - Familiarize with cotracker3/TAPIR models and APIs                                |       |
|      | - Perform initial inference tests on sample video datasets                         |       |
|      | - Document initial setup and installation steps                                    |       |
| 2    | **Backend inference pipeline development**                                         | 30    |
|      | - Implement backend code to run any-point tracking                                 |       |
|      | - Generate basic trajectory data (coordinates across frames)                       |       |
|      | - Conduct initial validations of generated trajectories                            |       |
|      | - Document backend inference pipeline                                              |       |
| 3    | **Backend refinement & debugging**                                                 | 30    |
|      | - Debug and refine inference pipeline                                              |       |
|      | - Improve robustness and error handling                                            |       |
|      | - Ensure stable integration of cotracker3/TAPIR inference                          |       |
|      | - Create backend unit tests                                                        |       |
| 4    | **Trajectory data export functionality**                                           | 30    |
|      | - Develop trajectory data export methods (CSV, JSON formats)                       |       |
|      | - Validate data export formats and consistency                                     |       |
|      | - Integrate export functionality into backend system                               |       |
|      | - Document export process clearly                                                  |       |
| 5    | **Frontend: Initial napari widget setup**                                          | 30    |
|      | - Design basic napari plugin structure                                             |       |
|      | - Implement video loading interface                                                |       |
|      | - Develop query point selection and storage functionality                          |       |
|      | - Document widget installation and basic usage                                     |       |
| 6    | **Frontend-backend integration & mid-term report**                                 | 30    |
|      | - Connect napari frontend widget with backend inference system                     |       |
|      | - Verify successful end-to-end tracking from widget interface                      |       |
|      | - Write and submit mid-term progress report                                        |       |
| 7    | **Trajectory visualization overlays within napari**                                | 30    |
|      | - Implement visualization overlays of trajectories onto loaded videos              |       |
|      | - Ensure accurate mapping of tracked points                                        |       |
|      | - Validate visualization correctness                                               |       |
| 8    | **Visualization interactivity improvements**                                       | 30    |
|      | - Implement interactive functionalities (zoom, pan, overlay toggles)               |       |
|      | - Enhance user experience with responsive UI                                       |       |
|      | - User testing and feedback collection                                             |       |
| 9    | **Optimization, performance testing & bug fixing**                                 | 30    |
|      | - Optimize inference speed and resource usage                                      |       |
|      | - Conduct extensive performance benchmarks                                         |       |
|      | - Address identified performance bottlenecks                                       |       |
|      | - Fix any remaining frontend/backend bugs                                          |       |
| 10   | **Detailed documentation and user guide preparation**                              | 30    |
|      | - Complete comprehensive backend/frontend documentation                            |       |
|      | - Write detailed user guides/tutorials                                             |       |
|      | - Prepare usage examples                                                           |       |
| 11   | **Code freeze, final testing, and submission preparation**                         | 30    |
|      | - Conduct final comprehensive tests                                                |       |
|      | - Address any critical bugs or performance issues                                  |       |
|      | - Begin preparation of final submission materials                                  |       |
| 12   | **Final feedback incorporation & project submission**                              | 30    |
|      | - Incorporate mentor and community feedback                                        |       |
|      | - Finalize and polish all documentation                                            |       |
|      | - Submit final deliverables                                                        |       |


**Total Project Duration:** 12 weeks × 30 hours/week = **~360 hours**

**Note:** No vacations or major commitments planned; weekly hours and tasks may adjust slightly based on mentor feedback and project progress.   

- **Communication plan**

- **Frequency:** Weekly stand-up meetings for updates and progress reviews; additional brief daily or bi-weekly check-ins via chat as needed.
- **Channels:** Regular video calls (Zoom/Google Meet) for weekly discussions; continuous communication and quick queries via Zulip or GitHub issues.
## Personal statement

_Length: max 0.75 page_

- **Past experienc.** 

I have a robust background in programming, open-source development, and research, highlighted by my ongoing roles as a Research Assistant at Yin Li’s Lab and Vikas Singh’s Lab at the University of Wisconsin-Madison. At Yin Li’s Lab, I designed and implemented algorithms to generate precise region prompts for the MedSAM model, enhancing localization accuracy in medical X-ray images. Additionally, I successfully applied CLIPSelf to improve dense feature representation, significantly boosting the model's accuracy.

At Vikas Singh’s Lab, I focused on hyperparameter tuning and model optimization for the SimpleTM model, executing extensive experiments on datasets such as PEMS and M4. Utilizing JAX and Triton frameworks, I optimized model efficiency, improving speed per iteration by sixfold. My published work at the International Conference on Representation Learning (ICLR 2025) reflects these efforts, establishing new benchmarks in multivariate time-series forecasting.

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

 I am consider between two projects from ethology repo
