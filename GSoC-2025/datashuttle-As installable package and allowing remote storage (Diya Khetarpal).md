# datashuttle: Allow Google Drive or AWS as remote storage and Deploy datashuttle as an installable package (Diya Khetarpal)

## Personal details
- **Full name:** Diya Khetarpal
- **Email:** diyakhetarpal@gmail.com
- **GitHub username:** [Diya910](https://github.com/Diya910)
- **Zulip username:** [Diya Khetarpal](https://neuroinformatics.zulipchat.com/#user/895220)
- **Location & time-zone:** New Delhi, India (UTC+5:30)
- **Personal website / project portfolio:** [Diya Khetarpal](https://www.linkedin.com/in/diya-khetarpal-b22a56249/)
- **Code contribution:**
    - I worked under Atulit to form a CLI command for [Xander Corp](https://github.com/Xander-AI-Main/xander-cli), a no-code AI solution which you can check out on [PyPI](https://pypi.org/project/xander-cli/).
    - Established a dedicated [Continuous Integration (CI)](https://github.com/sunpy/sunpy/pull/8010#) workflow for sunpy.coordinates (OpenAstronomy) to enhance testing efficiency.
    - [Implemented](https://github.com/sunpy/sunpy/pull/7953#issuecomment-2581136449) handling mechanisms for missing values to improve data robustness.
    - Adds support for ellipsis in [NDCube](https://github.com/sunpy/ndcube/pull/818) allowing users to slice objects using ellipsis.
- **Proposal discussion link:** [datashuttle installable package and remote storage feature](https://github.com/neuroinformatics-unit/gsoc/pull/73)

## Project proposal

### Synopsis
This project aims to enhance datashuttle in two significant ways: (1) extending its remote storage capabilities to include Google Drive and AWS S3, and (2) deploying it as a cross-platform installable package. These improvements will democratize access to standardized neuroscience data organization tools by removing technical barriers for researchers without programming expertise.

Cloud storage integration via RClone will allow researchers to securely transfer neuroinformatics data between local filesystems and popular cloud platforms with standardized structures and metadata validation. The cross-platform executable distribution will eliminate dependency on conda/Python expertise, making datashuttle accessible to a broader scientific community regardless of technical background.

The dual objectives of cloud storage integration and cross-platform packaging are achievable within the 350-hour period through strategic use of existing technologies: leveraging RClone's robust cloud connectors (rather than building from scratch) and using a modular development approach where components can be developed in parallel. The timeline is structured to allow cloud integration work in the first half of the program, with packaging work beginning while finalizing cloud features, ensuring efficient use of development time.

### Implementation timeline

**Minimal set of deliverables:**
1. Cloud storage integration (Google Drive & AWS S3) with authentication systems
2. Python API and Terminal UI extensions for cloud operations
3. Cross-platform executable distribution for Windows, macOS, and Linux
4. CI/CD pipeline for automated platform-specific builds
5. Comprehensive testing framework for cloud features and executables
6. Complete user and technical documentation

**Stretch goals:**
- Additional cloud provider support (Dropbox, Azure)
- Plugin architecture for community-contributed extensions(e.g., specialized storage connectors for institutional repositories, custom data validators for specific experiment types, visualization tools for tracking data transfer metrics)
- Integration with institutional storage systems
- Bandwidth optimization for large dataset transfers

**Weekly timeline:**

[Detailed project proposal with all planning and timelines](https://docs.google.com/document/d/1BdOF-X388s-LL3XlFQJfFreGWynCjuyFJ17EtcrzAe4/edit?usp=sharing)

| Week | Period | Deliverables | Hours/Week |
|------|--------|-------------|------------|
| Community Bonding | May 8 - Jun 1 | Set up dev environment, study RClone docs, research packaging technologies | 20 |
| 1 | Jun 2 - 8 | Analyze architecture, document integration points, create diagrams | 30 |
| 2 | Jun 9 - 15 | Implement OAuth 2.0 for Google Drive, AWS IAM auth for S3, secure credential storage | 30 |
| 3 | Jun 16 - 22 | Create CloudTransferManager base class, implement GoogleDriveConnector and AWSS3Connector | 30 |
| 4 | Jun 23 - 29 | Implement chunking for large uploads, transfer validation, resumable transfers | 30 |
| 5 | Jun 30 - Jul 6 | Design cloud config screens with Textual, create storage browser, implement progress indicators | 30 |
| 6 | Jul 7 - 13 | Evaluate packaging options (PyInstaller, cx_Freeze, Electron), research terminal emulation, create proofs-of-concept | 30 |
| 7 | Jul 19 - 25 | Test prototypes across platforms, document findings, select final approach | 30 |
| 8 | Jul 26 - Aug 1 | Create build configuration, implement entry points, develop modular build scripts | 30 |
| 9 | Aug 2 - 8 | Build platform-specific installers (Windows MSI, macOS DMG, Linux packages), configure code signing | 30 |
| 10 | Aug 9 - 15 | Set up GitHub Actions for multi-platform builds, create automated release process | 30 |
| 11 | Aug 16 - 24 | Develop unit and integration tests for cloud components, implement cross-platform testing | 30 |
| 12 | Aug 25 - Sep 1 | Complete documentation, perform final refinements, prepare submission | 30 |

### Communication plan
I plan to maintain regular communication with my mentor through:
- Weekly video calls for in-depth progress discussions and technical problem-solving
- Daily status updates via Zulip chat to maintain momentum
- GitHub PR reviews and issue discussions for code-specific collaboration
- Ad-hoc voice calls for urgent issues requiring immediate attention

I'm flexible with my schedule and can adjust my working hours (UTC 07:00-13:00 or UTC 15:00-19:30) to accommodate my mentor's availability.

## Personal statement

### Past experience
As a third-year Computer Science student at Maharaja Agrasen Institute of Technology, I've developed strong programming skills through academic coursework and hands-on projects. My open-source journey includes meaningful contributions to scientific Python packages:

- **SunPy**: Established CI workflows for sunpy.coordinates and implemented missing value handling
- **NDCube**: Added support for ellipsis syntax in coordinate-aware data arrays
- **OpenVINO**: Optimized mathematical equation calculations

My experience with ML systems deployment is demonstrated in the [Smart Warehouse project](https://wfp-smartwarehouse.in) for the World Food Programme during my research internship at [IIT Delhi](https://home.iitd.ac.in), where I built an intelligent surveillance system on NVIDIA Jetson devices using YOLOv8. This project required optimizing for resource-constrained environments—skills translatable to creating efficient cross-platform packages.

I was among the Top 6 finalists in the [Google Girl Hackathon 2025](https://github.com/Diya910/Google-girl-hackathon-2025/blob/main/README.md), driven by my determination to step outside my comfort zone. Despite coming from a Computer Science background, I embraced the challenge of exploring electronics and successfully reached the finals.

### Motivation: why this project?
Contributing to tools that solve real scientific challenges deeply motivates me, and datashuttle's mission to standardize neuroscience data organization addresses a critical barrier to collaboration and reproducibility. The opportunity to enhance this tool with cloud integrations and cross-platform executables directly aligns with my passion for building accessible, community-driven solutions.

By simplifying data transfers and eliminating dependency on programming expertise, this project empowers global researchers to focus on science rather than infrastructure. The technical challenges of integrating RClone, designing modular architectures, and solving cross-platform packaging problems excite me as learning opportunities with meaningful impact.

### Match: why you?
My background uniquely positions me for this project. My open-source experience provides insights into collaborative development processes, while my work with edge devices has taught me to build maintainable cross-platform solutions. My recent success as a finalist in Google Girl Hackathon '25 demonstrates my ability to develop innovative technical solutions under pressure.

My experience with cloud services (AWS deployment of [Xander CLI](https://pypi.org/project/xander-cli/)) and packaging terminal applications aligns perfectly with the project's goals. Most importantly, I'm driven by the mission to democratize research tools, making them accessible regardless of technical expertise.

### Availability
During the GSoC period, I'll be on summer break from university, allowing me to commit 30+ hours weekly to the project. I have no other professional commitments during this time and have planned my academic schedule to avoid conflicts.

## GSoC

### GSoC experience
From GSoC, I expect to gain valuable experience in open-source collaboration while making a tangible contribution to scientific research infrastructure. I look forward to:
- Technical growth through mentored feedback and code reviews
- Community engagement skills by interacting with diverse stakeholders
- Project management experience by delivering complex features on schedule
- Long-term contribution opportunities beyond the summer program

Working on datashuttle would provide me with insights into real scientific workflows and the challenges researchers face, helping me better understand how technology can accelerate discovery.

### Are you also applying to projects with other organisations in GSoC 2025?
I am also applying to OpenAstronomy. My preference would be datashuttle due to its direct impact on research workflows and the unique combination of cloud integration and cross-platform packaging challenges, which align perfectly with my skill set I gained at xander.