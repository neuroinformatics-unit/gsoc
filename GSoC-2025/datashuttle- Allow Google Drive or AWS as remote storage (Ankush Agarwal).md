# datashuttle: Allow Google Drive or AWS as remote storage (Ankush Agarwal)

## Personal details
Please include the following information:
- **Full name** : Ankush Agarwal
- **Email** : ankush.agarwal.202@gmail.com
- **GitHub username** : TheAnkushAgarwal
- **Zulip username** : Ankush Agarwal
- **Location & time-zone**: India (IST - Indian Standard Time, UTC +5:30)
- **Personal website / project portfolio** (optional)
- **Code contribution** :
  
  - [PR #481](https://github.com/neuroinformatics-unit/datashuttle/pull/481): Add v* in workflow tags to solve issue [#440](https://github.com/neuroinformatics-unit/datashuttle/issues/440). This PR got merged and is very useful for ensuring that incorrect-formatted tags are not accidentally pushed.
  - [PR #476](https://github.com/neuroinformatics-unit/datashuttle/pull/476) : Enable the 'save' button on configs when widget input is changed to solve issue [#330](https://github.com/neuroinformatics-unit/datashuttle/issues/330). This PR closes the issue [#330](https://github.com/neuroinformatics-unit/datashuttle/issues/330) as the benefits of the functionality added were outweighed by costs in code implementation, due to edge cases that the original issue [#330](https://github.com/neuroinformatics-unit/datashuttle/issues/330) did not consider. 

- **Proposal discussion link**
  - [neuroinformatics-unit#31](https://github.com/neuroinformatics-unit/gsoc/pull/31)

## Project proposal 

**Synopsis**

At present, datashuttle facilitates the transfer of data from one operating system to another through SSH and mounted drives. This project development extends the datashuttle capabilities to transfer data between user systems and cloud storage solutions across Google Drive, Dropbox and AWS Amazon Web Service buckets. The connectivity changes will incorporate RClone because RClone provides support for those cloud services. New features from cloud storage solutions provide datashuttle with advanced capabilities that benefit researchers in neuroscience. Some contributors have started contributing to this project by implementing some of the features, so I am extending this project and will be implementing Dropbox too as a storage option.


**Implementation Timeline**

Minimal Deliverables:
1. A new functionality will be added to the Python API to allow file transfers directly from Google Drive.
2. Extension of Python API for Dropbox, AWS bucket transfers
3. The system will establish TUI to enable users setup their connection to Dropbox, AWS bucket and Google Drive through the TUI interface.
4. Writing unit tests and integration tests for all new functionality
5. Documentation for both user-facing features and developer APIs


Stretch Goals:
1. Enhancing the TUI and  developing support for transfer progress visualization in the TUI
2. Optimization for large dataset transfers
3. Support for additional storage solutions, based on community needs such as Ceph, Cloudflare, FTP.
4. Scope for implementing additional features after consulting with my mentor and completing all remaining work throughout the journey of development.


**Weekly Timeline (12 weeks * 15 hours = ~ 180 hours):**

| Week | Tasks | Hours per week|
|------|-------|-------|
| Community Bonding | Study datashuttle codebase, understand RClone API for cloud services, discuss the implementation details with mentors, familiarize with project standards | 15-20 |
| Week 1-2 | Implement basic Google Drive connection functionality in Python API, write initial tests, Complete Google Drive implementation, check for bugs and errors, complete writing tests| 15-20 |
| Week 3-4 | Begin Dropbox implementation in Python API, write initial tests, Complete Dropbox implementation, check for bugs and errors, complete writing tests | 15-20 |
| Week 5-6 | Begin AWS S3 bucket implementation in Python API, write initial tests, Complete AWS implementation, prepare mid-term deliverables | 15-20 |
| Week 7-8 | Begin TUI integration for Google Drive and Dropbox, Complete TUI integration for Google Drive and Dropbox, begin TUI integration for AWS | 15-20 |
| Week 9-10 | Complete TUI integration for AWS, comprehensive testing of API and TUI implementations, Write user documentation for cloud storage features | 15-20 |
| Week 11-12 | Code freeze, focus on completing tests and documentation, Final testing, documentation refinement, prepare for final submission | 15-20 |

**Communication Plan**

The project period will involve continuous communication between me and my mentor through regular sessions.
1. I will organize video discussions sessions every week to evaluate project developments together with discussing obstacles and future action steps.
2. I will use Zulip chat to share daily updates about my progress alongside any encountered obstacles and for fast questions between regular meetings without set times.

I will maintain flexible meeting hours to address time zone differences because I am located in IST at UTC+5:30 and I guarantee fast replies to all messages.

## Personal Statement

- **Past Experience**

  My skills in Python programming create a solid base while I remain a new developer in the open-source community. I proved my ability to read and modify datashuttle codebase through my recent work.

  - [Solved Issue #440](https://github.com/neuroinformatics-unit/datashuttle/pull/481)
  - [Solved Issue #330](https://github.com/neuroinformatics-unit/datashuttle/pull/476)

  I started my open-source contribution with the Neuroinformatics Unit organisation in March 2025. In such a short span of time, I was able to contribute to the dattashuttle repository and tried solving 2 issues along with my mid-term examinations at my university. My first open-source PR got merged with NIU and this organisation will remain close to my heart forever. 


- **Motivation: Why This Project?**

  As from the past 1 month I am contributing to dattashuttle repository and I am familiar with the codebase. I have past experience in working with Python and this project excites me as I will be able to learn and grow. 

  The real-world impact of this project (datashuttle project), the technical challenge of integrating cloud services and the opportunity to contribute to an open source organisation motivates me.

- **Match: Why Me?**

  I am currently pursuing my Bachelor of Technology degree in Information Technology branch from Dr. B.R. Ambedkar National Institute of Technology Jalandhar. In my 3rd year of undergrad, I served as a founder in building the product [ColdScribe](https://www.producthunt.com/products/coldscribe#coldscribe). Coldscribe is an AI tool which generates customised cold emails. It uses Nextjs, Django and AWS services. Moreover, I have built a [Next.js landing page template](https://theankushagarwal.gumroad.com/l/NextjsLandingPage) and sold it on Gumroad, showcasing my passion for technology and continuous learning. 

  The combination of my technical expertise along with my current work at the datashuttle repository positions me to handle this project effectively.

  1. Through my previous work I showed my ability to use the datashuttle codebase as I contributed to it.
  2. My knowledge of Python includes programming with external APIs
  3. I have obtained basic knowledge of Google Drive and AWS together with other cloud platforms.

  Additionally, I like to write detailed-oriented and well-documented code. I will thoroughly test my code before raising PR. I am punctual and will deliver my work on time. My undergrad knowledge will also be helpful. 

  Apart from this, in the past, I have cleared JEE Mains examination and secured [98.75](https://drive.google.com/file/d/1CIgjOKSJvJNsuo1A_1i1n2a6zRfnDQwV/view?usp=sharing) percentile. It is considered one of the toughest logical examinations of India and around 1 million students appear for this examination. 

- **Availability**

  I am fully available to commit approximately 20 hours per week or more (as per project requirement of 175 total hours ) to this project throughout the GSoC period. I have no other major commitments during this time. Moreover, I will be having summer break from my university (Dr. B.R. Ambedkar National Institute of Technology Jalandhar) and I will not be involved in any other work during this period.

## GSoC

- **GSoC Experience**


  Google Summer of Code will deliver the following benefits to me:
  1. To receive valuable mentorship and guidance from experienced developers.
  2. The participation in this open source project will help me develop experience in building meaningful contributions to both real-world applications and open source systems.
  3. Growth in my technical skills.
  4. I will have the ability to establish myself as a future developer for the Neuroinformatics Unit organization.


- **Are you also applying to projects with other organisations in GSoC 2025?**

  I am not applying to any other GSoC organisation. I have chosen Datashuttle because it combines my skills perfectly and provides me with existing knowledge of the codebase due to earlier work.
