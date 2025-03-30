# Datashuttle: Allow Google Drive or AWS as remote storage (Shrey)

## Personal Details

- **Full name**: Shrey Singh 
- **Email**: sshrey0007@gmail.com
- **GitHub username**: cs7-shrey
- **Zulip username**: Shrey Singh
- **Location & time-zone**: India, GMT+5:30 (Asia/Kolkata)
- **Personal website / project portfolio**: https://github.com/cs7-shrey 
- **Code contribution**
    - Added thread workers to transfer data asynchronously in datashuttle TUI without freezing the screen allowing the TUI to display a loading animation indicating transfer in progress.
        - Issue: [#431](https://github.com/neuroinformatics-unit/datashuttle/issues/431) (closed)
        - PR: [#479](https://github.com/neuroinformatics-unit/datashuttle/pull/479) (merged)

    - Developed a prototype version of the core project adding Google Drive and AWS S3 support in the Datashuttle Python API and TUI
        - Issue: [#407](https://github.com/neuroinformatics-unit/datashuttle/issues/407)
        - PR: [#503](https://github.com/neuroinformatics-unit/datashuttle/pull/503) 
    
    - Implemented functionality to search both central and local repositories for suggesting next subject/session in the TUI.
        - Issue: [#409](https://github.com/neuroinformatics-unit/datashuttle/issues/409)
        - PR: [#484](https://github.com/neuroinformatics-unit/datashuttle/pull/484)

    - Implemented support for SSH to Windows Machine. The current method of setting up SSH assumes the target machine to be linux/unix. 
        - Issue: [#450](https://github.com/neuroinformatics-unit/datashuttle/issues/450)
        - PR: [#477](https://github.com/neuroinformatics-unit/datashuttle/pull/477)
    
    - Added test for renaming file/folder on directorytree in TUI
        - Issue: [#323](https://github.com/neuroinformatics-unit/datashuttle/issues/323) (closed)
        - PR: [#496](https://github.com/neuroinformatics-unit/datashuttle/pull/496) (merged)

    - Reviewed testing approach for testing SSH transfers with Docker images in PR [#208](https://github.com/neuroinformatics-unit/datashuttle/pull/208)
        - Review link: [208/review](https://github.com/neuroinformatics-unit/datashuttle/pull/208#pullrequestreview-2708596155)

- **Proposal discussion link**: [GSoC PR #9](https://github.com/neuroinformatics-unit/gsoc/pull/9)

## Project Proposal

- **Synopsis**
    
    The project involves supporting data transfers to and from Google Drive and Amazon Web Services (AWS) buckets. It involves extending Rclone's existing features to support setting up connections to Google Drive or AWS buckets and creating the required screens and tabs in the TUI.

    **Why is the project important?**
    As neuroscience projects grow in size, Datashuttle helps such projects manage their data between central and local repositories helping them maintain a standard structure of the project. Datashuttle currently allows connections to central machines like an HPC via SSH. However, not all labs have access to such machines. Google Drive and AWS buckets are excellent options to store neuroscience data in such cases and many researchers will already be storing their data in them due to their widespread adoption. Integrating support for Google Drive and AWS buckets as remote storage would significantly enhance Datashuttle's flexibility, and adoption making Datashuttle useful for neuroscience experiments using or planning to use Google Drive or AWS as storage options.

    **Goals**
    
    - Implement setting up Rclone config for Google Drive and AWS and expose them Datashuttle's Python API.
    - Extend Datashuttle's wrapping of Rclone to support Google Drive and AWS transfers and add utility functions for the same.
    - Create TUI interface to expose the Python API to enable users to setup connections to Google Drive and AWS and transfer data via the TUI.
    - Write tests to ensure that the setup works correctly, transfers happen correctly, transfer settings (overwrite, dry run, etc.) work properly, connection failures are handled and TUI works as expected.
    - Update the documentation to include the new features in API reference and the "How to" section. 


- **Implementation timeline**

    **Deliverables**

    - Support for setting up connections to Google Drive and AWS and transferring data in the Datashuttle's Python API using Rclone.
    - TUI tabs and screens to enable users to setup connections to Google Drive and AWS and transfer data via the TUI.
    - Integration and TUI tests for the implemented features.
    - Documentation for setting up Google Drive or AWS as central storage.

    **Stretch Goals**

    - Adding support for additional storage options like Dropbox, Cloudflare, Ceph, etc. after surveying 
    - Progress bar for data transfers.


    **Weekly timeline**

    **Community Bonding Period (May 8 - June 1)**
    
    - Take feeback on existing PRs to get them merged.
    - Explore the codebase for implementation of the features.
    - Discuss the project and implementation details with the mentor(s).

    **Week 1-2 (June 2 - June 15)**
    
    - Implement Rclone's config setup for Google Drive and expose it in the Datashuttle's Python API.
    - Write tests to ensure the working of data transfers to and from Google Drive via Datashuttle's Python API.
    
    **Week 3-4 (June 16 - June 29)**

    - Implement TUI screens for setting up Google Drive as central storage.
    - Write TUI tests to make sure the interface is working as expected.

    **Week 5-6 (June 30 - July 13)**

    - Complete testing for Google Drive transfers and update documentation for setting up Google Drive as central storage.
    - Implement Rclone's config setup for AWS buckets and expose it in the Datashuttle's Python API.
    
    **Week 7-8 (July 14 - July 27)**

    - Write tests to ensure the working of transfers to and from AWS via Datashuttle's Python API.
    - Implement TUI interface for setting up AWS as central storage. 

    **Week 9-10 (July 28 - August 10)**

    - Write TUI tests to make sure the interface is working as expected.
    - Complete testing for AWS transfers and update documentation for setting up AWS as central storage.

    **Week 11-12 (August 11 - August 27)**

    - Buffer period for any pending work or improvements.
    - Prepare the final report and submit it.

- **Communication Plan** 

    I plan to communicate with my mentor on Zulip chat and Github and have weekly meetings to discuss the progress and any blockers. 


## Personal Statement

- **Past Experience**
    
    I have about two years of experience programming in Python. I have used Python for just about everything from backend development to machine learning (eg. [collaborative filtering](https://www.kaggle.com/code/kglshrey/fastai-collaborativefiltering)). I have developed web scraping scripts and coded high performance backends in Python. I also have experience in UI development using frameworks like React. Although I am new to open-source, I have been catching up quickly and have made a few contributions to Datashuttle. Here's my [first PR](https://github.com/neuroinformatics-unit/datashuttle/pull/479) that got merged.

    **Projects**
    - [Voice search for hotels](https://github.com/cs7-shrey/haven)
    - [RAG for YouTube videos](https://github.com/cs7-shrey/youtube-rag-chatbot)
    - [Cross-platform desktop todo app](https://github.com/cs7-shrey/broski)
    

- **Motivation**
    
    I have always been interested in authentication and data transfers. Enabling the support for Google Drive and AWS in Datashuttle would allow me to explore even more methods of authentication used by these storage options. It would also allow me to create visual interfaces to automate underlying configuration and connection setup. Nothing motivates me more than the fact that the functionalities developed during this program would be used in real world projects by neuroscience researchers. The idea of making a meaningful difference to the open-source community by working on something I enjoy doing is what drives me the most. It's not usual that being a student, one gets to work on a clean and modular codebase like Datashuttle. It would immensely help me improve my coding style in general and learn from the experienced developers in the community.

- **Match**

    This project lies at the intersection of my skills and my interests. Despite not having worked previously with Textual and Rclone, I was able to make meaningful contributions to Datashuttle. My ability to think from first principles helps me see problems at a fundamental level and think about solutions from the ground up. I am always open to feedback. I take complete responsibility of the work I do and I am always willing to learn and improve from my mistakes and criticism. I have developed a working [prototype version](https://github.com/neuroinformatics-unit/datashuttle/pull/503) of the core project and I understand the codebase deeply to complete the project with high standards. Just an interesting side note, I chose biology over maths in my high school (UK equivalent of A-levels); just when my high school was about to end, I developed an interest in computer science; I took a gap year; studied two years of high school mathematics in one year and qualified one of the toughest undergraduate examinations in the world, JEE Advanced, with a rank of 2346. I bring the same energy to everything that I love doing. Through the hurdles and the challenges of the project, the fact that I enjoy working on it is alone sufficient for me to keep going.

- **Availability**

    I have a summer break from my university and I am mostly free during the period from May 15 to August 1. For the month of August, I have a few classes but I can manage my time to work on the project. I am available for about 30-35 hours every week.


## GSoC

- **GSoC Experience**

    I expect to learn the best practices in software engineering through this program and explore more in the domain of data stores, data transfers and authentication. I expect to write well tested and documented code to create features that are useful to the neuroscience community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, I am only applying to this project.