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
  - https://github.com/neuroinformatics-unit/gsoc/pull/44  

---

## Project proposal

### Synopsis
As someone deeply fascinated by the intricate workings of the brain, I have always admired how neuroanatomical atlases empower researchers to navigate complex brain structures with ease. BrainGlobe’s Atlas API stands out as a robust tool that consolidates atlas‑registered data into a unified Python interface. There is now an exciting opportunity to further enhance this system by adopting the OpenMINDS SANDS standard—a community‑driven format that delivers more interoperable brain data. This upgrade will enable researchers to derive deeper, more accurate insights and enable integration with tools and microserivices.

This implentation would entail : 
1) Analyzing the OpenMINDS SANDS schema to understand its structure and requirements for representing different atlas components (e.g., regions, hierarchies, metadata).

2) Developing a modular Python function (openminds_wrapup) that will take the internally processed atlas data from the existing packaging scripts and convert it into the OpenMINDS SANDS JSON format. This method will involve mapping BrainGlobe's internal data structures to the corresponding OpenMINDS SANDS entities and properties. 
3) Adapting the packaging script for the Allen Mouse Atlas to integrate this new openminds_wrapup function, ensuring that the resulting atlas data adheres to the SANDS standard. 
4) Creating comprehensive unit and integration tests to validate the correctness and schema compliance of the generated OpenMINDS SANDS output. 
5) Updating the BrainGlobe Atlas API documentation to guide users on generating and utilizing OpenMINDS SANDS-compliant atlases. By delivering this enhanced capability, the project will empower researchers with more interoperable and standardized brain atlas data, fostering broader data sharing and collaborative analysis within the neuroinformatics community.

### Implementation timeline

1. **Minimal Deliverables:**
   - Modify existing atlas packaging code to output atlas data conforming to the OpenMINDS SANDS standard.
   - Adapt at least one packaging script (e.g., the Allen Mouse atlas script) to incorporate this new functionality.
   - Develop comprehensive tests covering all new and modified features,specifically validating the generated JSON against the OpenMINDS SANDS schema.
   - Update the documentation to guide users on how to generate and utilize OpenMINDS SANDS‑compliant atlases.
2. **Stretch Goals (if time permits):**
   - Extend support for generating OpenMINDS SANDS output for additional existing atlases within the BrainGlobe ecosystem.
   - Integrate schema validation using tools like `jsonschema` within the openminds_wrapup function to ensure the generated JSON strictly adheres to the OpenMINDS SANDS schema.
   - Create a conversion script to facilitate the conversion of newly generated BrainGlobe atlas data (in the current standard format) to the OpenMINDS SANDS format.
3. **Time Commitment:**  
   I will be devoting 30–35 hours per week towards this GSoC project.

| **Week** | **Dates (Approx.)** | **Tasks & Deliverables (Estimated Hours)** |
|---|---|---|
| **1-2** | May 5 - May 18 | Immerse myself in the BrainGlobe Atlas API, current packaging scripts, and OpenMINDS SANDS documentation. Engage with mentors to clarify requirements and set up a focused development environment. | 30 |
| **3-4** | May 19 - June 1 | Map the existing atlas data to the OpenMINDS SANDS schema. Design a modular function (e.g., `wrapup_atlas_to_openminds`) and create clear wireframes for the conversion workflow. | 30 |
| **5-6** | June 2 - June 15 (Summer Break) | Develop the new `wrapup_atlas_to_openminds` function in a separate module (e.g., `openminds_wrapup.py`). Adapt the Allen mouse atlas packaging script to integrate this function and produce the new output. | 35 - 40 |
| **7-8** | June 16 - June 29 (Summer Break) | Enhance error handling, refine the field mappings, and write initial unit tests. Begin documenting the new process and gather early feedback from mentors and community members. | 35 - 40 |
| **9-10** | June 30 - July 13 | Develop comprehensive tests to validate the JSON output against the OpenMINDS SANDS schema. Incorporate community and mentor feedback, addressing any emerging issues. | 30 - 35 |
| **11-12** | July 14 - July 27 | Finalization and documentation: Polish the code and documentation, complete remaining tests, and prepare a final demo video. Reserve extra time to resolve unforeseen challenges. Create similar wrappers for other high-priority atlases and follow through on the process of testing and documenting if time permits. Try to create a universal wrapper function to convert the packaging script of ANY atlas to conform to the OpenMINDS SANDS schema so that this functionality is extended to any newly added atlases. | 30 - 35 |
---

