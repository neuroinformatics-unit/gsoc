## movement: front-end support for filtering module in movement (Harsh Bhanushali)
## Personal details
Please include the following information:
- **Full name: Harsh Rakesh Bhanushali** 
- **Email: bhanushali.harsh203@gmail.com**
- **GitHub username: harsh-bhanushali-05**      
- **Zulip username: harsh bhanushali**
- **Location & time-zone: Panjim, Indian Standard Time (GMT+5:30)**
- **Code contribution**
1) [Made report_nan_stats and calculate_nan_stats more permissive about dimensions.](https://github.com/neuroinformatics-unit/movement/pull/481)
2) [Added support for exporting bboxes in VIA-tracks.](https://github.com/neuroinformatics-unit/movement/pull/497)
3) [Added a Widget for drawing region of interest in napari. feature addition disscussed in #378](https://github.com/neuroinformatics-unit/movement/pull/489)

- **Proposal discussion link**
  
## Project proposal 
_Length: max 1 page_

- **Synopsis**

  This project aims to develop an intuitive napari plugin for Movement’s filtering module, enabling non-programmers to clean and analyze motion-tracking data (e.g., from pose estimation tools like DeepLabCut) through a graphical interface instead of Python scripting. <br><br>
    <u>Why It Matters</u>

    <b>Accessibility Gap</b>: majority biologists/neuroscientists lack coding skills but rely on pose-tracking data.

    <b>Time Efficiency</b>: Manual data cleaning consumes research time; real-time filtering previews could help with this.

    <b>Reproducibility</b>: GUI-driven workflows ensure standardized filtering across labs.

    <b>Open Science</b>: Democratizes advanced tools for underrepresented institutions with limited computational resources.


- **Implementation timeline**

    Please include the following information:
    1. A bullet point list with **minimal set of deliverables** <br> 
    2. ## **Stretch Goals** 
    - **JSON Workflow Export**: Save/load filter configurations  
    - **Hardware Acceleration**: GPU-backed filtering for large datasets  
    - **Community Presets**: Preconfigured settings for common use cases  

    3. ## <b>GSoC 2025:  Timeline</b>

    ## **Community Bonding Period** *(May 8 – June 1)*

    | Week   | Tasks                                                                                   | Hours | Output                         |
    |--------|-----------------------------------------------------------------------------------------|-------|--------------------------------|
    | **CB1** | - Study napari plugin architecture<br>- Draft widget wireframes with mentors | 7     | Environment setup guide       |
    | **CB2** | - Profile existing filter performance<br>- Create UML sequence diagrams for data flow<br>- Setup documentation skeleton with Sphinx | 8     | Technical design doc          |
    | **CB3** | - Finalize widget CSS theme alignment<br>- Write first Jupyter notebook draft| 5     | PR for docs infrastructure    |

    ---

    ## **Coding Period** *(June 2 – August 24)*

    ### **Core Deliverables Timeline**

    | Week   | Focus Area         | Critical Deliverables                                                                 | Hours |
    |--------|--------------------|---------------------------------------------------------------------------------------|-------|
    | **1**  | Widget Framework   | - Base widget class<br>- Confidence threshold UI<br>- Data binding                    | 15    |
    | **2**  | Median Filter      | - Rolling window logic<br>- Performance optimizations<br>- Unit tests                 | 14    |
    | **3**  | SavGol Filter      | - Polynomial order control<br>- Edge mode handling<br>- Benchmark suite               | 16    |
    | **4**  | Preview System     | - Live parameter tuning<br>- Side-by-side visualization<br>- Frame scrubber       | 14    |
    | **5**  | Error Handling     | - Parameter validation<br>- Tooltip explanations<br>- Logging system                  | 13    |
    | **6**  | **Midterm**        | - Cross-platform tests<br>- Performance report<br>- User docs v1                      | 14    |
    | **7**  | Advanced Features  | - Filter chaining logic<br>- Undo/redo stack                                          | 12    |
    | **8**  | Testing              | - Automated screenshot tests<br>- Codecov integration<br>- Release pipeline           | 15    |
    | **9**  | Documentation      | - Video tutorial production<br>- Animated tutorials<br>- Accessibility audit      | 14    |
    | **10** | Optimization       | - Memory leak fixes<br>- Batch processing mode                                        | 12    |
    | **11** | Polish             | - Keyboard shortcuts<br>- Theme consistency<br>- Contributor guide                    | 13    |
    | **12** | Validation         | - Windows/macOS tests<br>- Final benchmark<br>- Release checklist                     | 12    |

   
---
## **Evaluation Checkpoints**


- **Communication plan**

    Please explain: how do you plan to communicate with your mentor? How often? (e.g., daily or weekly stand-ups, longer meetings..?) What communication channels will you use? (e.g., video calls, Zulip chat...?)

## Personal statement

_Length: max 0.75 page_

- **Past experienc.** 

    Please describe your past experience with programming, open source, or any other experience you deem relevant for the project you are applying for. Any successful open source projects, published work or content of the like should definitely be highlighted.
- **Motivation: why this project?**

    Why are you interested in this specific project? What aspects of it motivate you to work on it? How does it link to your personal or professional interests? How do you envision its impact in the open source community?
- **Match: why you?**

    Why should we choose you for this project? What unique skills or experiences can you bring to the project and the community? Is there something you have worked on in the past that makes you particularly well-suited for this project?
- **Availability**

    Please state if you have any other plans for the work period (school work, another job, planned vacation)? If so, how do you plan to combine them with your GSoC work?

## GSoC

_Length: max 0.25 page_

- **GSoC experience**

    What do you expect from the program?

- **Are you also applying to projects with other organisations in GSoC 2025?**

    If so, which ones? What would be your preference in case of a tie?
