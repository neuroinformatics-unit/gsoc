# movement: implement outlier detection algorithms (Arismita Mukherjee)

# Personal details
- **Full name** Arismita Mukherjee
- **Email** arismita08.m@gmail.com
- **GitHub username** ArismitaM
- **Zulip username** Arismita M
- **Location & time-zone** Bangalore, India IST(UTC+5:30)
- **Personal website / project portfolio**
- **Code contribution** https://github.com/neuroinformatics-unit/movement/pull/459

- **Proposal discussion link** TBD
  
## Project proposal 
- **Synopsis**
Normally for any prediction, the "confidence score" is used as a measure of outlier detection. A low confidence signifies a possible outlier and a high confidence is assumed to be pointing to a prediction that is most probably correct. However, for pose estimation, if the backbone network (the model doing the prediction) may mistake the front hind paw of a mouse to be its left hind paw and predict its location with high confidence. Finding such "confident error" is aking to "needle-in-a-haystack" problem. Hence, we need to implement the following cost functions (as described in the lightning pose paper) for outlier detection:
    - **Temporal Continuity Loss**: Compare the pixel distance of the location of a keypont at (t)instance with that at (t-1)instance. Flag an outlier if the pixel distance exceeds a threshold.
    - **Pose Plausibility Loss**: All poses are not feasible due to natural restrictions of an animal movement. This loss function restricts the pose-prediction space to such a low-dimensional subspace and flags an outlier if the pixel distance of the prediction is above a threshold from the nearest location in this low-dimensional subspace.
    - **Multiview Consistency Loss**: Different 2D-perspectives from different cameras of a 3-D object restrict possible prediction to a low dimensional subspace. Multiple 2-D perspectives are merged into a 3-D perspective and then reprojected onto the 2D perspective of the camera to calculate the pixel distance of this re-projection against the prediction to calculate the loss and predict an outlier.
- **Implementation timeline**
  - **Minimal Set of deliverables** : 
    - Temporal Continuity Loss based outlier detection: Code and documentation
    -  Pose Plausibility Loss based outlier detection: Code and documentation
    -  Multivier Consistency Loss based outlier detection: Code and documentation

    Please include the following information:
    1. A bullet point list with **minimal set of deliverables**
    2. Additional **stretch goals** or "if time allows" deliverables (optional)
    3. A detailed **weekly timeline**: when do you plan to do what? 
        - Please use a week as a minimal unit of time, and include any planned vacations or other commitments. 
        - This timeline could be formatted as a table. 
        - Remember to also include the number of hours per week you plan to work on the GSoC project. 
        - When estimating the required time for a task, keep in mind deliverables should include investigation/research, coding and documentation. 
        - The default schedule for GSoC is 12 weeks - see the [GSoC timeline](https://developers.google.com/open-source/gsoc/timeline) for precise dates. 
        - Also please specify any prep work you plan to do during the "Community bonding period".
        - Usually week 1's deliverables already include some code. Week 6 marks the mid-term point, where usually more than half of the project should be completed. At the end of week 11 you may want to try to "freeze" the code and complete any remaining tests or documentation in weeks 11 and 12.

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