### Communication plan
I plan to maintain an open line of communication with my mentors through daily updates on Zulip and weekly video calls to discuss progress and challenges. I will also post regular status updates on GitHub issues and pull requests, ensuring transparency and timely feedback throughout the project.

---

## Personal statement

### Past experience
I am well-suited for this project due to my solid programming background and practical experience working on neuroscience projects during my studies at IIIT Delhi. I started learning Python and SQL in high school and have since built several projects, including a simple password manager and various data analysis scripts. In my coursework, I completed three neuroscience projects that involved processing and visualizing complex experimental data. For instance, I created raster and peri-stimulus time plots to analyze neuronal activity across different stimuli, statistically analyzed behavioral data from decision-making experiments, and generated figures that brought experimental results to life.

These projects have given me a strong foundation in handling and interpreting neurophysiological data, even though I have not directly worked on data schema conversion or image data processing in a professional context.I believe my coursework in data structures would help me convert the existing data format to the required data schema. Additionally, my coursework in algorithms, operating systems, and embedded systems has taught me to approach problems methodically and to learn collaboratively. I am genuinely excited about the opportunity to contribute to the BrainGlobe Atlas API project and look forward to learning and growing through this experience.

### Motivation: Why This Project?
The intersection of neuroscience and open source has always been a source of inspiration for me—it’s where rigorous science meets accessible technology. During a neuroscience course with Prof. Mrinmoy Chakroborty, I experienced firsthand the frustration researchers face when working with diverse and incompatible data formats. This project excites me because it tackles a real, pressing issue: enhancing the interoperability of neuroanatomical atlases by standardizing data output. By modifying the Atlas API to output data in a more comprehensive and consistent format, we can enable integration of brain atlas data with microservices and other research tools.

### Match: Why You?
I am currently a third-year undergraduate student at IIIT Delhi with a deep passion for programming and neuroscience. My journey began in class 11 when I first learned Python, networking, and SQL—a foundation that quickly evolved as I secured 94% in my Class 12 Computer Science board exam. Over the years, I have built several projects, including an elementary password manager using Python and SQL, and in my first year, I worked on diverse projects such as solving equations using RREF and extensive file handling in Python. In addition to Python, I have a solid background in C++ and have successfully completed courses in data structures, algorithms, and operating systems. I also pursued courses in embedded systems using open source software like Yosys, Vivado, and GTKWAVE simulator.

More recently, I used Python for data analysis in a neuroscience project where I analyzed cortical neuron activity from different brain regions using experimental datasets. These assignments—where I created detailed raster plots, peri-stimulus time plots, and performed comprehensive statistical analyses—have given me the skills to handle complex neurophysiological data. These experiences have enhanced my technical knwoledge and has instilled a passion for applying programming to solve real-world challenges in neuroscience and beyond.

### Availability
I have a flexible schedule with no conflicting commitments during the GSoC period. I am currently attending IIIT Delhi with a low course load this semester, which will allow me ample time to contribute meaningfully to the project.I have my summer break starting from June where I can dedicate even more time (40-45 hours) if needed. I can reliably dedicate approximately 30-35 hours per week to this project, with additional time available on weekends if needed. I plan to integrate my work seamlessly with my academic and personal responsibilities, ensuring consistent progress throughout the program.

---

## GSoC

### GSoC experience
I view GSoC as a transformative opportunity to work closely with experienced open source developers and to enhance my technical expertise through real-world project work. I expect to gain invaluable insights into best practices for scientific software development, refine my collaborative skills, and contribute significantly to a project that impacts neuroinformatics research. This experience will help me build lasting connections in the open source community while advancing my technical skills.

### Are you also applying to projects with other organisations in GSoC 2025?
While I have also applied to Fedora, BrainGlobe is my organization of choice for GSoC 2025. My strong interest in neuroscience and scientific programming makes this project my primary focus. I am fully committed to dedicating my efforts to this project and ensuring its successful completion.
