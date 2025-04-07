# datashuttle - Deploy datashuttle as installable package (Ankush Agarwal)

## Personal details
- **Full name**: Ankush Agarwal
- **Email**: ankush.agarwal.202@gmail.com
- **GitHub username**: TheAnkushAgarwal
- **Zulip username**: Ankush Agarwal
- **Location & time-zone**: India (IST - Indian Standard Time, UTC +5:30)
- **Personal website / project portfolio** (optional)
- **Code contribution**:
  - [PR #481](https://github.com/neuroinformatics-unit/datashuttle/pull/481): Add v* in workflow tags to solve issue [#440](https://github.com/neuroinformatics-unit/datashuttle/issues/440). This PR got merged and is very useful for ensuring that incorrect-formatted tags are not accidentally pushed.
  - [PR #476](https://github.com/neuroinformatics-unit/datashuttle/pull/476): Enable the 'save' button on configs when widget input is changed to solve issue [#330](https://github.com/neuroinformatics-unit/datashuttle/issues/330). This PR closes the issue [#330](https://github.com/neuroinformatics-unit/datashuttle/issues/330) as the benefits of the functionality added were outweighed by costs in code implementation, due to edge cases that the original issue [#330](https://github.com/neuroinformatics-unit/datashuttle/issues/330) did not consider.
- **Proposal discussion link**: 
  - [neuroinformatics-unit#50](https://github.com/neuroinformatics-unit/gsoc/pull/50)

## Project proposal

### Synopsis

Users face a substantial challenge when using the datashuttle project because it needs conda to operate. The project development targets datashuttle's transformation into a stand-alone executable program that functions across Windows, macOS and Linux platforms without user coding or dependencies.The main obstacle to overcome is that datashuttle's terminal user interface stems from Textual software which produces inadequate display results in original system terminal programs. The solution requires collecting information about adding terminal emulators to software packages. By leveraging packaging tools like PyInstaller, Hatch or Briefcase, we can create cross-platform distribution of a datashuttle executable. And by leveraging tools like Rich or PyTermGUI, we can create cross-platform terminal UI. 

Enhancing datashuttle will expand its user base by allowing researchers who require its functionality to use it without needing technical skills. Removing the conda requirement helps to remove entry obstacles thus expanding available user numbers.

### Implementation timeline

- #### Minimal set of deliverables:
  - A thorough research and evaluation of packaging tools (PyInstaller, Hatch, Briefcase) and terminal UI libraries (Rich, PyTermGUI)
  - Cross-platform executable distribution of datashuttle for Windows, macOS, and Linux
  - The application benefits from an automated testing solution that utilizes GitHub CI to build projects
  - Documentation for maintenance and future development and preparing the installation guide which will cover all deployment platforms supported by our application

- #### Stretch goals:
  - Auto-update functionality for the standalone application

- #### Weekly timeline (12 weeks * 30 hours = ~360 hours):

| Week | Tasks | Hours per week |
|------|-------|-------|
| Community bonding | Create a development environment, research Python packaging systems and terminal UI libraries, set up initial testing environment | 30 |
| Week 1-2 | Evaluate packaging tools (PyInstaller, Hatch, Briefcase) and terminal UI libraries (Rich, PyTermGUI), create proof-of-concept implementations, document findings and recommendations | 30-35 |
| Week 3-4 | Implement chosen packaging solution for Windows, develop prototype with selected terminal UI library, resolve platform-specific issues | 30-35 |
| Week 5-6 | Start implementation to macOS, test terminal UI rendering across different macOS versions| 30-35 |
| Week 7-8 | Start implementation to Linux, test terminal UI rendering across different Linux versions | 30-35 |
| Week 9-10 | Set up Continuous Integration (CI) pipeline for automated builds, implement testing framework for packaged applications | 30-35 |
| Week 11-12 | Optimize code, create documentation, focus on final testing and bug fixes, prepare final deliverables | 30-35 |

- **Communication Plan**

The project period will involve continuous communication between me and my mentor through regular sessions.
1. I will organize video discussions session every week to evaluate project developments together with discussing obstacles and future action steps.
2. I will use Zulip chat to share daily updates about my progress alongside any encountered obstacles and for fast questions between regular meetings without set times.

I will maintain flexible meeting hours to address time zone differences because I am located in IST at UTC+5:30 and I guarantee fast replies to all messages.

## Personal statement

- ### Past experience

My skills in Python programming create a solid base while I remain a new developer in the open-source community. I proved my ability to read and modify datashuttle codebase through my recent work.

- [Solved Issue #440](https://github.com/neuroinformatics-unit/datashuttle/pull/481)
- [Solved Issue #330](https://github.com/neuroinformatics-unit/datashuttle/pull/476)

I started my open-source contribution with the Neuroinformatics Unit organisation in March 2025. In such a short span of time, I was able to contribute to the dattashuttle repository and tried solving 2 issues along with my mid-term examinations at my university. My first open-source PR got merged with NIU and this organisation will remain close to my heart forever. 

- ### Motivation: why this project?


As from the past 1 month I am contributing to dattashuttle repository and I am familiar with the codebase. I have past experience in working with Python and this project excites me as I will be able to learn and grow. 

Developing cross-platform packages with Textual interfaces presents a difficult but worthwhile process to increase my mastery of Python packaging approaches. The successful deployment of this implementation would help datashuttle users while establishing design criteria for Textual application interfaces across the entire Python environment.

- ### Match: why you?

I am currently pursuing my Bachelor of Technology degree in Information Technology branch from Dr. B.R. Ambedkar National Institute of Technology Jalandhar. In my 3rd year of undergrad, I served as a founder in building the product [ColdScribe](https://www.producthunt.com/products/coldscribe#coldscribe). Coldscribe is an AI tool which generates customised cold emails. It uses Nextjs, Django and AWS services. Moreover, I have built a [Next.js landing page template](https://theankushagarwal.gumroad.com/l/NextjsLandingPage) and sold it on Gumroad, showcasing my passion for technology and continuous learning. 

My technical skills enable me to execute this project successfully by combining them with my current work at the datashuttle repository.

1. Through my previous work I showed my ability to use the datashuttle codebase as I contributed to it.
2. My knowledge of Python includes programming with external APIs
3. I have obtained basic knowledge of packaging tools like Hatch, PyInstaller, Briefcase along with Github CI.

Additionally, I like to write detailed-oriented and well-documented code. I will thoroughly test my code before raising PR. I am punctual and will deliver my work on time. My undergrad knowledge will also be helpful. 

Apart from this, in the past, I have cleared JEE Mains examination and secured [98.75](https://drive.google.com/file/d/1CIgjOKSJvJNsuo1A_1i1n2a6zRfnDQwV/view?usp=sharing) percentile. It is considered one of the toughest logical examinations of India and around 1 million students appear for this examination. 

- **Availability**

I am fully available to commit approximately 30 hours per week or more (as per project requirement of 350 total hours ) to this project throughout the GSoC period. I have no other major commitments during this time. Moreover, I will be having summer break from my university (Dr. B.R. Ambedkar National Institute of Technology Jalandhar) and I will not be involved in any other work during this period.

## GSoC

- **GSoC Experience**

Google Summer of Code will deliver the following benefits to me:
1. To receive valuable mentorship and guidance from experienced developers.
2. The participation in this open source project will help me develop experience in building meaningful contributions to both real-world applications and open source systems.
3. Growth in my technical skills.
4. I will have the ability to establish myself as a future developer for the Neuroinformatics Unit organization.



- **Are you also applying to projects with other organisations in GSoC 2025?**

I am not applying to any other GSoC organisation. I have chosen Neuroinformatic Unit (datashuttle) because it combines with my skills perfectly and provides me with existing knowledge of the codebase due to earlier work.