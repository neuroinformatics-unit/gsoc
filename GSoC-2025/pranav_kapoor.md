## Personal details
- **Full name:** Pranav Kapoor  
- **Email:** pranav33317@gmail.com  
- **GitHub username:** pranav33317  
- **Zulip username:** Pranav Kapoor  
- **Location & time-zone:** New Delhi, India (IST, GMT+5:30)  
- **Personal website / project portfolio:** [www.github.com/pranav33317](https://www.github.com/pranav33317)  
- **Code contribution:**  
  - PR: [https://github.com/brainglobe/brainglobe-atlasapi/pull/546#pullrequestreview-2729541724](https://github.com/brainglobe/brainglobe-atlasapi/pull/546#pullrequestreview-2729541724)  
    I tried to disable parallel mesh creation in various files to simplify mesh creation while simultaneously working on [Issue #429](https://github.com/brainglobe/brainglobeatlasapi/issues/429).  
- **Proposal discussion link:**  
  - [https://github.com/brainglobe/brainglobe-atlasapi/pull/554](https://github.com/brainglobe/brainglobe-atlasapi/pull/554)  
    This is a closed PR where I created a new file containing the wrapper function to convert an atlas to an OpenSANDS object and its file path.

---

## Project proposal

### Synopsis
As someone deeply fascinated by the intricate workings of the brain, I have always admired how neuroanatomical atlases empower researchers to navigate complex brain structures with ease. BrainGlobe’s Atlas API stands out as a robust tool that consolidates atlas‑registered data into a unified Python interface. There is now an exciting opportunity to further enhance this system by adopting the OpenMINDS SANDS standard—a community‑driven format that delivers more interoperable brain data. This upgrade will enable researchers to derive deeper, more accurate insights.

My project aims to enhance the utility of the BrainGlobe ecosystem by updating the atlas packaging scripts so they output data in the OpenMINDS SANDS format. This upgrade is critical for researchers who need consistent, comprehensive data to integrate findings across studies and species. By delivering a modular, well-documented solution complete with rigorous testing, I will enable both seasoned neuroscientists and new entrants in the field, making advanced neuroinformatics more accessible to all.

### Implementation timeline

1. **Minimal Deliverables:**
   - Modify existing atlas packaging code to output atlas data conforming to the OpenMINDS SANDS standard.
   - Adapt at least one packaging script (e.g., the Allen Human atlas script) to incorporate this new functionality.
   - Develop comprehensive tests covering all new and modified features.
   - Update the documentation to guide users on how to generate and utilize OpenMINDS SANDS‑compliant atlases.
2. **Stretch Goals (if time permits):**
   - Extend support for additional species or imaging modalities.
   - Integrate schema validation using tools like `jsonschema` to ensure full compliance with OpenMINDS SANDS.
   - Create a conversion utility for existing atlas packages to the new standard.
3. **Time Commitment:**  
   I will be devoting 30–35 hours per week towards this GSoC project.

| **Week** | **Tasks & Deliverables**                                                                                                                                                                                                                                         | **Hours** |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 1–2      | **Community Bonding & Research:**<br>- Immerse myself in the BrainGlobe Atlas API, current packaging scripts, and OpenMINDS SANDS documentation.<br>- Engage with mentors to clarify requirements and set up a focused development environment.      | 30        |
| 3–4      | **Design & Planning:**<br>- Map the existing atlas data to the OpenMINDS SANDS schema.<br>- Design a modular function (e.g., `wrapup_atlas_to_openminds`) and create clear wireframes for the conversion workflow.                                      | 30        |
| 5–6      | **Core Development – Part 1:**<br>- Develop the new wrap‑up function in a separate module (e.g., `openminds_wrapup.py`).<br>- Adapt the Allen Human atlas packaging script to integrate this function and produce the new output.                         | 30        |
| 7–8      | **Core Development – Part 2:**<br>- Enhance error handling, refine the field mappings, and write initial unit tests.<br>- Begin documenting the new process and gather early feedback from mentors and community members.                                  | 30        |
| 9–10     | **Testing & Feedback:**<br>- Develop comprehensive tests to validate the JSON output against the OpenMINDS SANDS schema.<br>- Incorporate community and mentor feedback, addressing any emerging issues.                                                  | 30        |
| 11–12    | **Finalization:**<br>- Polish the code and documentation, complete remaining tests, and prepare a final demo video.<br>- Reserve extra time to resolve unforeseen challenges and ensure high-quality deliverables.                                            | 30        |

---

### Communication plan
I plan to maintain an open line of communication with my mentors through daily updates on Zulip and weekly video calls to discuss progress and challenges. I will also post regular status updates on GitHub issues and pull requests, ensuring transparency and timely feedback throughout the project.

---

## Personal statement

### Past experience
I am well-suited for this project due to my solid programming background and practical experience working on neuroscience assignments during my studies at IIIT Delhi. I started learning Python in high school and have since built several projects, including a simple password manager and various data analysis scripts. In my coursework, I completed three neuroscience projects that involved processing and visualizing complex experimental data. For instance, I created raster and peri-stimulus time plots to analyze neuronal activity across different stimuli, statistically analyzed behavioral data from decision-making experiments, and generated figures that brought experimental results to life.

These projects have given me a strong foundation in handling and interpreting neurophysiological data, even though I have not directly worked on mesh generation or image data processing in a professional context. Additionally, my coursework in data structures, operating systems, and embedded systems has taught me to approach problems methodically and to learn collaboratively. I am genuinely excited about the opportunity to contribute to the BrainGlobe Atlas API project and look forward to learning and growing through this experience.

### Motivation: Why This Project?
The intersection of neuroscience and open source has always been a source of inspiration for me—it’s where rigorous science meets accessible technology. During a neuroscience course with Prof. Mrinmoy Chakroborty, I experienced firsthand the frustration researchers face when working with diverse and incompatible data formats. This project excites me because it tackles a real, pressing issue: enhancing the interoperability of neuroanatomical atlases by standardizing data output. By modifying the Atlas API to output data in a more comprehensive and consistent format, I believe we can unlock new possibilities for integrating brain atlas data with microservices and other research tools. I am driven by the opportunity to create a solution that not only supports innovative research but also empowers a global community of scientists to collaborate more effectively. This project perfectly aligns with my passion for making complex data accessible and impactful.

### Match: Why You?
I am currently a third-year undergraduate student at IIIT Delhi with a deep passion for programming and neuroscience. My journey began in class 11 when I first learned Python, networking, and SQL—a foundation that quickly evolved as I secured 94% in my Class 12 Computer Science board exam. Over the years, I have built several projects, including an elementary password manager using Python and SQL, and in my first year, I worked on diverse projects such as solving equations using RREF and extensive file handling in Python. In addition to Python, I have a solid background in C++ and have successfully completed courses in data structures, algorithms, and operating systems. I also pursued courses in embedded systems using open source software like Yosys, Vivado, and GTKWAVE simulator.

More recently, I used Python for data analysis in a neuroscience project where I analyzed cortical neuron activity from different brain regions using experimental datasets. These assignments—where I created detailed raster plots, peri-stimulus time plots, and performed comprehensive statistical analyses—have given me the skills to handle complex neurophysiological data. These experiences have not only strengthened my technical expertise but have also instilled a passion for applying programming to solve real-world challenges in neuroscience and beyond.

### Availability
I have a flexible schedule with no conflicting commitments during the GSoC period. I am currently attending IIIT Delhi with a low course load this semester, which will allow me ample time to contribute meaningfully to the project. I can reliably dedicate approximately 15 hours per week to this project, with additional time available on weekends if needed. I plan to integrate my work seamlessly with my academic and personal responsibilities, ensuring consistent progress throughout the program.

---

## GSoC

### GSoC experience
I view GSoC as a transformative opportunity to collaborate with seasoned open source developers and deepen my technical expertise through a real-world project. I expect to gain valuable insights into best practices for scientific software development, enhance my collaborative skills, and contribute meaningfully to a project that has a significant impact on neuroinformatics. The program will not only refine my technical capabilities but also allow me to build lasting connections within the open source community.

### Are you also applying to projects with other organisations in GSoC 2025?
I am focusing solely on this project with BrainGlobe for GSoC 2025, as it perfectly aligns with my interests and professional goals. This project is my top priority, and I am fully committed to its success.
