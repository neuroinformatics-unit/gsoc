- **Full name:** Pranav Kapoor  
- **Email:** pranav33317@gmail.com  
- **GitHub username:** pranav33317  
- **Zulip username:** Pranav Kapoor  
- **Location & time-zone:** New Delhi, India (IST, GMT+5:30)  
- **Personal website / project portfolio:** [github.com/pranav33317](https://github.com/pranav33317)  
- **Code contribution:**  
  - PR: [Disable parallel mesh creation (PR #546)](https://github.com/brainglobe/brainglobe-atlasapi/pull/546#pullrequestreview-2729541724)  
    (I worked on disabling parallel mesh creation in various files while addressing [Issue #429](https://github.com/brainglobe/brainglobe-atlasapi/issues/429).)  
- **Proposal discussion link:**  
  - [Proposal Discussion (PR #554)](https://github.com/brainglobe/brainglobe-atlasapi/pull/554)  
    (This closed PR includes a new file containing the wrapper function to convert atlas data to an OpenSANDS object and return its file path.)

---

## Project proposal

### Synopsis
The BrainGlobe brainrender tool is a widely used resource for visualizing brain data within a common coordinate framework defined by a “brain atlas.” However, its command-line interface makes it inaccessible to many researchers who lack programming expertise. The brainrender‑napari tool seeks to change this by bringing brainrender’s powerful visualization capabilities into napari—a popular open-source graphical image viewer.

Despite the overlap in functionality between brainrender and brainrender‑napari, certain publicly available atlas‑registered datasets, particularly those from mouse and fish brains, remain unsupported in the napari version. This project will implement code to enable users to seamlessly download and visualize atlas‑registered data from these species via a dedicated napari widget. By making brainrender functionality more accessible, this project will help democratize neuroinformatics research and foster greater collaboration within the open source community.

**Project Goals & Deliverables:**
- **Minimal Deliverables:**
  - Develop a Python napari widget that enables users to download and visualize atlas‑registered data from mouse and fish brains.
  - Implement comprehensive tests covering all new functionality.
  - Create clear and concise documentation for the new features.
- **Stretch Goals (if time permits):**
  - Extend support for additional species or imaging modalities.
  - Integrate schema validation using tools like `jsonschema` to ensure compliance with data standards.
  - Develop a conversion utility to update existing atlas packages to the new standard.

### Implementation timeline

I plan to commit 30–35 hours per week toward this project. Below is my detailed 12‑week timeline:

| **Week** | **Tasks & Deliverables**                                                                                                                                                                                                                                         | **Hours** |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 1–2      | **Community Bonding & Research:**<br>- Deeply explore the BrainGlobe brainrender and brainrender‑napari codebases.<br>- Study publicly available atlas‑registered data for mouse and fish brains.<br>- Engage with mentors and set up a focused development environment.      | 30        |
| 3–4      | **Design & Planning:**<br>- Map the current atlas data to a format suitable for brainrender‑napari.<br>- Design a modular napari widget with wireframes for the download and visualization workflow.<br>- Outline minimal deliverables and document initial design decisions.                                      | 30        |
| 5–6      | **Core Development – Part 1:**<br>- Implement the new widget and its supporting data download module.<br>- Integrate basic visualization capabilities using brainrender functions within napari.<br>- Adapt the Allen Human atlas packaging script to test the new workflow.                         | 30        |
| 7–8      | **Core Development – Part 2:**<br>- Enhance error handling, refine data mapping, and add initial unit tests.<br>- Begin writing documentation and gather early feedback from mentors and the community.                                  | 30        |
| 9–10     | **Testing & Feedback:**<br>- Develop comprehensive tests to validate the functionality of the widget.<br>- Incorporate mentor and community feedback to refine the user interface and code.<br>- Ensure smooth integration with existing BrainGlobe tools.                                                  | 30        |
| 11–12    | **Finalization:**<br>- Polish the code and complete documentation.<br>- Finalize all tests and prepare a final demonstration video of the widget in action.<br>- Reserve extra time to resolve any unforeseen issues and ensure a robust deliverable.                                            | 30        |

### Communication plan
I will keep open communication with my mentors through daily updates on Zulip and hold weekly video calls for deeper discussions on progress and challenges. I will also post regular updates on GitHub issues and pull requests to ensure complete transparency and prompt feedback throughout the project.

---

## Personal statement

### Past experience
I am a third-year undergraduate at IIIT Delhi with a strong passion for programming and neuroscience. My journey began when I learned Python, networking, and SQL in high school, and I built projects like a simple password manager early on. Over the years, I have completed several significant neuroscience assignments that involved processing and visualizing complex experimental data. For example, I created raster and peri-stimulus time plots to analyze neuronal activity, statistically analyzed behavioral data from decision-making experiments, and generated detailed figures to illustrate experimental findings. These projects have given me a robust foundation in handling neurophysiological data. Additionally, my coursework in data structures, operating systems, and embedded systems has taught me to approach problems methodically and collaborate effectively. While I have not yet worked professionally with widget implementation or advanced image processing, my academic projects have prepared me well to tackle new challenges. I am excited about the opportunity to contribute to the BrainGlobe brainrender‑napari project and bring my passion for accessible neuroinformatics to a wider audience.

### Motivation: Why This Project?
The intersection of neuroscience and open source deeply intrests ,e. I have seen firsthand how diverse and incompatible data formats can hinder scientific progress during a neuroscience course with Prof. Mrinmoy Chakroborty. This project excites me because it directly addresses these challenges by enhancing the interoperability of neuroanatomical data through a user-friendly napari widget. By enabling researchers to easily download and visualize atlas‑registered data from mouse and fish brains, we can remove significant technical barriers and accelerate research. I am driven by the chance to create a tool that makes complex data more accessible, thereby empowering a global community of scientists to collaborate more effectively.

### Match: Why You?
I believe I am uniquely positioned for this project due to my solid programming background and my deep interest in neuroscience. My experiences—from learning Python in high school and college to executing detailed neuroscience assignments at IIIT Delhi—have equipped me with the practical skills necessary to develop robust data analysis and visualization tools. Although I haven’t directly worked with widget developmeny or advanced image processing in a professional setting, my hands-on projects have given me a strong understanding of neurophysiological data. My commitment, motivation and my eagerness to learn new technologies make me a suitable  candidate for the project.

### Availability
I have a flexible schedule during the GSoC period with no conflicting commitments. I am currently attending IIIT Delhi and have a low course load this semester, allowing me ample time to contribute meaningfully to the project. I can reliably dedicate approximately 15 hours per week, with additional hours on weekends if needed, ensuring steady progress throughout the program.

---

## GSoC

### GSoC experience
I view GSoC as a transformative opportunity to work closely with experienced open source developers and to enhance my technical expertise through real-world project work. I expect to gain invaluable insights into best practices for scientific software development, refine my collaborative skills, and contribute significantly to a project that impacts neuroinformatics research. This experience will help me build lasting connections in the open source community while advancing my technical skills.

### Are you also applying to projects with other organisations in GSoC 2025?
I am focusing solely on this project with BrainGlobe for GSoC 2025, as it aligns perfectly with my interests and professional goals. This project is my top priority, and I am fully committed to its success.
