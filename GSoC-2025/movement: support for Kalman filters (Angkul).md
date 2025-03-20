## movement: support for Kalman filters (Angkul)

## Persona details
- **Full name**: Angkul Puniya
- **Email**: angkul58@gmail.com
- **GitHub username**: angkul07
- **Zulip username**: angkul
- **Location & time-zone**: India, (GMT+5:30)
- **Personal website / project portfolio**: https://github.com/angkul07
- **Code Contribution**:

    I have contributed in implementing a general `rolling filter` function for mean and median filters in movement which focus on fixing the [issue #454](https://github.com/neuroinformatics-unit/movement/issues/454). Later on the suggestion of my mentor I extended this general function for min and max too and change the relevant documentation and write test cases for the rolling filter function. Here is my merged [PR #455](https://github.com/neuroinformatics-unit/movement/pull/455).

- **Proposal discussion link**

## Project Proposal

- **Synopsis**

    This project focuses on implementing the Kalman Filter in movement for data cleaning and filtering, specifically to smooth position, velocity, and acceleration data in animal tracking data. This helps in reducing noise in data and improve the data consistency and quality. Additionally, the project tackles the identity-switch problem in multi-animal tracking, ensuring more reliable tracking and analysis. 
    This project is important because this aims to reduce the noisiness in animal tracking data and thus improving the data quailty for analysing motion tracking. 
    
    Deliverables include the Kalman Filter implementation, extending Kalman Filter to fix identity switch, testing-documentation of the new functionality and an example in movement gallery.  With the help of this Kalman Filter implementation, the open-source community will gain cleaner, more consistent, and high-quality data for motion tracking analysis benefiting the researchers, scientists.

- **Implementation timeline**
    
    **Deliverables**
    - Kalman Filter for Smoothing of position, velocity, acceleration
    - Tests for the Kalman Filter Smoothing
    - Documentation for Kalman Filter function and smoothing
    - Example use case of Kalman Filter in movement gallery

    **Stretch Goals**
    - Kalman Filter for Identity Switch correction in Multi-Animal Tracking
    - Extended tests and documentation for Identity correction

    **Weekly Timeline**

    | Time Frame | Tasks & Deliverables |
    |------------|---------------------|
    | **Pre GSOC period**  <br> March 24 - May 8 | - Take a deeper dive into the work done so far, learn about the Kalman filter, explore the other existing implementations of the Kalman Filter.  <br> - Explore the movement codebase, docs and testing things, fix bugs, implement examples to understand the internal working of movement functions. |
    | **Community Bonding Period (Before week 1)**  <br> May 8 - June 1 | - Much time won’t be wasted as I’m aware of most parts of the codebase and know the mentors well and the development environment is already set.  <br> - Discuss and decide the best possible method to implement the Kalman Filter with the mentor. |
    | **Week 1**  <br> June 2 - June 9 | - Implement the basic Kalman Filter for position smoothing.  <br> - Test the position smoothing feature on the movement dataset. |
    | **Week 2**  <br> June 10 - June 17 | - Extend the Kalman Filter to handle velocity and acceleration smoothing.  <br> - Derive the velocity and acceleration data from the position data using the kinematics module for testing purposes.  <br> - Test the velocity and acceleration smoothing on the derived dataset. |
    | **Week 3**  <br> June 18 - June 25 | - Discuss the current progress with the mentor and ask for review and suggestions.  <br> - Work on the suggestions and unit testing for the smoothing functionality. |
    | **Week 4**  <br> June 26 - July 2 | - Write the docstring for the Kalman filter functions. Write documentation and guide for the Kalman filter and smoothing feature.  <br> - Create an initial example for the movement gallery. |
    | **Week 5**  <br> July 3 - July 10 | - Asked for mentor feedback and refined the smoothing feature based on feedback.  <br> - Finalize the integrations, documentation, and prepare for mid-term examination. |
    | **Week 6**  <br> July 11 - July 18 | - **Mid-term Submission:** Smoothing feature should be fully implemented, tested, and documented. |
    | **Week 7**  <br> July 19 - July 26 | - Research, discuss, and design Kalman filter approach for identity switch correction. This feature will be more difficult to implement.  <br> - Collect the data related to identity switch, discuss with mentors, and set up the development environment. |
    | **Week 8**  <br> July 27 - August 3 | - Implement data association using Hungarian Algorithm or Mahalanobis distance.  <br> - Start implementing the Kalman filter prediction, cost matrix for multi-animal tracking.  <br> - Test basic identity switches detection. |
    | **Week 9**  <br> August 4 - August 11 | - Improve identity correction using re-identification techniques such as confidence scores.  <br> - Implement the tests for identity switch correction. |
    | **Week 10**  <br> August 12 - August 19 | - Optimize Kalman filter performance for multi-animal tracking. Optimization is required to make sure that switch corrections are identified correctly.  <br> - Integration of identity correction in the movement codebase. |
    | **Week 11**  <br> August 20 - August 27 | - Start writing the documentation for Identity switch correction feature.  <br> - Freeze the codebase. |
    | **Week 12**  <br> August 28 - September 4 | - Finish remaining tests and documentations.  <br> - Code polishing, final testing & performance checks.  <br> - Final GSOC report. |

    I estimated that minimum number of hours required to complete this project is between 170-180 hours. I plan to dedicate the 15-20 hours per week and approx. 4-5 hours daily.

    **Communication plan**
    
    To communicate with the mentors, I will follow the default communication channels follow by movement which are zulip chats and zoom meetings.I will communicate with my mentors daily on Zulip chat for guidance and continuous feedback. To review the progress from the previous week and discuss plans for the upcoming week, I will do a weekly stand-up Zoom meeting with my mentors.

## Personal statement

- **Past experience**
    
    I have been programming for 2 years and I am proficient in python, pandas, numpy, pytorch and various other libraries. So, my experience with data libraries aligns with this project. I think the experience which I gained working with the movement in the past few weeks, it will help me in my future contribution in the movement.

- **Motivation**
    
    I have been always interested in mapping the bridge between the data preprocessing, machine learning and read-world use cases. I think this project provides the best opportunity to do that. And given my background with numpy, pandas and ML, this projects align with my skills. Moreover, working on this project gives me an opportunity to contribute to a open-source library, making movement more robust and useful for researchers, scientists, and future developers. The idea of helping improve animal tracking and animal research, basically I am contributing directly to the nature in an open-source setting motivates me because it has real-world impact beyond just writing code.

- **Match: why me**
    
    I have been contributing to movement for some time now, fix issues, opened draft PR for kalman filter and I completely understand the movement's codebase, team structure, how the team work. I have been in regular touch with the mentors and active in the Zulip chat. All this shows, my the dedication towards the movement and this project. Given my familiarity with both the codebase and the team, I am confident that I can efficiently implement 
    the Kalman filter features in the movement library.

- **Availabilty**
    
    I will be fully available during the working period because at that time, I will have my summer breaks of 3 months from may to july. So, I will be fully available.
    I will be most active between Monday and Friday from 3 pm to 3 am IST.

## GSOC

- **GSoC experience**

    For me, GSoC is more than just a program—it's a chance to learn, grow, and be part of something bigger. As a first-time participant, I am very excited to work closely with mentors, gain new skills, and grow as a developer. 
    Beyond just coding, I see GSoC as a chance to develop problem-solving skills, collaborate in a structured development environment, and make meaningful contributions to open source.
    Most of all, I can’t wait to make meaningful contributions in the research with the help of movement, learn from others, and give back to the community that has taught me so much. This is going to be an incredible journey!

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am 100% dedicated to movement and have no plans whatsoever to submit a proposal to any other organization.