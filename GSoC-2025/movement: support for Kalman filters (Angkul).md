## movement: support for Kalman filters (Angkul)

## Persona details

* **Full name**: Angkul Puniya  
* **Email**: [angkul58@gmail.com](mailto:angkul58@gmail.com)  
* **GitHub username**: angkul07  
* **Zulip username**: [angkul](https://neuroinformatics.zulipchat.com/#user/881687)  
* **Location & time-zone**: India, (GMT+5:30)  
* **Personal website / project portfolio**: [https://github.com/angkul07](https://github.com/angkul07) & [https://www.kaggle.com/angkul/](https://www.kaggle.com/angkul/)  
* **Code Contribution**:


| Issue | Pull request | Description |
| :---- | :---- | :---- |
| [\#454](https://github.com/neuroinformatics-unit/movement/issues/454) | [\#455](https://github.com/neuroinformatics-unit/movement/pull/455) | Added a generall filter function for mean, median, min and max filters. |
| [\#326](https://github.com/neuroinformatics-unit/movement/issues/326) | [\#500](https://github.com/neuroinformatics-unit/movement/pull/500) | Extended the interpolate\_over\_time to bfill, ffill, nearest and constant functionality. |
| [\#10](https://github.com/neuroinformatics-unit/movement/issues/10) | [\#457](https://github.com/neuroinformatics-unit/movement/pull/457)(draft) | Working on the implementation of Kalman Filter for movement. |

* **Proposal discussion link:** [https://github.com/neuroinformatics-unit/gsoc/pull/4](https://github.com/neuroinformatics-unit/gsoc/pull/4)

## Project Proposal

* **Synopsis**  
    
  This project aims to apply the Kalman Filter to movement to smooth and filter data, that is, to smooth and filter velocity, acceleration, and position data in animal tracking data. This helps in reducing noise in data and improving the data consistency and quality. Additionally, the project tackles the identity-switch problem in multi-animal tracking, ensuring more reliable tracking and analysis. This project is important because this aims to reduce the noise in animal tracking data and thus improving the data quality for analysing motion tracking.  
    
  Deliverables include the Kalman Filter implementation, extending Kalman Filter to fix identity switch, testing-documentation of the new functionality and an example in movement gallery.  With the help of this Kalman Filter implementation, the open-source community will have cleaner, consistent, and high-quality data for motion tracking analysis to the advantage of the researchers and scientists.  
    
* **Implementation timeline**  
    
  **Deliverables**  
    
  * Kalman Filter for Smoothing of position, velocity, acceleration  
  * Tests for the Kalman Filter Smoothing  
  * Documentation for Kalman Filter function and smoothing  
  * Example use case of Kalman Filter in movement gallery


  **Stretch Goals**


  * Kalman Filter for Identity Switch correction in Multi-Animal Tracking  
  * Extended tests and documentation for Identity correction  
* **Weekly Timeline**


| Time Frame | Tasks & Deliverables | Hours |
| :---- | :---- | :---- |
| **Pre GSOC period**   March 24 \- May 8 | \- Take a deeper dive into the work done so far, learn the Kalman filter, explore the other existing implementations of the Kalman Filter([PyKalman](https://github.com/pykalman/pykalman), [nfoursid](https://nfoursid.readthedocs.io/en/latest/source/kalman.html)) <br> \- Explore the movement codebase, docs and testing things, fix bugs, implement examples to understand the internal working of movement functions. | 15 |
| **Community Bonding Period (Before week 1\)**   May 8 \- June 1 | \- Research to fix the identity switch problem in Multi-Animal Tracking so that we can save time in later weeks and directly work on fixing this problem. Regular discussion with mentors. <br>\- Discuss and decide the best possible method to implement the Kalman Filter with the mentor. | 15 |
| **Week 1** <br>  June 2 \- June 8 | \- Implement the basic Kalman Filter for position smoothing.   <br>\- Test the position smoothing feature on the movement dataset and synthetic data, ensuring it is working as expected. Ask mentors for feedback and suggestions. | 15 |
| **Week 2** <br>  June 9 \- June 15 | \- Extend the Kalman Filter to handle velocity and acceleration smoothing.   <br>\- Derive the velocity and acceleration data from the position data using the kinematics module for testing purposes. Test the implementation by using synthetic data. <br>\- Test the velocity and acceleration smoothing on the derived dataset. Ask mentors for feedback and suggestions. | 15 |
| **Week 3** <br>  June 16 \- June 22 | \- Discuss the current progress with the mentor and ask for review and suggestions.   <br>\- Optimize the Kalman filter  Work on the suggestions and unit testing for the smoothing functionality. | 15 |
| **Week 4** <br>  June 23 \- June 29 | \- Write the docstring for the Kalman filter functions. Write documentation and guide for the Kalman filter and smoothing feature.   <br>\- Create an initial example for the movement gallery. | 15 |
| **Week 5** <br>  June 30 \- July 6 | \- Ask mentors for feedback and refined the smoothing feature based on feedback.   <br>\- Finalize the integrations, documentation, and prepare for mid-term examination. | 15 |
| **Week 6** <br>  July 7 \- July 13 | \- **Mid-term Submission:** Smoothing features should be fully implemented, tested, and documented. <br>\- Submit the mid-term evaluation.  | 15 |
| **Week 7** <br>  July 14 \- July 20 | \- Research, discuss, and design Kalman filter approach for identity switch correction. This feature will be more difficult to implement.  <br> \- Collect the data related to identity switch, discuss with mentors, and set up the development environment. | 15 |
| **Week 8** <br>  July 21 \- July 27 | \- Implement data association using Hungarian Algorithm or Mahalanobis distance. However, other methods might be possible after research. I explained it in [this comment](https://github.com/neuroinformatics-unit/gsoc/pull/4#discussion_r2017404525). <br>\- Start implementing the Kalman filter prediction, cost matrix for multi-animal tracking. <br>\- Test basic identity switches detection. | 15 |
| **Week 9** <br>  July 28 \- August 3 | \- Improve identity correction using re-identification techniques such as confidence scores.   <br>\- Implement the tests for identity switch correction and ask mentors for feedback. | 15 |
| **Week 10** <br>  August 4 \- August 10 | \- Optimize Kalman filter performance for multi-animal tracking. Optimization is required to make sure that switch corrections are identified correctly.   <br>\- Integration of identity correction in the movement codebase. <br>\- Ask mentors for feedback and suggestions. | 15 |
| **Week 11** <br>  August 11 \- August 17 | \- Start writing the documentation for Identity switch correction feature.   <br>\- Freeze the codebase. | 14 |
| **Week 12** <br>  August 18 \- August 24 | \- Finish remaining tests and documentation..   <br>\- Code polishing, final testing & performance checks. <br>\- Submit the final GSOC report. | 15 |

* **Communication plan**  
  I will communicate with my mentors daily on Zulip chat for guidance and continuous feedback. To review the progress from the previous week and discuss plans for the upcoming week, I would appreciate weekly video calls with my mentors.

## Personal statement

* **Past experience**  
  I have two years of experience in python and I am proficient in core machine learning libraries like numpy, pandas, xarray, sklearn and pytorch. I worked on many machine learning projects where I handle the datasets, pre-process the dataset and build the machine learning models. I have also taken part in numerous [Kaggle competitions](https://www.kaggle.com/angkul/code), additionally enhancing my skills. Beside core data processing and machine learning libraries, I am also proficient in libraries like langchain, crewai and smolagents.  
    
* **Motivation**

	There are two main reasons why I wanted to work on this project. First of all this is a rare and exciting project(there are only a few  
	projects which research on the animals) and second this project aligns with my skill set. I always wanted to work on a project where I       
  can apply my skill set in a real world scenario. So, this project gives me that opportunity. To be honest, I have never been good with   
  the data cleaning and processing but this time the work I have done so far for this project(all issues I solved, PRs), the time I spent,  
  gives me a chance to improve my skills and I understood the working of these libraries under the hood. This is one of the most exciting and important reason which motivates me to work on this project. 

  This project is more than about data, this project gives me an opportunity to contribute to open-source research and I will be helping so many  future researchers, scientists. This is very exciting for me and I am very excited to work on this project.  
	

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