## Project Title
## movement: Web-based Graphical User Interface for Pose Filtering and Trajectory Analysis (Priyam Raj)

---

## Personal Details
- **Full Name**: Priyam Raj
- **Email**: rajpriyam27@gmail.com
- **GitHub username**: [Priyam12345-cloud](https://github.com/Priyam12345-cloud)
- **Zulip username**: Priyam Raj
- **Location**: Mumbai, Indian Standard Time (GMT+5:30)  
- **Portfolio**: [Portfolio](https://priyam12345-cloud.github.io/Devcom-developers/)
- **Code Contributions**:
  - [PR: Test scene from sample data #543](https://github.com/neuroinformatics-unit/movement/pull/543#issuecomment-2781009563)
- **Proposal Discussion**:
  - [Discussion PR](https://github.com/neuroinformatics-unit/gsoc/pull/77)

---

## Project Proposal

### Synopsis
This project aims to build a modern, web-based GUI for the `movement` package, allowing users to visually explore and filter pose trajectories and export results. Current usage relies on scripts or notebooks. A web interface—via Dash, Streamlit, or React+D3—will open `movement` to a broader audience, including non-programmers in neuroscience and biomechanics.

**Community Benefit**: A browser-based GUI will make movement more approachable for a broader audience, including students and researchers in neuroscience and biomechanics. It aligns with the project’s vision of usability and lowers the barrier to entry for pose analysis.

---

### Implementation Timeline

#### Minimal Set of Deliverables
- **Interactive Trajectory Viewer** - Build an intuitive interface to visualize keypoint trajectories over time, with zoom, pan, and playback controls.
- **File Loader & Video Sync** - Load pose estimation data and synchronize it with video playback, overlaying trajectories frame-accurately.
- **Live Filter Tuning** - Integrate Kalman and particle filters with sliders or input fields to tune parameters in real time.
- **Batch Processing Interface** - Support filtering and analyzing multiple sessions in one go, with options to manage large datasets easily.
- **Export & Sharing Tools** - Enable users to export processed results as videos, plots, or structured files (like CSV), ready for sharing or downstream analysis.

#### Stretch Goals *(If Time Permits)*

- **Authentication & Session Storage** - Add user login and the ability to save filter settings and sessions.
- **Side-by-Side Filter Comparison** - Allow parallel comparison of different filtering strategies on the same trajectory.
- **Cloud Dataset Integration** - Connect with platforms like Google Drive or AWS S3 to load/save data from the cloud.
- **Real-Time Streaming Support** - Visualize trajectories live from incoming pose estimation streams via WebSockets or REST APIs.


### Google Summer of Code 2025 – Weekly Timeline

| Week & Dates                        | Hours/week | Tasks and Deliverables |
|------------------------------------|------------|-------------------------|
| **Community Bonding (May 8 – June 1)** | 10         | • Explore relevant napari plugins and collaborate with mentors to define the project scope and milestones  <br> • Finalize the overall technology stack, UI wireframes, and system architecture for the tool |
| **Week 1 (June 2 – June 8)**       | 20         | • Implement the file upload module for user data (JSON/CSV formats) <br> • Develop the basic trajectory plotting component using napari viewer <br> • Integrate basic zoom and pan functionality for trajectory inspection |
| **Week 2 (June 9 – June 15)**      | 20         | • Design and build the trajectory filtering interface (e.g., by subject, body part, or confidence threshold) <br> • Connect filtering parameters to backend logic for real-time updates <br> • Modularize codebase for scalability |
| **Week 3 (June 16 – June 22)**     | 18         | • Integrate interactive controls for parameter tuning with live plot refresh <br> • Introduce color-coded visualization based on uncertainty levels <br> • Refine UI responsiveness and state management |
| **Week 4 (June 23 – June 29)**     | 20         | • Develop video overlay system to superimpose pose trajectories over frames <br> • Synchronize pose playback with video timeline controls <br> • Add seek, pause, and frame-by-frame navigation support |
| **Week 5 (June 30 – July 6)**      | 20         | • Implement batch processing support for multiple datasets <br> • Enable export of filtered trajectories in user-defined formats (CSV/JSON) <br> • Ensure metadata preservation during export |
| **Week 6 (July 7 – July 13)**      | 20         | • Finalize the core pipeline: data upload → filter → visualize → playback → export <br> • Conduct code cleanup and add docstrings/comments <br> • Prepare and submit midterm deliverables and documentation |
| **Midterm Evaluation (July 14 – July 18)** | —          | • Submit midterm evaluation form and mentor feedback <br> • Present a working demo showcasing key features and progress so far |
| **Week 7 (July 14 – July 20)**     | 18         | • Add session management features: configuration save/load, state function <br> • Introduce support for selecting and comparing multiple tracked subjects <br> • Begin handling edge cases in user inputs |
| **Week 8 (July 21 – July 27)**     | 20         | • Develop reporting tools for exporting summaries (CSV, PDF) with trajectory statistics <br> • Add ability to capture and export annotated screenshots of visualizations ensuring compatibility with major OS and browsers |
| **Week 9 (July 28 – August 3)**    | 20         | • Enhance timeline controls: zoom in/out, play speed adjustment, and hover tooltips <br> • Optimize large dataset performance and improve rendering speed <br> • Conduct end-to-end tests with real sample data |
| **Week 10 (August 4 – August 10)** | 15         | • Polish overall UI/UX: design consistency, add animations, improve layout <br> • Improve accessibility (keyboard navigation, alt-texts) <br> • Fix minor bugs from community testing feedback |
| **Week 11 (August 11 – August 17)**| 12         | • Finalize all documentation (developer guide, user manual, setup instruction) <br> • Conduct usability testing sessions with sample users <br> • Prepare feedback form and implement last-minute improvements |
| **Week 12 (August 18 – August 25)**| 10         | • Submit all final deliverables and evaluation <br> • Publish project blog post summarizing contributions, and future scope |
| **Post-GSoC (August 26 onwards)** | —          | • Continue refining features and performance <br> • Engage with the community and contribute to issue tracking, documentation, and future roadmap |


## Communication Plan
- **Primary Channel**: Zulip (daily async updates)
- **Weekly Meetings**: Zoom call
- **Task Tracking**: GitHub Issues and PRs
---

## Personal Statement

### Past Experience
I'm an undergraduate at IIT Bombay with a strong background in Artificial Intelligence, data science, and full-stack web development. My technical work spans contributions to both open-source and industry-focused projects, including working with Code for GovTech (C4GT) on the Open Network for Digital Commerce, where I am developing a Magento adaptor to facilitate seamless seller onboarding. I’ve built AI-powered tools at CleverNav, such as a voice-to-text and translation module, and led full-stack development for open-source platforms like the Seasons of Code portal under the Web and Coding Club, which supports 150+ projects. My prior work also includes machine learning-based financial models, geospatial analysis using QGIS, and robust UI/UX-driven mobile apps built with Flutter.As a core member of the Web and Coding Club (WnCC) at IIT Bombay, I’ve led workshops and mentored peers in web development, data visualization, and open-source culture.I’ve already started contributing to movement, am familiar with its structure, and am excited to scale my impact in this ecosystem.

### Motivation
This project aligns deeply with my dual passion for scientific computing and intuitive design. I believe good interfaces are critical in democratizing access to powerful tools—especially in domains like movement science, data visualization, or infrastructure systems. I’m drawn to projects that blend backend logic with frontend usability, and I see this as a unique opportunity to contribute something that is both technically robust and widely impactful. 

### Why Me?
I bring a strong blend of technical and user-focused experience—ranging from Python, Dash, and React to data tools like NumPy and pandas. I’ve built intuitive UIs for real-world users, contributed to movement, and worked on data-driven visual systems that prioritize accessibility. My understanding of pose analysis workflows and filtering methods (like Kalman/SavGol) allows me to bridge backend logic with frontend clarity. My experience building platforms for education, civic infrastructure, and analytics equips me with the understanding needed to contribute meaningfully.

### Availability
I’ll be on a 3-month summer break after my end-semester exams in April, with no academic or internship commitments. I’ll be able to focus fully on GSoC and scale efforts as needed for evaluations and communicate proactively.

---

## GSoC Details

### GSoC Experience
I see GSoC as an opportunity to contribute meaningfully to open-source and work closely with mentors on impactful projects. This proposal balances scientific relevance with practical usability, and I'm eager to build something that truly helps the community.

### Other Applications
I'm applying solely to the Neuroinformatics Unit for GSoC 2025. This project is my top and only choice. I am genuinely interested in contributing to this project's goals and see strong alignment with my skills and long-term interests.
