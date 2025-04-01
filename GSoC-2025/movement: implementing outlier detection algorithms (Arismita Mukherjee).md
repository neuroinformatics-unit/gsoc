# movement: implementing outlier detection algorithms (Arismita Mukherjee)

# Personal details
- **Full name**: Arismita Mukherjee
- **Email**: arismita08.m@gmail.com
- **GitHub username**: ArismitaM
- **Zulip username**: Arismita M
- **Location & time-zone**: Bangalore, India IST(UTC+5:30)
- **Personal website / project portfolio**: https://github.com/ArismitaM
- **Code contribution**: I implemented a rolling mean filter for movement using <https://github.com/neuroinformatics-unit/movement/pull/459>

- **Proposal discussion link**: [PR#21](https://github.com/neuroinformatics-unit/gsoc/pull/21)
  
## Project proposal 
- **Synopsis**

   Normally for any prediction, the "confidence score" is used as a measure of outlier detection. A low confidence signifies a possible outlier and a high confidence is assumed to be pointing to a prediction that is most probably correct. However, for pose estimation, if the backbone network (the model doing the prediction) may mistake the front hind paw of a mouse to be its left hind paw and predict its location with high confidence. Finding such "confident error" is aking to "needle-in-a-haystack" problem. Hence, we need to implement the following cost functions (as described in the lightning pose paper) for outlier detection:
    - **Temporal Continuity Loss**: Compare the pixel distance of the location of a keypont at (t)instance with that at (t-1)instance. Flag an outlier if the pixel distance exceeds a threshold. There are 2 interesting scenarios that will be interesting to think about. An example, will perhaps, be able to explain these better (Let us use x co-ord of 1 keypoint for illustration, and assume 10 as the threshold to trigger an outlier-detection):
        1. x=12 (t=0), x=32 (t=1), x=15 (t=2), x=10 (t=3)
        2. Let us assume we pad row 0 with the values of the actual row 0, so, we get as many diffs as there are rows.
        3. As per the temporal loss calculation, diff-ing sequential rows, will flag t=1 (t=0, in input) and t=2 (t=1 in input) as outliers. However, t=1 (t=0, in input) is definitely not an outlier.
        4. If we were to do diff first between t and t+1 and then between t-1 and t, we will have outlier marked in both cases only for t=1, thereby identifying the exact outlier.
        5. If we were to consider a case where we see a set of clustered outliers e.g., x=12(t=0), x=32(t=1), x=35(t=2), x=30(t=3), x=15(t=4), x=11(t=5), x=13(t=6), clearly t=1 (t=2 after padding), t=2 (t=3 after padding), t=3 (t=4 after padding) are outliers. But using the 2 diffs (t to t+1 and t-1 to t), we will not breach the threshold for any of the points for both diffs simultaneously. This is, perhaps, a clear indication that we do not have a single outlier but a series of outliers and the position of the threshold breaches act as start and end markers for the set of outliers.
    - **Pose Plausibility Loss**: All poses are not feasible due to natural restrictions of an animal movement. This loss function restricts the pose-prediction space to such a low-dimensional subspace and flags an outlier if the pixel distance of the prediction is above a threshold from the nearest location in this low-dimensional subspace. In order to restrict the plausible pose space, the LP paper suggests the use of pose PCA to identify the dominant Principal Pose components. The predictions, are then, projected onto this restricted Pose Space and reprojected back onto the keypoints to identify the loss based on the pixel difference between the actual prediction and the pose reprojection.
    - **Multiview Consistency Loss**: Different 2D-perspectives from different cameras of a 3-D object restrict possible prediction to a low dimensional subspace. Multiple 2-D perspectives are merged into a 3-D perspective and then reprojected onto the 2D perspective of the camera to calculate the pixel distance of this re-projection against the prediction to calculate the loss and predict an outlier. Normally, to merge multiple 2-D camera perspectives onto 3-D, all these cameras are calibrated to identify their intrinsic parameters (e.g., their focal length and distortion). These intrinsic paramteres along with extrinsic parameters (the exact relative location of the cameras in the 3-D space), determine the 2D-projection that each camera sees of a 3-D object. However, camera calibration is laborious, time-consuming and at times not feasible in tightly constained spaces. Moreover, the calibration has to be done for every change to either location of the camera or the camera itself. The Lightning Pose Paper [LP](https://www.nature.com/articles/s41592-024-02319-1) approximates the position of the keypoints in 3-D space by using Principal Component Analysis (of 3 principal components). The 3-D space is approxomated by calculating the EigenVector for each of these 3 principal components and the Loading Score of each of the camera towards these EigenVectors determine the transformation of the 2-D perspective of each of these cameras onto this 3-D space. Thus, each of the camera perspectives are projected onto this approximated 3-D space. Every point in this 3-D space is, then, re-projected back onto the 2-D space of specific cameras by reversing the steps described above. The pixel distance between the actual prediction of a keypoint and the reprojection back from the 3-PCA 3-D space back to the 2-D space of the camera defines this cost function. Thus, this novel 3-PCA approach removes the need for the repetitive camer callibration.

    Outlier detection based on these loss calculation will be implemented as a user-friendly Python API. Test cases will be implemented to exercise these APIs and ensure they work as per expectation. Documentation to explain the use of these APIs will be put in place. Examples will be added in the codebase, to enable users to start using these APIs with ease. 

- **Implementation timeline**
  1. **Minimal Set of deliverables** : 
    - Temporal Continuity Loss based outlier detection (**WP1**): Code, test cases, example usecases and documentation
    -  Pose Plausibility Loss based outlier detection (**WP2**): Code, test cases, example usecases and documentation
    -  Multiview Consistency Loss based outlier detection (**WP3**): Code, test cases, example usecases and documentation
  2. **Stretch Goals**:
    - Support calibrated camera data for an alternate Multiview Consistency Loss calculation. Compare the performance of this calibrated Multiview Consistency Loss to that of uncalibrated (3-PCA based) Multiview Consistency Loss for outlier detection.
    - Implement UI for visualizing the outlier keypoints in each video frame based on the different loss calculations.
  3. **Weekly Timeline**:
       |       Week        |    Start    |    End      |                        Activity                        |
       | ----------------- | ----------- | ------------| -------------------------------------------------------|
       | Community Bonding | 2025/05/08  | 2025/06/01  |<ul><li>xarray, pandas, numpy revision</li> <li>understand the developer workflow for contribution to movement</li> <li>interact and get to know the movement developer community and my mentors</li></ul>|
       |    Week 1         | 2025/06/02  | 2025/06/08  |<ul><li>add to the initial understanding of WP1 from LP paper, LP code base and movement code base</li><li>start coding for single frame outlier detection</li></ul>|
       |    Week 2         | 2025/06/09  | 2025/06/15  |<ul><li>complete code for single frame outlier detection</li><li>add test cases for single frame outlier detection</li><li>start coding for multi frame outlier detection</li></ul>| 
       |    Week 3         | 2025/06/16  | 2025/06/22  |<ul><li>complete code for multi frame outlier detection</li><li>add test cases for multi frame outlier detection</li><li>add example usecases for WP1</li><li> documentation for WP1</li>|
       |    Week 4         | 2025/06/23  | 2025/06/29  |<ul><li>understand WP2 from LP paper and code base</li><li>start coding to generate the restricted pose space using pose PCA</li></ul>|
       |    Week 5         | 2025/06/30  | 2025/07/06  |<ul><li>complete code for pose PCA</li><li>start coding to determine the loss for WP2</li></ul>|
       |    Week 6         | 2025/07/07  | 2025/07/13  |<ul><li>complete code to determine the loss for WP2</li><li>start adding test cases for WP2</li></ul>|
       |    Week 7         | 2025/07/14  | 2025/07/20  |<ul><li>complete adding test cases for WP2</li><li> add example usecases for WP2</li><li>documentation for WP2</li></ul>|
       |    Week 8         | 2025/07/21  | 2025/07/27  |<ul><li>understand WP3 from LP paper and code base</li><li>start coding for projecting multi camera views onto 3-PCA model</li></ul>|
       |    Week 9         | 2025/07/28  | 2025/08/03  |<ul><li>complete code for projecting multi camera views onto 3-PCA model</li><li>start coding to determine loss for WP3</li></ul>|
       |    Week 10        | 2025/08/04  | 2025/08/10  |<ul><li>complete code to determine loss for WP3</li><li> start adding test cases for WP3</li></ul>|
       |    Week 11        | 2025/08/11  | 2025/08/17  |<ul><li> complete adding test cases for WP3</li><li>add example usecases for WP3</li><li>documentation for WP3</li></ul>|
       |    Week 12        | 2025/08/18  | 2025/08/24  |<ul><li>final code/testcases/usecases/documentation cleanup</li><li>GSoC final submission</li></ul>|
  3.  I will be devoting 30-35 hours per week towards this GSoC project. 

- **Communication plan**
  Communication with my mentors will be done in 2 levels:
  1. Any questions/clarifications/advice sought will be updated in github - so, there is an easy way of tracking and referring to all communication related to the project in 1 place. Daily updates and feedback will be done through Zulip.
  2. Weekly standup. This will be a video call at an agreed upon time. This will help provide the mentors with update on progress and any deviation from the plan.
  3. Maintaining a **devlog** could be a very effective way to chronicle the goings on, issues faced, resolutions discussed with mentors and solution arrived at. This can ultimately be published as the project blog. I have not created a devlog before. However, am interested in following this approach for this project. Decision on the appropriate devlog tool will be arrived at after advise from the mentors.

## Personal statement

- **Past experience** 
  1. As part of an [ML project](https://github.com/AGiLe-IIITB/HackNite_MasterRepo) that I worked on, along with 2 other members, I developed the following:
    - **Blink detection** by identifying the relative distance between eye keypoints.
    - **Face Identification**: Automatic clustering of faces from an unseen video based on DBScan of face encodings using keypoint detection. The primary reason for using DBScan, as the clustering algorithm, instead of the K-Means clustering method, was the fact that you do not need to pre-state the number of clusters to DBScan. When building a cluster of same faces (of the same person), there was no way to prejudge how many individual persons were going to be there in the unknown video that was to act as the input. However, K-Means mandates the number of cluster to be put in as an input. Some of these clusters were, later, merged manually to train the model to identify different aspects of the same face. This manual merging was done by looking at the sample faces of different clusters. When 2 clusters were found which were different aspects of the same face, they were marked as clusters to be merged - wherein, the cluster-id (which could be user input name) of the merged cluster was updated to the cluster-id to which this was merged. Ultimately, all the 128-d keypoints of each face was stored in a dictionary containing the final face-id(or name) of the person. These clusters (stored as a pickle file) were subsequently used to identify known faces from unseen videos, by encoding the faces in the unknown video and calculating the euclidean distance to the encoded faces in the dictionary and using the id of the closest face encoding as the id of the identified face. Further details about this project is available at my [face_detection](https://github.com/ArismitaM/face_detection?tab=readme-ov-file)
  2. [Landcover classification](https://github.com/ArismitaM/Land_Cover_Classification) from satellite imaging
    - Involved identification of different type of landcovers by identifying the RGB code for different pixels on .tif file. These pixels were then clustered using DBScan and bounding boxes were drawn around these clusters. This data, therefore, became labeled training data for training models (e.g., Yolov5, RetinaNet and VGG5). The models trained with this labelled data was used to classify the landcover from unseen satellite images. Such auto-classification of landcover serves as a very useful mechanism of detecting deforestation. Or to identify where aforestation activities are succeeding, so, the same can be replicated. Identification of human encroachments in ecologically sensitive areas or in landslide prone areas, can provide actionable information to the local government to take corrective actions. Such actions can prevent loss of human lives when natural calamities, like landslides, strike.
  3. As part of my curriculum (integrated M-Tech majoring in Electronics and Communication Engineering at International Institute of Information Technology, Bangalore), I have taken courses in Python coding and used the same in the above mentioned projects. I am currently studying a course on Digital Signal Processing as part of my curriculum and I find DSP to be very interesting. The simple fact that converting a signal from analog to digital domain, by quantizing it, makes it much more robust against noise, is fascinating. At present, we are learning and trying to use adaptive filters. The fact that the same filter can adapt to prevalent noise, and thereby, become more effective against different types of noise automatically, fascinates me. The use of such filters (e.g., Kalman Filter) in ML to correct prediction and track an object in real time makes the learning even more interesting. Another such filter that we have learnt is the Gradient Descent, where, it follows the gradient to reach a goal. While learning about the training process of Deep Neural Networks, I have seen practical use of this filter in ML. This use of concepts from DSP in ML is what makes me appreciate the subject of DSP, even more.
    
- **Motivation: why this project?**
I am eager to learn how AI/ML can be used to improve the quality of life on this planet. My past projects have primarily been steps to understand how AI/ML works and how to use it to achieve solution to practical problems. The possibility of reducing human involvement in training machines fascinates me. Hence, my inclination towards using clustering to auto-generate high quality training data. Automatic identification of possible errors in prediction is a logical next step in this area of interest - as it helps automatically find errors with minimal human intervention. Hence, my interest in implementation of outlier detection in movement.
I believe, removing the responsibility of sifting through hundreds of prediction to identify errors, will allow humans to concentrate on things we do best. Like, identification of reason for the errors - and correcting the same. 

- **Match: why you?**
In my previous projects, I have worked on concepts which were unknown to me when I started. However, my interest in learning new ideas and concepts allowed me to get upto speed quickly and learn on the job to complete these tasks successfully, on time. This project poses a similar challenge. My past experience in handling similar challenges and my desire to learn as well as my interest in the area of work, I believe, make me the right match for this project. Over the past month, I have worked towards understanding the movement codebase, discussing, with mentors, about possible paths of implemention of outlier detection and provided suggested code changes in https://github.com/neuroinformatics-unit/movement/issues/145. So, I feel, I have gained usable experience to hit the ground running for this project.

- **Availability**:
My end-semester exams get over early May - making me available for the GSoC project. I will be taking a week off in May, before the GSoC project kicks off. Post that, I will be available full-time to complete my GSoC project.

## GSoC

- **GSoC experience**
  - Gain a deep understanding of statistical modelling in AI/ML
  - Gain an understanding of how knowledge about animal movement helps in advanced research in areas like biomechanics and neuroscience.
  - Understand the nuances of working as part of a geographically distributed team
  - Gain experience of contributing to a large scale open source software project
  - Improve my communication skills through regular interaction with my mentors.

- **Are you also applying to projects with other organisations in GSoC 2025?**

  No I am not applying to any other GSoC 2025 projects with any other organisations.
