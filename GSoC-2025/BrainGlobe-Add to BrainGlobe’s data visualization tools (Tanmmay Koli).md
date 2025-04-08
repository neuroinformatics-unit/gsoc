# BrainGlobe: Implementing Atlas-Registered Data Visualization in brainrender-napari (Tanmmay Koli)

## Personal details
- **Full name**: Tanmmay Koli  
- **Email**: tanmmaykoli@gmail.com  
- **GitHub username**: TanmmayKoli  
- **Zulip username**: Tanmmay Koli  
- **Location & time-zone**: Davis, California, US / GMT -7  
- **Personal website**: [www.linkedin.com/in/tanmmay-koli-068a992a6](https://www.linkedin.com/in/tanmmay-koli-068a992a6)  
- **Code contribution**: [PR #195](https://github.com/brainglobe/brainrender-napari/pull/195)  
- **Proposal discussion link**: [neuroinformatics-unit/gsoc#79](https://github.com/neuroinformatics-unit/gsoc/pull/79)  

## Project proposal

### Synopsis
The BrainGlobe brainrender tool is used to visualise brain data in a common coordinate space defined by a "brain atlas" (We refer to this data as "atlas-registered" data). However, brainrender is inaccessible to people without programming skills. The brainrender-napari tool aims to make brainrender functionality available to more people through a plugin for the popular open-source graphical image viewer napari. This project is supposed to expand on the functionality of the brainrender-napari tool by implementing code that will add a widget, designed in python, that allows users to download and visualise atlas-registered data from mouse and fish brains. This will make the brainrender-napari tool more accessible to neuroscience researchers and contribute to an expanded employment of advanced data technologies for neuroimagery research.

### Goals and Deliverables
**Core**:
- Develop a python plugin widget that will allow users to be able to download and visualize atlas-registered data, primarily from fish and mouse brains.
- Implement tests that will cover the expanded functionality
- Create clear documentation for the new functionality

**Stretch Goals (if there is additional time)**:
- Implement a side by side visualization of different atlases with 3d navigation, used to compare different species at once
- Add a tool to export and calculate different brain region metrics (volume, surface area, eg.)  

### Implementation timeline
**Duration**: Medium (~175 hours), 12 weeks  
**Weekly commitment**: ~15 hours, ~3 hours everyday 

| Week       | Hours | Tasks |
|------------|-------|-------|
| **Community Bonding & Research (May 8 - June 1)** | 30 | Complete "Visualize an atlas in napari" tutorial along with other tutorials of the Brainrender tool. Study existing brainrender widget code and different python libraries for implementation. Discuss schedule and project details more in depth with mentor. |
| **Week 1-2** | 30 | Design UI for widget using QtPy. Work on designing the outline and framework of the widget. |
| **Week 3-4** | 30 | Identify fish and mouse brain atlases datasets and set up data fetching, load sample data into napari from bg_atlasapi. Start process of programming the functionality of the widget on python. |
| **Week 5-6** | 30 | Build an interactive GUI and implement functionality with QtPy. Design and test the python implemented widget with visualization on BrainGlobe. Implement unit testing to ensure proper data handling and integrate with BrainGlobe's data API. |
| **Week 6-7** | 30 | Complete bulk of the initial coding process, continue testing and visualizing in BrainGlobe. Start documentation for widget code and functionality. Prepare for midterm project report documentation. |
| **Week 8-9** | 30 | Start implementing feedback from mentor and midterm report. Make any adjustment to the widget code if needed along with additional testing to ensure proper functionality. |
| **Week 10-12** | 30 | Finalize refinement and optimize the widget's performance. Prepare final report for documentation and showcase of widget functionality (If available time, implement stretch goals). |

## Communication plan
I will be active on Zulip to communicate with mentors, Alessandro Felder and Igor Tarnikov, and the rest of the community involved in NIU's projects. I will also be using zoom for online meetings and progress reports with my mentors and peers. I plan to push my changes onto the BrainGlobe brainrender-napari Github repo to receive feedback and track my development. I will also document and post weekly summaries for my development process so that I can receive feedback as well.

## Personal statement

### Past experience
I have been programming for 3 years now and I am in my second year of my Bachelor's degree in Computer Science at the University of California, Davis. I have pursued various levels of coding projects, in both python and C, and I am also a member of various tech-related clubs at UC Davis. I have worked on projects that range from a data loss prevention agent and data classification to brain computer interfaces (BCI) as part of my club at school and they have all exposed me to various different types of systems and programming features that have helped refine my skills. For the BCI project, specifically, I worked on developing a program in python that can read EEG data waves and use an algorithm to determine how confident a person is when they are studying and give it a score. For the BCI, we used OpenBCI EEG tech and developed a quiz system to repeat a series of questions based on the confidence score given to a user when they answer a question. The idea is that it is a live feedback loop that will update the questions each time until all the questions have been answered. It can also display the average confidence score at the end to show users how well the user is retaining the information of the quiz, helping them learn more effectively.

### Motivation: Why this project?
The reason why this specific project interests me the most is because I am deeply fascinated by visualization technologies, as part of my experience with OpenBCI software. EEG data always interested me ever since I started working with it as part of my club and BrainGlobe's software intrigued me a lot as it showed 2D and 3D models of different animal brains, which was quite exciting to play around with. Working on a widget that can actually contribute and affect BrainGlobe's software motivates me the most as it links pretty well to my own personal interests and professional as I gain a lot more crucial experience with python and can use that for future projects as well. I also envision that this can have a pretty positive impact for the open source community as researchers in neuroscience can find work like this very useful for their own work as the open source community can make it easier for them to conduct their research and help expand understanding of neuro anatomical data in different animals. It can also help with research into different human brains as well and deepen understanding of several neural phenomena.

### Match: Why you?
I believe I match quite well with this project as it pertains to my personal interests as well my professional and academic ones due in part to my experience with neuroscience and programming. My hands-on experience with neural data and my background in python should be the right technical fit for developing the widget. Although I haven't worked exactly with widget creation before, I believe my coding contribution for BrainGlobe and my previously mentioned projects should indicate my adaptiveness and willingness to learn new technologies in order to achieve my goal for any project. Plus, I am very willing to learn and collaborate with a community of neuroscience and programming enthusiasts such as myself.

### Availability
For availability, I should be available for most of the summer with the exception of the first two weeks as my school is on a quarterly system so that would mean that my final exams do end at around June 12th so, I was hoping to coordinate my mentor the beginning of week 1 a bit further than the start of June 1st in order to properly acclimate at the start of the project.

## GSoC

### GSoC experience
I intend to gain first hand experience on an open source for the first time and get more experience in building visualization tool technology. I also expect to gain more experience in real world software development through this program.

### Are you also applying to projects with other organisations in GSoC 2025?
No, I am only focusing on one project for the Neuroinformatics Unit in GSoC 2025 as it aligns with my interests in Neuroscience and computer science. I am focused only on this BrainGlobe project for now as I find it the most engaging and also the most friendly experience to expand my programming capabilities.
