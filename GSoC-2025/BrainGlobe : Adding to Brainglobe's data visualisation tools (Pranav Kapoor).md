- **Full name:** Pranav Kapoor  
- **Email:** pranav33317@gmail.com  
- **GitHub username:** pranav33317  
- **Zulip username:** Pranav Kapoor  
- **Location & time-zone:** New Delhi, India (IST, GMT+5:30)  
- **Personal website / project portfolio:** [github.com/pranav33317](https://github.com/pranav33317)  
- **Code contribution:**  
  - PR: [Disable parallel mesh creation (PR #546)](https://github.com/brainglobe/brainglobe-atlasapi/pull/546#pullrequestreview-2729541724)  
    (I worked on disabling parallel mesh creation in various files and am currently addressing [Issue #429](https://github.com/brainglobe/brainglobe-atlasapi/issues/429).)  
- **Proposal discussion link:**  
  - [Proposal Discussion ](https://github.com/neuroinformatics-unit/gsoc/pull/62) 

---

## Project proposal

### Synopsis
The BrainGlobe brainrender tool is a widely used resource for visualizing brain data within a common coordinate framework defined by a “brain atlas.” However, its command-line interface makes it inaccessible to many researchers who lack programming expertise. Currently, brainrender-napari lacks direct support for visualizing atlas-registered datasets from mouse and zebrafish brains, hindering broader adoption. This project will develop a dedicated napari widget to overcome this limitation.This will involve: 
1) Developing a napari widget with a user interface for browsing and selecting publicly available mouse and zebrafish datasets from sources like the Allen Brain Atlas.This will necessitate handling API interactions or direct data downloads.
2) Implementing data handling modules to parse and transform the downloaded data into formats compatible with brainrender's visualization pipeline (e.g., handling different file formats and coordinate systems). 
3) Integrating brainrender functions within the widget's backend to render the processed data within the napari canvas, ensuring correct spatial alignment with the corresponding brain atlas. 
4) Creating comprehensive unit and integration tests to validate the widget's functionality, data handling, and brainrender integration. 
5) Providing clear documentation for users on how to install and use the new widget. This implementation will empower researchers without coding expertise to seamlessly visualize critical mouse and zebrafish brain data within napari, democratizing access to brainrender's powerful visualization capabilities.

**Project Goals & Deliverables:**
- **Minimal Deliverables:**
  - Develop a Python napari widget: This will involve using napari's plugin API (napari.Viewer, magicgui) to create a user interface with elements for:
    - Dataset Browsing: Displaying a list of available mouse and zebrafish datasets fetched from relevant APIs (e.g., Allen Mouse Atlas API using requests library) or accessible via direct download URLs. 
    - This might involve parsing JSON responses or HTML.
    - Dataset Selection: Allowing users to select datasets for download.
    - Visualization Trigger: A button to initiate the visualization process.
  - Implement data handling modules: These Python modules will be responsible for:
    - Data Parsing: Reading and interpreting the downloaded data files (which may be in formats like NIfTI, CSV, or    custom formats). This will involve using libraries like nibabel for neuroimaging data and pandas for tabular data.
    - Data Transformation: Converting the parsed data into a format that brainrender can directly utilize for visualization (e.g., creating brainrender.actors like Volume, Points, Mesh). This will require understanding brainrender's API and data input requirements.
  - Integrate brainrender visualization: Within the widget's backend, utilize brainrender functions to create and add actors to the napari.Viewer instance, displaying the downloaded and transformed data in 3D. This will involve instantiating brainrender.Scene and adding actors with appropriate parameters (e.g., color).
  - Implement comprehensive tests using pytest
  - Create clear and concise documentation
  - Create clear and concise documentation for the new features.
- **Stretch Goals (if time permits):**
  - Extend support for visualizing additional data modalities associated with the atlas-registered data (e.g., cell segmentations)  if possible
  - Enhance UI with advanced filtering and search: Implement UI elements (e.g., dropdown menus, search bars) to allow users to filter datasets based on metadata.We can use pandas to filter metadata.
  - Implement caching mechanisms for downloaded data to improve performance and reduce redundant downloads.

### Implementation timeline

I plan to commit 30–35 hours per week toward this project. Below is my detailed 12‑week timeline:

| **Week** | **Tasks & Deliverables**                                                                                                                                                                                                                                         | **Hours** |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 1–2      | **Community Bonding & Research:**<br>- Deeply explore the BrainGlobe brainrender and brainrender‑napari codebases.<br>- Study publicly available atlas‑registered data for mouse and fish brains.<br>- Engage with mentors and set up a focused development environment.      | 30        |
| 3–4      | **Design & Planning:**<br>- Map the current atlas data to a format suitable for brainrender‑napari.<br>- Design a modular napari widget with wireframes for the download and visualization workflow.<br>- Outline minimal deliverables and document initial design decisions.                                      | 30        |
| 5–6  (Summer Break)     | **Core Development – Part 1:**<br>- Implement the new widget and its supporting data download module.<br>- Integrate basic visualization capabilities using brainrender functions within napari.<br>- Adapt the Allen Human atlas packaging script to test the new workflow.                         | 35-40        |
| 7–8   (Summer Break)   | **Core Development – Part 2:**<br>- Enhance error handling, refine data mapping, and add initial unit tests.<br>- Begin writing documentation and gather early feedback from mentors and the community.                                  | 35-40        |
| 9–10     | **Testing & Feedback:**<br>- Develop comprehensive tests to validate the functionality of the widget.<br>- Incorporate mentor and community feedback to refine the user interface and code.<br>- Ensure smooth integration with existing BrainGlobe tools.                                                  | 30        |
| 11–12    | **Finalization:**<br>- Polish the code and complete documentation.<br>- Finalize all tests and prepare a final demonstration video of the widget in action.<br>- Reserve extra time to resolve any unforeseen issues and ensure a robust deliverable.                                            | 30        |

### Communication plan
I will keep open communication with my mentors through daily updates on Zulip and hold weekly video calls for deeper discussions on progress and challenges. I will also post regular updates on GitHub issues and pull requests to ensure complete transparency and prompt feedback throughout the project.

---

## Personal statement

### Past experience
I am a third-year undergraduate at IIIT Delhi with a strong passion for programming and neuroscience. My journey began when I learned Python, networking, and SQL in high school, and I built projects like a simple password manager early on. Over the years, I have completed several significant neuroscience projects that involved processing and visualizing complex experimental data. For example, I created raster and peri-stimulus time plots to analyze neuronal activity, statistically analyzed behavioral data from decision-making experiments, and generated detailed figures to illustrate experimental findings. These projects have given me a robust foundation in handling neurophysiological data. Additionally, my coursework in data structures, operating systems,algorithms and embedded systems has taught me to approach problems methodically and collaborate effectively. While I have not yet worked professionally with widget implementation or advanced image processing, my academic projects have prepared me well to tackle new challenges. I am excited about the opportunity to contribute to the BrainGlobe brainrender‑napari project and bring my passion for accessible neuroinformatics to a wider audience.

### Motivation: Why This Project?
The intersection of neuroscience and open source deeply intrests me. I have seen firsthand how diverse and incompatible data formats can hinder scientific progress during a neuroscience course with Prof. Mrinmoy Chakroborty. This project excites me because it directly addresses these challenges by enhancing the interoperability of neuroanatomical data through a user-friendly napari widget. By enabling researchers to easily download and visualize atlas‑registered data from mouse and fish brains, we can remove significant technical barriers and accelerate research.

### Match: Why You?
I believe I am uniquely positioned for this project due to my solid programming background and my interest in neuroscience. My experiences—from learning Python in high school and college to doing neuroscience projects at IIIT Delhi—have equipped me with the practical skills necessary to develop robust data analysis and visualization tools. Although I haven’t directly worked with widget development or advanced image processing in a professional setting, my hands-on projects have given me a strong understanding of neurophysiological data. My commitment, motivation and my eagerness to learn new technologies make me a suitable  candidate for the project.

### Availability
I  have a flexible schedule with no conflicting commitments during the GSoC period. I am currently attending IIIT Delhi with a low course load this semester, which will allow me ample time to contribute meaningfully to the project.I have my summer break starting from June where I can dedicate even more time (40-45 hours) if needed. I can reliably dedicate approximately 30-35 hours per week to this project, with additional time available on weekends if needed. I plan to integrate my work seamlessly with my academic and personal responsibilities, ensuring consistent progress throughout the program.

---

## GSoC

### GSoC experience
I view GSoC as a transformative opportunity to work closely with experienced open source developers and to enhance my technical expertise through real-world project work. I expect to gain invaluable insights into best practices for scientific software development, refine my collaborative skills, and contribute significantly to a project that impacts neuroinformatics research. This experience will help me build lasting connections in the open source community while advancing my technical skills.

### Are you also applying to projects with other organisations in GSoC 2025?
While I have also applied to Fedora, BrainGlobe is my organization of choice for GSoC 2025. My strong interest in neuroscience and scientific programming makes this project my primary focus. I am fully committed to dedicating my efforts to this project and ensuring its successful completion.
