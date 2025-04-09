# DataShuttle: Cross-platform Executable Package (Aakash Kharb)

## Personal Details

- **Full name**: Aakash Kharb
- **Email**: [akharbrtk2@gmail.com](mailto:akharbrtk2@gmail.com)
- **GitHub username**: aakash-test7
- **Zulip username**: Aakash Kharb
- **Linkedin**: [https://linkedin.com/in/aakash-kharb/](https://linkedin.com/in/aakash-kharb/)
- **Location & Time-zone**: India, Indian Standard Time (GMT+5:30)

## Code Contribution

- [https://github.com/neuroinformatics-unit/datashuttle/pull/473](https://github.com/neuroinformatics-unit/datashuttle/pull/473)
- [https://github.com/neuroinformatics-unit/datashuttle/pull/471](https://github.com/neuroinformatics-unit/datashuttle/pull/471)

## Project Proposal

### Synopsis

DataShuttle currently requires Conda for installation, which limits accessibility for non-technical users. This project aims to create a standalone, cross-platform executable package for DataShuttle that works on Windows, macOS, and Linux. This project will:

- 1. Package DataShuttle as a standalone, cross-platform executable (Windows, macOS, Linux) without Conda/Python, prioritizing CLI/headless compatibility.
- 2. Solve Textual’s terminal rendering issues by:
  - Bundling a lightweight terminal (e.g., wezterm) only for GUI systems.
  - Providing a fallback mode for headless environments (e.g., basic TTY output or Web-based rendering).
- 3. Ensure robust deployment via pip-installable wheels + self-contained binaries for flexibility.

## Key Challenges
- Terminal rendering
- Cross-platform support
- Minimal dependencies

### Deliverables

-  **Research Report**
  - - Comparison of packaging tools (PyInstaller, PyOxidizer, Nuitka, Briefcase) with pros/cons for CLI vs. GUI.
  - - Evaluation of Textual rendering fallbacks (e.g., --headless mode, WebRender).
  
-  **Implemented Solution**
  - - Primary: Statically linked binaries (CLI-first) for all platforms.
  - - Optional GUI: Bundled terminal (disabled by default in headless mode).
  - - pip support: Installable via `pip install datashuttle`.
  
-  **CI/CD Integration**
  - - Automated builds for native binaries (Windows .exe, Linux .AppImage, macOS .app).
  - - HPC testing: Verify compatibility on SSH-only environments.
  
-  **Documentation**
  - - Proper detailed writings.
  - - Entry and endpoints marked, along with some creative visualisations.
  
-  **Testing Framework**
  - - Headless testing: I'll setup in a virtual machine instance. 
  - - GUI testting: A display environment , I have a Mac.
  - - Performance tests: Time, memory

### Implementation Timeline

| Period          | Tasks                                                         | Hours/Week |
|-----------------|---------------------------------------------------------------|------------|
| Community Bonding | Familiarize with codebase, setup dev environment, finalize research plan | 25         |
| Week 1-2        | Research packaging solutions (PyInstaller, PyOxidizer, Briefcase), evaluate approaches | 35         |
| Week 3-5        | Prototype selected solution, address terminal rendering issues | 40         |
| Week 6-7        | CI/CD for multi-platform builds + headless testing            | 40         |
| Week 8          | pip wheel support, minor testing, analysis                    | 35         |
| Week 9-10       | Comprehensive testing across platforms                        | 35         |
| Week 11-12      | Documentation, final polishing, mentor review                 | 35         |

Total time = 25 + 180 = 205

### Stretch Goals

- Implement auto-update functionality
- Create GUI installer for each platform
- Optimize package size and performance

### Communication Plan

- Weekly video calls with mentor for progress updates
- Daily stand-ups via Zulip chat
- Regular updates via GitHub PRs/issues
- Immediate communication for blockers via Zulip/email

## Personal Statement
"There's no value in lies. I know how to work and I am passionate about it. At night, sleep becomes easy, especially when I see something I've created."

### Past Experience

With 3 years of Python experience, I've worked on:

- Full-stack applications (chickpea7.streamlit.app, aakash-dbms.streamlit.app)
- Terminal applications (aakash-terminal.vercel.app)
- Machine learning and data science workflows
- Backend system design and implementation

### Motivation

I'm passionate about making technical tools more accessible. DataShuttle solves important problems in neuroinformatics, but its current installation process creates unnecessary barriers. This project aligns perfectly with my interest in developer tools and user experience.

### Why Me?

- Strong Python fundamentals and problem-solving skills
- Experience with cross-platform development challenges
- Quick learner with ability to dive into new technical areas
- Passion for creating polished end-user experiences

### Availability

- No other commitments during GSoC period
- Available 35-40+ hours per week
- No planned vacations during program

## GSoC Expectations

I hope to:

- Contribute meaningfully to open-source neuroscience tools
- Deepen my understanding of Python packaging and distribution
- Learn from experienced mentors in the field
- Build connections within the neuroinformatics community

## Other Applications

Currently only applying to NIU for GSoC 2025. Fully committed to this project.
