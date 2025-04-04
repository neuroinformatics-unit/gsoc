# GSOC 2025 Application 


## Extend Spikewrap Test Functionality

## Personal details
Please include the following information:
- **Full name** : Ajitesh Kumar Singh
- **Primary Email** :  Ajitesh.Kumar@iiitb.ac.in
- **Secondary Email** : y.ajitesh710@gmail.com
- **GitHub username** : Transyltooniaa
- **Zulip username** : Ajitesh Kumar Singh
- **Location & time-zone** India (UTC+5.30) 
- **Personal website / project portfolio** (optional) :  [Linkedin](https://www.linkedin.com/in/ajitesh-kumar-singh-140529201/)


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

    This project focuses on improving the spikewrap test suite by extending beyond basic execution checks.

  
    **Goals:**
    - Expanding test coverage for critical but under-tested components (sync channel handling, preprocessing, sorting ,raw data).
    - Eliminating gaps in edge-case validation (invalid configurations, cross-run consistency).
    - Test Containerized Execution – Implement tests for Docker and Singularity environments to ensure consistent performance( Image Availability,Container Execution and Output Consistency).
    - Provide clear documentation to support and encourage community contributions.

- **Implementation timeline**
    
    **Deliverables**


    1. **Expanded Test Suite** – Comprehensive tests for sync handling, preprocessing, and sorting.  
    2. **Edge-Case Validation** – Tests for invalid configs, missing data, and cross-run consistency.  
    3. **Container Testing** – Docker/Singularity execution tests with image validation.  
    4. **Contributor Docs** – Clear test guidelines for community-driven improvements.

    **Stretch Goals**

    - Refine Existing Code – Address TODO comments in the main execution code to enhance functionality.
    - Work along with the motion detection team to further develop the project.


    **Weekly timeline**
    Below is the revised timeline table with 3–4 bullet points per period, excluding any mention of runtime_metrics.json and ensuring that improvements on existing code (including TODO areas) are addressed in the later weeks:

| **Timeline** | **Deliverables & Testing Objectives** |
|--------------|-----------------------------------------|
| **Pre GSoC Period (April 1 – May 7)** | • Explore the codebase and identify key modules (Sorting, Preprocessing, RawRun). <br> • Map test targets (e.g., invalid sorter names, Docker/Singularity path issues). <br> • Work on Existing Issues and Create Pull Requests for them.
| **Community Bonding Period (May 8 – June 1)** | • Collaborate with my mentor to review the tests document and refine test cases. <br> • Finalize the test suite structure into Sorting, Preprocessing, and Raw Data tests. <br>|
| **Week 1-2 (June 2 – June 15)** | • Implement core Sorting tests for parameter validation (e.g., invalid `per_shank`, `concat_runs`, and sorter names). <br> • Develop tests for error handling in invalid cases (e.g., missing Docker/Singularity images). <br> • Begin drafting tests for missing preprocessing functions such as `phase_shift` and `bandpass_filter`. |
| **Week 3-4 (June 16 – June 29)** | •  Develop tests for Docker integration, ensuring automatic image downloads and consistent execution outputs in both local and CI environments. <br> • Implement Singularity tests to ensure proper image download and execution in shared paths. <br> • Enhance SLURM tests by validating job scripts, adding support for loading required modules (e.g., MATLAB) in SLURM scripts, and tracking dependencies effectively.|
| **Week 5-6 (June 30 – July 13)** | • Validate sorting outputs: check non-empty spike data and correct overwrite behavior when simulating existing outputs. <br> • Verify that **sorter outputs are saved in the correct locations**. <br> • Test preprocessing step orders, invalid parameters (e.g., `freq_min > freq_max`), and output key naming conventions. <br> • Continue drafting tests for additional preprocessing functions (e.g.`common_reference`). |
| **Week 7-8 (July 14 – July 27)** | • Implement tests for raw data loading, probe extraction, and sync channel operations in RawRun, SeparateRawRun, and ConcatRawRun. <br> • Validate sync channel operations (silence, save, plot) against raw data lengths. <br> • Validate that mixed preprocessing approaches (e.g., per-shank vs. non-per-shank) do not cause inconsistencies when loading from disk. |
| **Week 9-10 (July 28 – August 10)** | • Integrate all tests across Sorting, Preprocessing, and Raw Data modules to ensure comprehensive coverage. <br> • Develop tests for parallel sorting execution and concurrency, confirming that downstream functions correctly load outputs. <br> • Ensure that temporary test files are properly deleted after execution. <br> • Finalize detailed inline documentation and technical comments for all tests. |
| **Week 11-12 (August 11 – August 27)** | • Run the complete test suite across environments (Linux/macOS, CI/CD with Docker/Singularity) to ensure cross-platform compatibility and proper file permissions. <br> • Address pending issues and refine tests based on feedback from previous runs. <br> • Work on improving existing code where TODOs have been mentioned, ensuring the improvements integrate smoothly with the test suite. |
| **Week 12 (August 28 – September 1)** | • Use the buffer period to resolve any final issues and optimize test execution times. <br> • Conduct a last round of code improvements on existing modules marked with TODOs. <br> • Finalize and submit the comprehensive project report with complete documentation of the testing strategy and code enhancements. |



## Personal statement

_Length: max 0.75 page_

- **Past experience** 
    
    With over 2 years of experience in developing Python-based applications, I have worked on projects like building backend for web apps using Django and Flask framework, Automation scripts using Python and Machine Learning (Traditional,Deep Learning,Computer Vision and Reinforcement Learning). Along with my team, I built a Vision-Based Product Inspection system for Flipkart (Ecommerce giant in India) in a hackathon in which we were among the top 10 teams out of 3500 teams.
    
    **Projects**
    - [Vision-Based Product Inspection](https://github.com/Transyltooniaa/FlipkartGrid_SmartVision.git)
    - [ImageEffect Application](https://github.com/Transyltooniaa/ImageEffect.git)
    - [SportsPal](https://github.com/Transyltooniaa/SportsPal.git)

    

- **Motivation: why this project?**

    Writing tests for the Spikewrap is a great way to learn about the project and its features. It demonstrates a strong understanding of code quality, debugging, and software development best practices, which are highly valued qualities in a developer. This project is a great opportunity to learn and grow in these areas, Plus, it’s a great chance for me to contribute to an open-source project that directly supports scientific research while learning from experienced developers along the way. I am highly motivated to work on this project and bring an impactful contribution to the community.
        
- **Match: why you?**

    Having worked with python for over 2 years, I am confident in my ability to write clean and efficient code. I am also a quick learner and can adapt to new technologies quickly
    Experience building production-level applications at 
    [NIMHANS Lab](https://www.iiitb.ac.in/media/iiitbangalore-and-nimhans-collaborate-to-deliver-the-tele-manas-app-for-247-mental-health-support) at IIIT-Bangalore has equipped me to handle technical challenges and adapt to evolving project requirements. 

 
- **Availability**

    As a college student, I intend to utilise my summer breaks from May to July to work on the project. After completing my University exams in April, I will start working in May. I can dedicate 40 hours a week from May to July, while in August after the classes commence, I can dedicate about 25 hours a week. 
    There are no exams or planned vacations throughout the coding period. I generally work from 4 PM to 2 AM IST (6:30 AM to 4:30 PM Eastern Time), although I find it flexible to adjust my working hours if required. 
    Besides this project.


## GSoC

_Length: max 0.25 page_

- **GSoC experience**
    Through the GSoC program, I will gain valuable experience not only in the open-source community but also in industry-level software development. This will allow me to collaborate with experienced developers, improve my coding and problem-solving skills, and learn best practices for working in a professional development environment. Additionally, I will gain firsthand experience in contributing to real-world projects, enhancing my ability to work effectively within a team.

- **Are you also applying to projects with other organisations in GSoC 2025?**
    
    I have no plans to submit a proposal to any other organisation or project.

