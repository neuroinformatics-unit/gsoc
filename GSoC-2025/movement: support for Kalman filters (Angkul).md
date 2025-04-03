## movement: support for Kalman filters (Angkul)

## Personal details

* **Full name**: Angkul Puniya  
* **Email**: [angkul58@gmail.com](mailto:angkul58@gmail.com)  
* **GitHub username**: [angkul07](https://github.com/angkul07)  
* **Zulip username**: [angkul](https://neuroinformatics.zulipchat.com/#user/881687)  
* **Location & time-zone**: Haryana, India. Time-Zone: Asia/Kolkata (GMT+5:30)  
* **Personal website / project portfolio**: [https://github.com/angkul07](https://github.com/angkul07) & [https://www.kaggle.com/angkul/](https://www.kaggle.com/angkul/)  
* **Code Contribution**:

  i. [Added a generall filter function for mean, median, min and max filters](https://github.com/neuroinformatics-unit/movement/pull/455)
  <br>ii. [Extended the interpolate\_over\_time to bfill, ffill, nearest and constant functionality](https://github.com/neuroinformatics-unit/movement/pull/500)

* **Proposal discussion link:** [https://github.com/neuroinformatics-unit/gsoc/pull/4](https://github.com/neuroinformatics-unit/gsoc/pull/4)

## Project Proposal

* **Synopsis**  
  This project aims to apply the Kalman Filter to movement for smoothing and filtering data, i.e, to smooth and filter velocity, acceleration, and position data in animal motion tracking. This helps in reducing noise in data and improving the data consistency and quality. Additionally, the project tackles the identity-switch problem in multi-animal tracking, ensuring more reliable tracking and analysis. This project is important because this aims to reduce the noise in animal tracking data and thus improving the data quality for analysing motion tracking.  
    
  Deliverables include the Kalman Filter implementation, extending Kalman Filter to fix identity switch, testing-documentation of the new functionality and an example in movement gallery.  With the help of this Kalman Filter implementation, the open-source community will have cleaner, consistent, and high-quality data for motion tracking analysis to the advantage of the researchers and scientists.  
    
* **Implementation timeline**  
  **Deliverables**  
  * Kalman Filter implementation for Smoothing of position, velocity, acceleration.  
  * Add tests to cover the Kalman Filter Smoothing.  
  * Documentation and use case example for Kalman Filter function and smoothing.  
    

  **Stretch Goals**  
  * Kalman Filter for Identity Switch correction in Multi-Animal Tracking. Add its tests and documentation.  
      
* **Weekly Timeline**


| Time Frame | Tasks & Deliverables | Hours |
| :---- | :---- | :---- |
| **Pre GSOC period**   March 24 \- May 8 | \- Explore the movement codebase, docs and testing things, fix bugs, implement examples to understand the internal working of movement functions. <br>\- Understand the Kalman filter, experiment with the existing Kalman Filter implementations([PyKalman](https://github.com/pykalman/pykalman), [nfoursid](https://nfoursid.readthedocs.io/en/latest/source/kalman.html), [dynamax](https://probml.github.io/dynamax/), [movingpandas](https://movingpandas.readthedocs.io/en/main/api/trajectorysmoother.html)). This helps in assessing each library's flexibility, ease of integration with the movement library. I already experimented with [darts](https://unit8co.github.io/darts/generated_api/darts.models.filtering.kalman_filter.html)(it doesn’t provide any flexibility) and [filterpy](https://filterpy.readthedocs.io/en/latest/kalman/KalmanFilter.html)(it is outdated) so these are not suitable. | 15 |
| **Community Bonding Period (Before week 1\)**   May 8 \- June 1 | \- Discuss the best possible method to implement the Kalman Filter with the mentors based on the experiment's results. <br>\- Research the methods to fix the identity switch problem in Multi-Animal Tracking so that we can save time in later weeks and directly work on fixing this problem. Regular discussion with mentors. | 15 |
| **Week 1** **& Week 2** (June 2 \- June 15\) | \- Implement the basic Kalman Filter for position smoothing and generate the synthetic data for position.   <br>\- Test the position smoothing feature on the movement dataset and noisy synthetic data. Check if it smooths the position or not. Ask mentors for feedback and suggestions. Fix bugs and work on suggestions. <br>\- Extend the Kalman Filter to handle velocity and acceleration smoothing. Test and evaluate the extended functionality on the dataset by checking if it can recover the true motion. | 15 |
| **Week 3**   <br> June 16 \- June 22 | \- Optimize the Kalman filter parameters if the chosen Kalman filter implementation doesn’t support the automatic optimization of these parameters. Libraries like PyKalman, Dynamax support the EM(Expectation-Maximization) algorithm which automatically optimizes the parameters to generalise over the movement dataset. <br>\- Discuss the progress with mentors, review and suggestions. Fix bugs and work on the suggestions. | 15 |
| **Week 4** **& Week 5** (June 23 \- July 6\) | \- Add the unit tests for the Kalman filter. Write documentation and guide for the Kalman filter and smoothing feature. Create an example of the Kalman filter for the movement gallery. <br>\- Ask mentors for feedback and refine the smoothing feature based on feedback. Finalize the integrations, documentation, and prepare for mid-term examination. | 15 |
| **Week 6**   <br> July 7 \- July 13 | \- **Mid-term Submission:** Run the final checks, to ensure that Kalman filter implementations are working as expected. Submit the mid-term evaluation. | 15 |
| **Week 7**   <br> July 14 \- July 20 | \- Explore methods to fix the identity switches problem. I will continue the progress of the community bonding period. Based on my current research, methods such as using [Hungarian Algorithm](https://en.wikipedia.org/wiki/Hungarian_algorithm), [Mahalanobis distance](https://en.wikipedia.org/wiki/Mahalanobis_distance) and [Joint Probabilistic Data Association (JPDA)](https://en.wikipedia.org/wiki/Joint_Probabilistic_Data_Association_Filter) can solve this problem. Combining the Hungarian Algorithm and Mahalanobis distance is better over JPDA because it is simple and effective. <br>\- Collect the relevant data to identify switches, discuss the approach with mentors, and set up the development environment. | 15 |
| **Week 8**   <br> July 21 \- July 27 | \- The proposed steps are: predict the future positions of tracked animals using the Kalman filter, and create a distance matrix using the Mahalanobis distance between future positions and original positions. Apply the Hungarian Algorithm on the distance matrix to find the optimal assignments of identities and update the identities.  <br>\- Implement the Mahalanobis distance and Hungarian Algorithms for identity switch correction. <br> \- Discuss the progress with mentors, review and suggestions. Fix bugs and work on the suggestions. | 15 |
| **Week 9**   <br> July 28 \- August 3 | \- Test the implemented solution on the datasets and edge cases like where two animals crossed paths. <br>\- Improve identity correction using re-identification techniques such as confidence scores. If the confidence score is less than the threshold for a corrected identity then that identity predicted is wrong and so initializes the other identity. | 15 |
| **Week 10** **& Week 11** (August 4 \- August 17\) | \- Implement the unit tests for identity switch correction and integrate the identity correction in the movement codebase. Ask mentors for feedback and suggestions. <br>\- Create a use case example and write documentation of identity switch corrections implementation. | 15 |
| **Week 12**   <br> August 18 \- August 24 | \- Code polishing, final testing, performance checks and finalizing the documentation. <br>\- Freeze the codebase and submit the project and final GSOC report. | 15 |

* **Communication plan**  
  I will communicate with my mentors daily on Zulip chat for guidance and continuous feedback. To review the progress from the previous week and discuss plans for the upcoming week, I would appreciate weekly video calls with my mentors.

## Personal statement

* **Past experience**  
  I have two years of experience in python and I am proficient in core machine learning libraries like numpy, pandas, xarray, sklearn and pytorch. I worked on many machine learning projects where I handle the datasets, pre-process the dataset and build the machine learning models. I have also taken part in numerous [Kaggle competitions](https://www.kaggle.com/angkul/code), additionally enhancing my skills. Beside core data processing and machine learning libraries, I am also proficient in libraries like langchain, crewai and smolagents.  
    
* **Motivation**

	There are two main reasons why I wanted to work on this project. First of all this is a rare and exciting project(there are  
  only a few projects which research on the animals) and second this project aligns with my skill set. I always wanted to   
  work on a project where I can apply my skill set in a real world scenario. So, this project gives me that opportunity. To be honest, I have never been good with the data cleaning and processing but this time the work I have done so far for this project(all issues I solved, PRs), the time I spent, gives me a chance to improve my skills and I understood these libraries under the hood. This is one of the most important reason which motivates me to work on this project. 

  This project is more than about data, this project gives me an opportunity to contribute to open-source research and I will be helping so many future researchers, scientists. This is very exciting for me and I am very excited to work on this project.  
  

* **Match: why me**  
  I have been contributing to the movement for many weeks now. In these past weeks, I opened the 3 PRs([\#455](https://github.com/neuroinformatics-unit/movement/pull/455), [\#500](https://github.com/neuroinformatics-unit/movement/pull/500), [\#457](https://github.com/neuroinformatics-unit/movement/pull/457)). To make all the PRs, I need to understand how movement works internally, learn all related libraries, Kalman Filter. This shows that I am a quick learner and disciplined. I am also active in the movement’s zulip chat and instead of asking unnecessary questions to mentors, I asked relevant questions, show my direct work. This shows my decision taking skills and shows that I can take responsibility for a project and I am a discipline oriented person.   
    
  As I mentioned in my past experience, I am proficient in libraries like numpy, pandas, xarray and in data handling. And thanks to my contributions in movement, I am very familiar with the movement codebase. So, I think all these factors made me well-prepared for this project.  
    
* **Availability**  
  I will be fully available during the working period as I will have a 3 month summer break from May to July. I will be most active between Monday and Friday from 3 pm to 3 am IST.

## GSOC

* **GSoC experience**  
  For me, GSoC is more than just a program—it's a chance to learn, grow, and be part of something bigger. As a first-time participant, I am very excited to work closely with mentors, gain new skills, and grow as a developer. Beyond just coding, I see GSoC as a chance to develop problem-solving skills, collaborate in a structured development environment, and make meaningful contributions to open source. Most of all, I can’t wait to make meaningful contributions in the research with the help of movement, learn from others, and give back to the community that has taught me so much. This is going to be an incredible journey\!  
    
* **Are you also applying to projects with other organisations in GSoC 2025?**  
  I am 100% dedicated to movement and have no plans whatsoever to submit a proposal to any other organization.