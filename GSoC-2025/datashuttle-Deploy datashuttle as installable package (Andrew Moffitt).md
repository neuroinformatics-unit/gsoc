# datashuttle-Deploy datashuttle as installable package (Andrew Moffitt)

## Personal details
Please include the following information:
- **Full name** Andrew Moffitt
- **Email** moffittandrew@outlook.com
- **GitHub username** MoffittAndrew
- **Zulip username** Andrew Moffitt (User ID: 890214)
- **Portfolio** https://www.linkedin.com/in/andrew-moffitt/
- **Location & time-zone** Edinburgh, UK (BST, UTC +01:00)
- **Code contribution**

    [Add docstring linting (#493)](https://github.com/neuroinformatics-unit/datashuttle/pull/493): Addressing issues [#369](https://github.com/neuroinformatics-unit/datashuttle/issues/369) and [#483](https://github.com/neuroinformatics-unit/datashuttle/issues/483), enforcing linting rules on docstrings and editing/adding docstrings to comply with the rules.

- **Proposal discussion link**

    TODO

## Project proposal

- **Synopsis**

    The process for installing and using datashuttle is more complicated than it needs to be, requiring conda to be installed and then set up to be done through the command line. This project will package datashuttle into a cross-platform executable that can be installed, setup and run easily by users on without deep computing experience.

- **Implementation timeline**

    1. **Deliverables**:
        - Research different packaging tools
        - Research different approaches to packaging a TUI -will research how [textualitty](https://github.com/lllama/textualitty/tree/main/src/textualitty) packages textual, and whether this approach could be expanded to work cross-platform, and will research different approaches to deploying a terminal as part of a python package.
        - Produce a report with the findings, analyzing each tool and approach, highlighting pros/cons, robustness and maintainability, and identifying what approach will be best suited for datashuttle.
        - Produce a proof-of-concept executable using the identified approach
        - Fine-tune the process of packaging datashuttle, ensuring this process works cross-platform
        - Automate this process through GitHub CI
        - Test the solution rigorously to ensure that the packaged executable does not create any additional bugs
        - Create documentation on the packaging process, as well as updating installation instructions for users.

    2. **Timeline** (35 hours per week):
        - Community Bonding Period: Initial research, discussing findings with mentor and community, start writing report
        - Weeks 1 & 2: Finalize report, develop proof of concept
        - Weeks 3 & 4: Fine tune packaging process for Linux, extend this process for Windows and MacOS
        - Week 5: Unavailable (See Availability section)
        - Weeks 6 & 7: Automate the packaging process
        - Weeks 8 & 9: Test the executable rigorously for each platform
        - Week 10: Unavailable (See Availability section)
        - Weeks 11 & 12: Create documentation and fix any remaining bugs
        - Week 13: Submit final product

- **Communication plan**

    I expect to have some kind of active direct message channel with my mentor (for asking for help when needed, sharing short progress updates whenever something is accomplished or seeking review/feedback on a piece of work), and a weekly stand-up meeting (through a video call platform which allows screen sharing, as this will likely be useful) to go over progress over the past week and to plan next steps, ensuring that I am staying on track. I am also flexible to more/less communication, and through different means if that works best for the mentor.

## Personal statement

- **Past experience.** 

    I have been working with Python for 6 years through schoolwork, university work and personal projects. For some of these projects, I have also utilized PyInstaller and Nuitka to package the code into an executable. Although I do not have experience specifically working on open source projects, I have spent the past year working for the University of Edinburgh, in which I contribute code to a repository alongside a team of Software Engineers, including testing and documentation of the code.

- **Motivation: why this project?**

    I have a particular interest in the field of Cognitive Science and Neuroscience, so this organization immediately caught my attention. I am interested in this project as I believe I have the skills and experience to do an excellent job.

- **Match: why you?**

    Most notably, I secured an internship after my first year of university, in which I was assigned a project and worked independantly to research approaches, code, test and document a solution, whilst regularly communicating and seeking advice and support from a supervisor, which is very similar to what this project requires. I excelled at this job and was hired back to continue work part-time, which demonstrates I am equipped to handle this project and complete it to a high standard. I am also very familiar with working on both Windows and Linux machines, which will prove to be valuable when it comes to debugging and ensuring support across operating systems. I believe these experiences make me an ideal candidate for this project.

- **Availability**

    I have exams until the 23rd of May, however I will still be free to participate during the community bonding period (but unable to commit large portions of my time). I will be unavailable during the week beginning 30th June, and the week beginning 4th August, leaving 10 weeks during the standard coding period in which I can work 35 hours a week to allow enough time to complete the project. I will also be unavailable during the week beginning the 1st September - this is after the standard coding period ends, but will have an impact if the time to complete the project is extended. Other than the weeks listed above, I will have no other commitments during the coding period.

## GSoC

- **GSoC experience**

    From this program, I am hoping to gain valuable experience working on an open source project with the support of a mentor who has in-depth knowledge and experience in the world of open source.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am not applying to any other projects.