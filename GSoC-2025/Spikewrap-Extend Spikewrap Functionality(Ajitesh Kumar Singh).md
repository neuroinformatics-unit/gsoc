# GSOC 2025 Application 


## Extend Spikewrap Test Functionality

## Personal details
Please include the following information:
- **Full name** :   Ajitesh Kumar Singh
- **Primary Email** :  Ajitesh.Kumar@iiitb.ac.in
- **Secondary Email** : y.ajitesh710@gmail.com
- **GitHub username** : Transyltooniaa
- **Zulip username** : Ajitesh Kumar Singh
- **Location & time-zone** : India (UTC+5.30) 
- **Personal website / project portfolio** (optional) : [Linkedin](https://www.linkedin.com/in/ajitesh-kumar-singh-140529201/)


- **Code contribution**
    - [Automate Sphinx Documentation Deployment with Versioned Switcher](https://github.com/neuroinformatics-unit/datashuttle/pull/486) : 
    Automates Sphinx docs deployment using GitHub Actions, deploying tagged releases to versioned directories, updating switcher.json, and maintaining the latest release.
    
    - [Enhance Existing Slurm test](https://github.com/neuroinformatics-unit/spikewrap/pull/229) : This PR ensures that the synchronization file is correctly saved by asserting its existence in the specified directory.

    - [Add option to delete a project](https://github.com/neuroinformatics-unit/datashuttle/issues/436) :
        Developed a function to delete both the DataShuttle project configuration and associated data from local and central paths. The implementation is currently on hold until it is requested by a user. But, the issue is left open and serves as a reference for future extensions.

    - [Completing Docstring for parameters of get_next_sub ](https://github.com/neuroinformatics-unit/datashuttle/pull/482) :
        Adding docstrings for the parameters of get_next_sub function.This PR was prompted by a previous comment, leading to the opening of a related issue [#483](https://github.com/neuroinformatics-unit/datashuttle/issues/483)
    
    - [Implemented New Getters](https://github.com/neuroinformatics-unit/datashuttle/pull/480) :
    This PR introduces two new methods to streamline folder lookups within the datashuttle. 

    **Merged** : 
    
    - [Clipping Python version to avoid dependency conflicts](https://github.com/neuroinformatics-unit/spikewrap/pull/234)
  
    - [Fixing json syntax in the mountainsort5 sorting yaml](https://github.com/neuroinformatics-unit/spikewrap/pull/228)  

- **Proposal discussion link**

    [Pull Request Link](https://github.com/neuroinformatics-unit/gsoc/pull/40/files)

## Project proposal 
_Length: max 1 page_

- **Synopsis**

    This project focuses on improving the existig Spikewrap test suite by extending beyond basic execution checks as well as creating new test cases to validate the functionality of existing modules and features.

  
    **Goals:**
    - Expanding test coverage for the most important but under-tested components (sync channel handling, preprocessing, sorting ,raw data).
    - Completing edge-case validation of the already implemented tests(invalid configurations, cross-run consistency).
    - Test Containers – Implement tests for Docker and Singularity environments to ensure consistent performance (Image Availability,Container Execution and Output Consistency).
    - Provide clear documentation for others to contribute.

- **Implementation timeline**
    
    **Deliverables**

    1. **Expanded Test Suite** : Comprehensive tests for sync handling, preprocessing, and sorting.  
    2. **Edge-Case Validation** : Tests for invalid configs, missing data, and cross-run consistency.  
    3. **Container Testing** : Docker/Singularity execution tests with image validation.  
    4. **Contributor Docs** : Clear test guidelines for others to contribute.

    **Stretch Goals**

    - Refine Existing Code : Address TODO comments in the main execution code to enhance functionality. [Example](https://github.com/neuroinformatics-unit/spikewrap/blob/1285936fe7a88f5660744f26135df353ff24076f/spikewrap/structure/_preprocess_run.py#L47)
    - Work along with the motion detection team to further develop the project.


    **Weekly timeline**

| **Timeline** | **Deliverables & Testing Objectives** |
|--------------|-----------------------------------------|
| **Pre GSoC Period (April 1 – May 7)** | • Explore the codebase and understand key modules (Sorting, Preprocessing, RawRun).  <br> • Work on existing issues and create PR for them.
| **Community Bonding Period (May 8 – June 1)** | • Work with my mentor to review the tests document and refine test cases. <br> • Finalize the test suite structure for Sorting, Preprocessing, and Raw Data tests. <br>|
| **Week 1-2 (June 2 – June 15)** | • Implement Sorting tests for validating parameters  (e.g., invalid `per_shank`, `concat_runs`, and sorter names). <br> • Develop tests for handling invalid cases (e.g., missing Docker/Singularity images). <br> • Continue tests for missing preprocessing functions (`phase_shift` and `bandpass_filter`.) |
| **Week 3-4 (June 16 – June 29)** | •  Develop tests for Docker integration, ensuring automatic image downloads and consistent outputs in both local and CI environments. <br> • Implement Singularity tests to ensure proper image download and execution in shared paths. <br> 
| **Week 5-6 (June 30 – July 13)** | • Validate sorting outputs: check for non-empty spike data and correct overwrite behavior when simulating existing outputs. <br> • Verify that sorter outputs are saved in the correct locations. <br> • Test preprocessing step orders and invalid parameters 
| **Week 7-8 (July 14 – July 27)** | • Implement tests for loading raw data, probe extraction, and sync channel operations in RawRun, SeparateRawRun, and ConcatRawRun. <br> • Validate that mixed preprocessing approaches (e.g., per-shank vs. non-per-shank) do not raise errors when loaded from the disk. |
| **Week 9-10 (July 28 – August 10)** | • Develop tests for parallel sorting execution to make sure that downstream functions correctly show outputs. <br> • Validate sync channel operations (silence, save, plot) for the raw data. <br> • Finalize docstring/documentation for all tests. |
| **Week 11-12 (August 11 – August 27)** | • Ensure that temporary test files are properly deleted after execution. <br> • Run the complete tests in all environments for compatibility and file permissions check. <br> • Address pending issues and refine tests based on feedback from previous runs. |
| **Week 12 (August 28 – September 1)** | •  Resolve any final issues in buffer time <br> • Finalize and submit the report with complete documentation 



## Personal statement

_Length: max 0.75 page_

- **Past experience** 
    
    With over 2 years of experience in developing Python-based applications, I have worked on projects like building backend for web apps using Django and Flask framework, Automation scripts using Python and Machine Learning (Traditional,Deep Learning,Computer Vision and Reinforcement Learning). Along with my team, I built a Vision-Based Product Inspection system for Flipkart (Ecommerce giant in India) in a hackathon in which we were among the top 10 teams out of 3500 teams.
    
    **Projects**
    - [Vision-Based Product Inspection](https://github.com/Transyltooniaa/FlipkartGrid_SmartVision.git)
    - [ImageEffect Application](https://github.com/Transyltooniaa/ImageEffect.git)
    - [SportsPal](https://github.com/Transyltooniaa/SportsPal.git)

    

- **Motivation: why this project?**

    Writing tests for a young project like Spikewrap is a great way for me to learn about its features. To do this, I need to have a good understanding of code quality, debugging, and software development best practices, which are highly valued qualities in any developer. This project is a great opportunity to learn and grow in these areas, Plus, it will be a great chance for me to contribute to an open-source project that directly supports scientific research at the same time learning from experienced developers . I am highly motivated to work on this project and bring an impactful contribution to the community.
        
- **Match: why you?**

    Having worked with python for over 2 years, I am confident in my ability to write clean and efficient code. I am also a quick learner and can adapt to new technologies quickly
    Experience building production-level applications at 
    [NIMHANS Lab](https://www.iiitb.ac.in/media/iiitbangalore-and-nimhans-collaborate-to-deliver-the-tele-manas-app-for-247-mental-health-support) at IIIT-Bangalore has equipped me to handle technical challenges and adapt to evolving project requirements.
    The desire of proving myself always keeps me motivated to accomplish and tackle new challenges.


 
- **Availability**

    As a college student, I intend to utilise my summer breaks from May to July to work on the project. After completing my University exams in April, I will start working in May. I can dedicate 40 hours a week from May to July, while in August after the classes commence, I can dedicate about 25 hours a week. 
    There are no exams or planned vacations throughout the coding period. I generally work from 4 PM to 2 AM IST (6:30 AM to 4:30 PM Eastern Time), although I find it flexible to adjust my working hours if required. 
    Besides this project.


## GSoC

_Length: max 0.25 page_

- **GSoC experience**
    From the GSoC program, I will get industry-level experience as well as hands-on experience not only within the open-source domain but also at the industry level in terms of software development. I will learn best practices regarding work within an industry-standard development environment. It will give me a firsthand experience with real-world contribution, thus ensuring I become highly proficient at work within a team environment.


- **Are you also applying to projects with other organisations in GSoC 2025?**
    
    I have no plans to submit a proposal to any other organisation or project.

