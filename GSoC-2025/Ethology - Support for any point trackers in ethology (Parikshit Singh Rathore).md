## Personal details

- **Full name** Parikshit Singh Rathore
- **Email** 14.parikshitsingh@gmail.com
- **GitHub username** parikshit14
- **Zulip username** PSRathore
- **Location & time-zone** Bengaluru, India | IST (GMT +5:30)
- **Personal website / project portfolio** https://sites.google.com/view/parikshit-singh-rathore
- **Code contribution**

    1. https://github.com/neuroinformatics-unit/ethology/pull/58 (Support for Tracking-Any-Point)
    2. https://github.com/neuroinformatics-unit/movement/pull/526 (Aggregating multiple source for better trajectory)
    3. https://github.com/brainglobe/cellfinder/pull/494 (Sub-volume crop support for cell detection)
    4. https://github.com/brainglobe/brainglobe-workflows/pull/145 (Workflow update to rectify failing test of sub-volume crop)

- **Proposal discussion link**
    https://github.com/neuroinformatics-unit/gsoc/pull/54

## Project proposal 
_Length: max 1 page_

- **Synopsis**

    Understanding complex motion in a scenario and the physical interaction with it, is a fundamental task in computer vision, and of great importance to video object tracking, segmentation, action recognition, and physical world understanding. Previously solved using optical-flow, but fails during occlusion. Thats where Tracking-Any-Point (TAP) models have gained recent popularity, not only because of there ability to model long range point motion which can include occlusion but also its ability to track any diverse set of points. Any-point trackers enable detailed monitoring of animal movements and behaviors for ethological studies. The aim of this proposal is to add support of the Tracking-Any-Point in the ethology repository to enable researcher track keypoints/individuals and further facilitate analysis using a sister repository `movement`. TAP is particularly important because that will enable researchers to analyse how the animal is moving even in moving camera conditions (by subtracting relative camera motion by applying TAP on the background points). With the possibility to add all functionalities like detection, tracking, and TAP will create an uncanny under one hood repository for ethological researchers to be benefitted.


