# movement: implementing outlier detection algorithms (Arismita Mukherjee)

# Personal details
- **Full name** Arismita Mukherjee
- **Email** arismita08.m@gmail.com
- **GitHub username** ArismitaM
- **Zulip username** Arismita M
- **Location & time-zone** Bangalore, India IST(UTC+5:30)
- **Personal website / project portfolio**: https://github.com/ArismitaM
- **Code contribution** I implemented a rolling mean filter for movement using <https://github.com/neuroinformatics-unit/movement/pull/459>

- **Proposal discussion link** A draft PR https://github.com/neuroinformatics-unit/movement/pull/470 was opened for discussing my proposal. However, as per advice of mentors, this draft PR was closed and all proposal discussion about the project has happened on this <https://github.com/neuroinformatics-unit/movement/issues/145>
  
## Project proposal 
- **Synopsis**

Normally for any prediction, the "confidence score" is used as a measure of outlier detection. A low confidence signifies a possible outlier and a high confidence is assumed to be pointing to a prediction that is most probably correct. However, for pose estimation, if the backbone network (the model doing the prediction) may mistake the front hind paw of a mouse to be its left hind paw and predict its location with high confidence. Finding such "confident error" is aking to "needle-in-a-haystack" problem. Hence, we need to implement the following cost functions (as described in the lightning pose paper) for outlier detection:
    - **Temporal Continuity Loss**: Compare the pixel distance of the location of a keypont at (t)instance with that at (t-1)instance. Flag an outlier if the pixel distance exceeds a threshold.
    - **Pose Plausibility Loss**: All poses are not feasible due to natural restrictions of an animal movement. This loss function restricts the pose-prediction space to such a low-dimensional subspace and flags an outlier if the pixel distance of the prediction is above a threshold from the nearest location in this low-dimensional subspace.
    - **Multiview Consistency Loss**: Different 2D-perspectives from different cameras of a 3-D object restrict possible prediction to a low dimensional subspace. Multiple 2-D perspectives are merged into a 3-D perspective and then reprojected onto the 2D perspective of the camera to calculate the pixel distance of this re-projection against the prediction to calculate the loss and predict an outlier.
- **Implementation timeline**
  1. **Minimal Set of deliverables** : 
    - Temporal Continuity Loss based outlier detection (**WP1**): Code and documentation
    -  Pose Plausibility Loss based outlier detection (**WP2**): Code and documentation
    -  Multiview Consistency Loss based outlier detection (**WP3**): Code and documentation
  2. **Weekly Timeline**
       |       Week        |    Start    |    End      |                        Activity                        |
       | ----------------- | ----------- | ------------| -------------------------------------------------------|
       | Community Bonding | 2025/05/08  | 2025/06/01  |            xarray, pandas, numpy revision              |
       |    Week 1         | 2025/06/02  | 2025/06/08  | understand WP1 from LP paper and code base. Start Code |
       |    Week 2         | 2025/06/09  | 2025/06/15  |                 code, test cases for WP1               | 
       |    Week 3         | 2025/06/16  | 2025/06/22  |code, test cases, example usecase, documentation for WP1|
       |    Week 4         | 2025/06/23  | 2025/06/29  |        understand WP2 from LP paper and code base      |
       |    Week 5         | 2025/06/30  | 2025/07/06  |                code, test cases for WP2                |
       |    Week 6         | 2025/07/07  | 2025/07/13  |                code, test cases for WP2                |
       |    Week 7         | 2025/07/14  | 2025/07/20  |code, test cases, example usecase, documentation for WP2|
       |    Week 8         | 2025/07/21  | 2025/07/27  |        understand WP3 from LP paper and code base      |
       |    Week 9         | 2025/07/28  | 2025/08/03  |                code, test cases for WP3                |
       |    Week 10        | 2025/08/04  | 2025/08/10  |                code, test cases for WP3                |
       |    Week 11        | 2025/08/11  | 2025/08/17  |code, test cases, example usecase, documentation for WP3|
       |    Week 12        | 2025/08/18  | 2025/08/24  |    any pending work and final project submission       |
  3.  I will be devoting 30-35 hours per week towards this GSoC project. 

- **Communication plan**
  Communication with my mentors will be done in 2 levels:
  1. Any questions/clarifications/advice sought will be updated in github - so, there is an easy way of tracking and referring to all communication related to the project in 1 place. A message informing the mentors of the same will be posted on Zulip to ensure that mentors are informed about my request.
  2. Weekly standup. This will be a video call at an agreed upon time. This will help provide the mentors with update on progress and any deviation from the plan.

## Personal statement

- **Past experience** 
  1. As part of an [ML project](https://github.com/AGiLe-IIITB/HackNite_MasterRepo) that I worked on, along with 2 other members, I developed the following:
    - **Blink detection** by identifying the relative distance between eye keypoints.
    - **Face Identification**: Automatic clustering of faces from an unseen video based on DBScan of face encodings using keypoint detection. Some of these clusters were later merged manually to train the model to identify different aspects of the same face. These clusters were subsequently used to identify known faces from unseen videos.
  2. [Landcover classification](https://github.com/ArismitaM/Land_Cover_Classification) from satellite imaging
    - Involved identification of different type of landcovers by identifying the RGB code for different pixels on .tif file. These pixels were then clustered using DBScan and bounding boxes were drawn around these clusters. This data, therefore, became labelled training data for training models (e.g., Yolov5, RetinaNet and VGG5).
  3. As part of my curriculum (integrated M-Tech majoring in Electronics and Communication Engineering), I have taken courses in Python coding and used the same in the above mentioned projects. I am currently studying a course on Digital Signal Processing as part of my curriculum and I find DSP to be very interesting
    
- **Motivation: why this project?**
I am eager to learn how AI/ML can be used to improve the quality of life on this planet. My past projects have primarily been steps to understand how AI/ML works and how to use it to achieve solution to practical problems. The possibility of reducing human involvement in training machines fascinates me. Hence, my inclination towards using clustering to auto-generate high quality training data. Automatic identification of possible errors in prediction is a logical next step in this area of interest - as it helps automatically find errors with minimal human intervention. Hence, my interest in implementation of outlier detection in movement.
I believe, removing the responsibility of sifting through hundreds of prediction to identify errors, will allow humans to concentrate on things we do best. Like, identification of reason for the errors - and correcting the same. 

- **Match: why you?**
In my previous projects, I have worked on concepts which were unknown to me when I started. However, my interest in learning new ideas and concepts allowed me to get upto speed quickly and learn on the job to complete these tasks successfully, on time. This project poses a similar challenge. My past experience in handling similar challenges and my desire to learn as well as my interest in the area of work, I believe, make me the right match for this project. Over the past month, I have worked towards understanding the movement codebase, discussing, with mentors, about possible paths of implemention of outlier detection and provided suggested code changes in https://github.com/neuroinformatics-unit/movement/issues/145. So, I feel, I have gained usable experience to hit the ground running for this project.

- **Availability**
My end-semester exams get over early May - making me available for the GSoC project. I will be taking a week off in May, before the GSoC project kicks off. Post that, I will be available full-time to complete my GSoC project.

## GSoC

- **GSoC experience**
  - Gain a deep understanding of statistical modelling in AI/ML
  - Gain an understanding of how knowledge about animal movement helps in advanced research in areas like bimechanics and neuroscience.
  - Understand the nuances of working as part of a geogrpahically distributed team
  - Gain experience of contributing to a large scale open source software project
  - Improve my communication skills through regular interaction with my mentors.

- **Are you also applying to projects with other organisations in GSoC 2025?**
  No I am not applying to any other GSoC 2025 projects with any other organisations.
