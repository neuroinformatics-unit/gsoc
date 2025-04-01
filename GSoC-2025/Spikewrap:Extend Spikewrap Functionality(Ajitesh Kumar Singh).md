# GSOC 2025 Application 


## Extend Spikewrap Test Functionality

## Personal details
Please include the following information:
- **Full name** : Ajitesh Kumar Singh
- **Primary Email** :  Ajitesh.Kumar@iiitb.ac.in
- **Secondary Email** : y.ajitesh710@gmai.com
- **GitHub username** : Transyltooniaa
- **Zulip username** : Ajitesh Kumar Singh
- **Location & time-zone** India (UTC+5.30) 
- **Personal website / project portfolio** (optional) : https://www.linkedin.com/in/ajitesh-kumar-singh-140529201/


- **Code contribution**
    - [Automate Sphinx Documentation Deployment with Versioned Switcher](https://github.com/neuroinformatics-unit/datashuttle/pull/486)  
        Addresses [#372](https://github.com/neuroinformatics-unit/datashuttle/issues/372): Automates Sphinx docs deployment using GitHub Actions, deploying tagged releases to versioned directories, updating switcher.json, and maintaining the latest release.

    - [Add option to delete a project](https://github.com/neuroinformatics-unit/datashuttle/issues/436)
        Developed a function to delete both the DataShuttle project configuration and associated data from local and central paths. The implementation is currently on hold until it is requested by a user. But, the issue is left open and serves as a reference for future extensions. 

    - **merged** : [Fixing json syntax in the mountainsort5 sorting yaml](https://github.com/neuroinformatics-unit/spikewrap/pull/228)  
    While exploring the codebase and trying to understand it to better, I caught upon this minor syntax error and fixed it.

    - [Completing Docstring for parameters of get_next_sub ](https://github.com/neuroinformatics-unit/datashuttle/pull/482)
        Adding docstrings for the parameters of get_next_sub function. TDocstrings were added for the parameters of the get_next_sub function. This PR was prompted by a previous comment, leading to the opening of a related issue [#483](https://github.com/neuroinformatics-unit/datashuttle/issues/483)
    
    - [Implemented New Getters](https://github.com/neuroinformatics-unit/datashuttle/pull/480)
    This PR introduces two new methods to streamline folder lookups within the datashuttle. Although the functionality of get_all_sub_and_ses_names which is now called get_all_sub_and_ses_paths was introduced in [#464]() which was soon to
    be merged at that time, But since this was my first pull request , it help me understand the codebase.

    - [Devlopment of Website for National Institute of Mental Health and Neuro Sciences](https://www.nimhans.ac.in/)
    ![image](https://github.com/Transyltooniaa/gsoc/blob/MyProposal/GSoC-2025/Nimhans.png) 
    A private Repository so cannot be shared

- **Proposal discussion link**

    Please link to the pull request where you discussed your project proposal with the community. 

## Project proposal 
_Length: max 1 page_

- **Synopsis**

    The project involves developing a robust test suite for spikewrap. This involves moving beyond basic smoke tests that only check for error-free execution and instead focus on verifying that the outputs are exactly as expected. For instance, enhancing SLURM tests—which currently rely on assumptions based on non-SLURM runs—by explicitly validating their results.

    This project is important because it will greatly enhance the reliability of spikewrap, as well as its accuracy.SLURM-based execution must be rigorously tested to confirm that job scheduling, resource allocation, and parallel execution do not introduce unexpected issues.

    **Goals:**
    - Enhance SLURM tests to explicitly validate outputs.
    - Replace superficial smoke tests with detailed checks for correctness.
    - Integrate the comprehensive test suite into a continuous integration workflow.
    - Provide clear documentation to support and encourage community contributions.

- **Implementation timeline**
     **Deliverables**

    - Develop a comprehensive test suite covering preprocessing, sorting, and SLURM execution.
    - Enhance SLURM tests to explicitly validate outputs.
    - Enhance existing smoke tests to validate correctness.
    - Completing docstring for the tests and existing code.
    - Document the testing framework for future contributors.

    **Stretch Goals**

    - Improve the effieciency of the existing functions with new approaches.
    - Work along with the motion detection team to further develop the project.


    **Weekly timeline**

    <table>
    <thead>
        <tr>
            <th>Timeline</th>
            <th>Deliverables</th>
        </tr>
    </thead>
    <tbody>
    <tr>
        <td><strong>Pre GSoC Period <br> (April 1 - May 7)</strong></td>
            <td>
                <ul>
                    <li>Go through the codebase to understand the existing features and architecture.</li>
                    <li>Work on Existing Issues and Create Pull Requests for them.</li>
                    <li>Work on those PR after Code reviews.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><strong>Community Bonding Period <br> (May 8 - June 1)</strong></td>
            <td>
                <ul>
                    <li>With the help of my mentor, I’ll help to familiarize myself with the community and the codebase.</li>
                    <li> Identify missing test cases and plan the test suite structure.</li>
                    <li>Discuss project implementation details and finalize the approach with mentors</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><strong>Week 1-2 <br> (June 2 - June 15)</strong></td>
            <td>
                <ul>
                    <li>Analyze unit tests for core preprocessing and sorting functionalities.</li>
                    <li>Begin replacing smoke tests with detailed output validation.</li>
                    <li>Optimize existing functions using better approaches (as mentioned in the comments in the codebase).</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><strong>Week 3-4 <br> (June 16 - June 29)</strong></td>
            <td>
                <ul>
                    <li> Extend SLURM-specific tests to explicitly validate outputs. </li>
                    <li>Test Singularity integration within the pipeline.</li>
                    <li>Identify and address any testing gaps in preprocessing and sorting.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><strong>Week 5-6 <br> (June 30 - July 13)</strong></td>
            <td>
                <ul>
                    <li>Implement additional validation for test cases, ensuring correctness across different HPC environments.</li> 
                    <li>Optimize test execution time for better efficiency. </li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><strong>Week 7-8 <br> (July 14 - July 27)</strong></td>
            <td>
                <ul>
                    <li> Work on test cases for TestLegacyOpenEphysLoading  TestSpikeGLXRunLoading</li>
                    <li>Improve test coverage for sync,probe and whiten.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><strong>Week 9-10 <br> (July 28 - August 10)</strong></td>
            <td>
                <ul>
                    <li>Finalize comprehensive test coverage for all the classes. </li>
                    <li>Improve logging and debugging tools for failed test cases.</li>
                    <li>Complete docstring for the tests and corresponding methods.</li>
                </ul>
            </td>
        </tr>
            <td><strong>Week 11-12 <br> (August 11 - August 27)</strong></td>
            <td>
                <ul>
                    <li>Resolve pending issues and finalize test suite.</li>
                    <li>
                       Prepare the final project report and seek mentor feedback.
                    </li>
                    <li>Ensure all deliverables are well-documented and ready for submission.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><strong>Week 12-12 <br> (August 28 - September 1)</strong></td>
            <td>
                <ul>
                    <li>Buffer period for any pending work or improvements.</li>
                    <li>Submit the final report and complete project wrap-up.</li>
                </ul>
            </td>
        </tr>
        <tr>
    </tbody>
</table>


## Personal statement

_Length: max 0.75 page_

- **Past experience** 
    
    With over 2 years of experience in developing Python-based applications, I have worked on projects like building backend for web apps using Django and Flask framework,Automation scripts using Python and Machine Learning (Traditional,Deep Learning,Computer Vision and Reinforcement Learning). Along with my team, I built a Vision-Based Product Inspection system for Flipkart (Ecommerce giant in India) in a hackathon in which we were among the top 10 teams out of 3500 teams.
    
    **Projects**
    - [Vision-Based Product Inspection](https://github.com/Transyltooniaa/FlipkartGrid_SmartVision.git)
    - [ImageEffect Application](https://github.com/Transyltooniaa/ImageEffect.git)
    - [SportsPal](https://github.com/Transyltooniaa/SportsPal.git)

    

- **Motivation: why this project?**

    Writing tests for the spikewrap project is a great way to learn about the project and its features.It demonstrates a strong understanding of code quality, debugging, and software development best practices, which are highly valued qualities in a developer. Having a strong interest in cloud computing and HPC, I am excited to work on a project that will help me understand the practical aspects of cloud computing and HPC.
        
- **Match: why you?**

    Having worked with python for over 2 years, I am confident in my ability to write clean and efficient code. I am also a quick learner and can adapt to new technologies quickly.
    
    Experience building production-level applications at 
    [NIMHANS Lab](https://www.iiitb.ac.in/media/iiitbangalore-and-nimhans-collaborate-to-deliver-the-tele-manas-app-for-247-mental-health-support) at IIIT-Bangalore has equipped me to handle technical challenges and adapt to evolving project requirements. 

    I cleared JEE Advanced with a rank of 1500 and GATE exam with a rank of 1551, one of the world's toughest exams with an acceptance rate of just 1%,. This earned me a seat at IIIT-bangalore (One of the best research institutes in India) which is in IT hub of India. This was possible because of my nature to never give up on things and my determination to succeed.My strong problem-solving skills, honed through academic challenges, ensure I can tackle complex tasks effectively. I believe with my hardwork and consistency, I will be able to succeed in this project.

- **Availability**

    As a college student, I intend to utilise my summer breaks from May to July to work on the project. After completing my University exams in April, I will start working in May. I can dedicate 40 hours a week from May to July, while in August after the classes commence, I can dedicate about 25 hours a week. 
    There are no exams or planned vacations throughout the coding period. I generally work from 4 PM to 2 AM IST (6:30 AM to 4:30 PM Eastern Time), although I find it flexible to adjust my working hours if required. 
    Besides this project, I have no commitments/vacations planned for the summer. I shall keep my status posted to all the community members every week and maintain transparency in the project.
    I am 100% dedicated to Neuroinformatics Unit and have no plans to submit a proposal to any other organisation or project.


## GSoC

_Length: max 0.25 page_

- **GSoC experience**
    Through the GSoC program, I will gain valuable experience not only in the open-source community but also in industry-level software development. This will allow me to collaborate with experienced developers, improve my coding and problem-solving skills, and learn best practices for working in a professional development environment. Additionally, I will gain firsthand experience in contributing to real-world projects, enhancing my ability to work effectively within a team.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I have no plans to submit a proposal to any other organisation or project.