- **Implementation timeline**

    **Deliverables**:
    - Add support for SOTA track-any-point models to `ethology`. Current SOTA include [LocoTrack](https://arxiv.org/abs/2407.15420), and [BootsTAP](https://openaccess.thecvf.com/content/ACCV2024/papers/Doersch_BootsTAP_Bootstrapped_Training_for_Tracking-Any-Point_ACCV_2024_paper.pdf) depending upon the feasibility, compatibility and ease of use with `ethology`

    - Napari support to interact with TAP models
        1. Drop-down for supported trackers
        2. Query modes: Grid (with customizable size) / specific query points / default query points (like the center of the video)
        3. Load videos, project the first frame, custom select the point using cursor/ X,Y coordinates.
        4. Customizable parameters for TAP models (weight files, offline/online/version of model architecture, type of model)

    - Combining detection with TAP models
        Get the centroid of the detected bounding box (yolo/rt-detr/co-detr) -> Extract the coordinates of the centroid -> Apply TAP module on the coordinates -> compare how TAP models perform vs standard trackers (Bytetrack/BoT-SORT). Issues https://github.com/neuroinformatics-unit/ethology/issues/13 , https://github.com/neuroinformatics-unit/ethology/issues/12

    - Integration of TAP with movement repository
        1. Ensure proper serialization to/from movement repo
        2. Translating keypoints & individuals to some entity in TAP model 

    I feel 30% of the efforts will go into developing the Napari plugins while the remaining 70% in the backend support and customizations.

    **Stretch goals**:
    - Benchmarking these TAP, Detection and Tracking models on dataset of interest. Labeling techniques:
        1. Using semi-supervised approach for training a TAP model as suggested in [BootsTAP](https://openaccess.thecvf.com/content/ACCV2024/papers/Doersch_BootsTAP_Bootstrapped_Training_for_Tracking-Any-Point_ACCV_2024_paper.pdf) using a semi supervised approach to prepare ground truth from a "trained TAP" model (large model) with some human feedback
    - Solve existing issues in `ethology`, some interesting ones include (not an exhaustive list):
        1. https://github.com/neuroinformatics-unit/ethology/issues/5 : Grid on the first frame -> Apply TAP on these points -> TAP return the visibility of these points across the frames -> statistics for outlier detection
        2. https://github.com/neuroinformatics-unit/ethology/issues/15 : Bounding box centroid -> SAM/SAMURAI input prompt coordinates -> Video with segmentation masks on the detected objects (in subsequent frames we can apply segmentation with input prompt point directly from TAP model output for that frame instead of apply detection again)
    - Implement low-shot detectors like [CD-ViTO](https://arxiv.org/pdf/2402.03094) for labeling large dataset.
    
    **Community bonding period**:
    - Get to know the core-team and co-interns
    - Checkout how the team prefer to communicate and adapt
    - Convey the expectations and deliverables
    - Add detail and further breakdown on the weekly deliverables
    - Contribute to issues of interest
    - Brainstorming on the future path for the project
    - Setup devlogs for weekly updates during the coding period

    **Weekly timeline**:
    | Week | Task                                                                                     | Hours/Week |
    |------|------------------------------------------------------------------------------------------|------------|
    | 1    | Research and implement initial support for LocoTrack(S/B) TAP in `ethology`: <br> - Read paper of LocoTrack <br> - Find drawbacks of cotracker/tapir, compare what they propose vs what we want <br> - Integrate LocoTrack as a dependency                    | 30         |
    | 2    | Add support for bootsTAP tracker checkpoint and test integration with `ethology` (probably some few addons to TAPIR support)                      | 30         |
    | 3    | Video features in Napari: <br> - Support for loading video <br> - Taking input on the video (coordinates of points to track) <br> - Plot trajectories using a standard color coded meaning-full format (eg: `individual_1` colored *blue* and its keypoints differing by some $\alpha$ gradient)| 30         |
    | 4    | Napari plugins to add support for customizing the TAP pipeline parameters: <br> - Load model parameters like weight files, offline/online/version(v1, v2, v3...) of model architecture, type of model (TAPIR/Co-Tracker/LocoTrack) <br> - Video options like display results, save results, display first frame to draw keypoints <br> - Query point selection options grid, point, bbox centroid | 30         |
    | 5    | Integrate detection models like YOLOv8, Rt-Detr, Co-Detr <br> - Each detection model has different sized architectures check feasibility <br> - Integrate as a dependency from original repository | 30         |
    | 6    | Compare TAP models with state of the art tracking algorithms like ByteTrack, BotSORT, SMILETrack for tracking centroid of detection bounding box    | 30         |
    | 7    | Integrate working example of each of the proposed approach for incoming new users: <br> - Tracking-Any-Point generic example <br> - Detection + Tracker vs Detection + TAP  | 30        |
    | 8    | Add napari plugins for detection and tracking: <br> - Ability to select all combination of detector + tracker <br> - Customizable parameters like re-ID weight file, track buffer, min confidence threshold, etc                     | 30         |
    | 9    | Check the feasibility of each tracker with a benchmark metric to check the the efficiency: <br> - Object-Detection <br> - Tracking <br> - TAP models <br> on dataset of interest (in increasing order of difficulty to benchmark)                   | 30         |
    | 10    | Benchmarking Continued: Benchmarking on Occlusion Accuracy, fraction of visible points tracked within 1, 2, 4, 8 and 16 pixels (averaged over thresholds), Average Jaccard (measuring tracking and occlusion prediction accuracy together) [these metrics were used in co-tracker evaluation] | 30         |
    | 11   | Solve existing issues in `ethology` <br> - Trajectory spikes https://github.com/neuroinformatics-unit/ethology/issues/5 <br> - Segmentation masks https://github.com/neuroinformatics-unit/ethology/issues/15       | 30         |
    | 12   | Finalize code, write leftout tests, and prepare documentation and submit final deliverables                   | 30         |

    `NOTE: Haven't mentioned tests explicitly in each week's contribution, but have them in each weeks plans` 

- **Communication plan**

    1. During the initial days, we can have introductory meeting with the entire team. Getting to know each other, familiarizing with the work culture of the team.

    2. Communication can happen via PRs, Zulip and Video calls. 

    3. Time availability 
        - Chat (07:00 - 00:00 IST)
        - Video calls/Meetings (18:00 - 00:00 IST)
        - Meetings can be held twice a week/once a week for an hour discussing the progress/blockers (with mentors)
        - Once a week/bi-weekly meeting with the entire team  
    4. Weekly dev-log 

## Personal statement

_Length: max 0.75 page_

- **Past experience.** 

    **Open-Source contributions**
    1. Previously interned at [Outreachy](https://www.outreachy.org/) similar to GSoC. The organization I participated under was ModECI (https://github.com/ModECI) under Padraig Gleeson (UCL) and Ankur Sinha (UCL). My contributions include the following repositories [MDF](https://github.com/ModECI/MDF/issues?q=is%3Apr%20state%3Aclosed%20author%3Aparikshit14) & [modelspec](https://github.com/ModECI/modelspec/issues?q=is%3Apr+author%3Aparikshit14). 
    2. I have also contributed to [Keras-CV](https://github.com/keras-team/keras-cv/pull/186), [tardis](https://github.com/tardis-sn/tardis/pull/1562), [TrainYourOwnYOLO](https://github.com/AntonMu/TrainYourOwnYOLO/pull/192)

    **Programming Experience**
    1. Junior Research Fellow @ Indian Institute of Science (2023-Current)
        - Research towards solving transportation using AI
        - Representation learning for state-of-the-art self supervised models (SimSiam, MoCo, SimCLR)
    2. Outreachy intern @ ModECI (2022)
        - Added support to ONNX format for deep learning models conversion
        - Pytorch model conversion from MDF format(computation graph -> json) and vice-versa
        - Support for BSON format serialization and de-serialization
    3. SRE intern @ Motorola Solution (2021-2022)
        - Built GitHub Advanced security workflows for static code scanning with CodeQL
        - Migrated Datadog dashboards to Grafana
    4. Data-Science intern @ Quantum AI Systems (2020)
        - Deployed a binary classification based loan approval Web-App using Django
        - Implemented facial landmark detection deep-learning models


- **Motivation:**

    **Why this project?**

    Ethology facilitate the application of a wide range of computer vision tasks to animal behaviour research at a single place align with my goal of AI for Impact. Any-point trackers enable detailed monitoring of animal movements and behaviors without invasive methods, preserving naturalistic observation. Having expertise in the field of multi object detection and tracking, it was a no brainer for me to contribute to `ethology` and start exploring TAP models. Possibility to add all functionalities like detection, tracking, and TAP will create an uncanny opportunities for ethological researchers to benefit from such open-source work.

    
    **How does it link with me?**

    My passion for AI for impact led me to a research role at IISc, where I tackle Bengaluru’s severe traffic congestion using multi-object tracking and UAV-based solutions. Earlier, I focused on AI for agriculture, developing a low-complexity weed recognition model published at HiPC. I also interned at Princeton’s ModECI, standardizing computational model exchanges. All these work had one common factor `AI for Impact`. Computers would take off and re-design themselves at an ever-increasing rate. When that happens, we need to ensure the computers have goals aligned with ours. Along with this, I contributed to open-source projects like Keras-CV and TARDIS in past showing my commitment for open source development. 


- **Match: why you?**

    - In my current work, I work with object detection and tracking models for UAVs to monitor traffic. I have extensively benchmarked the SOTA tracking models on metrics including HOTA, Identity, MOTA. Published a paper titled: Benchmarking Object Detection and Tracking for UAVs (proceeding under way). Moving cameras add lot of complexity in terms of trajectory analysis, which led me to explore optical-flow and TAP to cancel out camera movement from the trajectory (work in progress)
    - Experience with edge deployment, particularly nvidia jetson orin nano and RPi. We can take this project and add edge-feasibility perspective as well
    - I have worked with a very similar org previously working on neuroscience and ML intersection: ModECI, which works towards interoperability of computational models in computational neuroscience and Machine Learning, making me a perfect fit for this organization having worked with similar researchers

- **Availability**

    - Currently, I am working as a researcher at a university. I have enough time to manage both GSoC and my full time research role.
    - I was recently selected as a visiting scholar at MIT and was invited to visit the campus in first week of June for 5-6 days. If I visit, I will make sure to compensate for my efforts on the lost time.
    - Don't have any other planned events as of now, if in case something arise, will make sure to put in extra effort.

## GSoC

_Length: max 0.25 page_

- **GSoC experience**

    I expect long-term research outcomes, long-term collaborators, improvement in my programming and communication skills, join the core team :grin: (not in any order).

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am not.



#### Additional references -
    - TAP Models : https://paperswithcode.com/task/point-tracking
    - Few-shot Detectors : https://paperswithcode.com/task/few-shot-object-detection#benchmarks
    - LocoTrack - 
        paper: https://arxiv.org/abs/2407.15420
        code: https://github.com/cvlab-kaist/locotrack
    - BootsTAP -
        paper: https://arxiv.org/html/2402.00847v1
        code: https://bootstap.github.io/
    - Co-Tracker - 
        paper: https://arxiv.org/abs/2307.07635
        code: https://github.com/facebookresearch/co-tracker
    - TAPIR - 
        paper: https://arxiv.org/abs/2306.08637
        code: https://github.com/google-deepmind/tapnet
    - YOLOv8 -
        code: https://docs.ultralytics.com/models/yolov8/
    - RT-DETR -
        paper: https://arxiv.org/abs/2304.08069
        code: https://github.com/lyuwenyu/RT-DETR
    - Co-DETR -
        paper: https://arxiv.org/pdf/2211.12860
        code: https://github.com/Sense-X/Co-DETR
    - ByteTrack -
        paper: https://arxiv.org/abs/2110.06864
        code: https://github.com/ifzhang/ByteTrack
    - BotSort -
        paper: https://arxiv.org/abs/2206.14651
        code: https://github.com/NirAharon/BoT-SORT