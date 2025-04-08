## Personal details
- **Full name**  Pranav Kapoor
- **Email** pranav33317@gmail.com
- **GitHub username** pranav33317
- **Zulip username** Pranav Kapoor 
- **Location & time-zone** New Delhi,India and IST (GMT+5:30)
- **Personal website / project portfolio** (optional) www.github.com/pranav33317
- **Code contribution**

    PR : https://github.com/brainglobe/brainglobe-atlasapi/pull/546#pullrequestreview-2729541724
    I tried to disable parallel mesh creation in various files to simplify mesh creation and simultaneosly working on https://github.com/brainglobe/brainglobe-atlasapi/issues/429. 
- Proposal PR:
    https://github.com/neuroinformatics-unit/gsoc/pull/44

## Project proposal 

- **Synopsis**

    As someone deeply fascinated by the intricate workings of the brain, I have always admired how neuroanatomical atlases empower researchers to navigate complex brain structures with ease. There is now an exciting opportunity to further enhance this system by adopting the OpenMINDS SANDS standard—a community‑driven format that delivers more interoperable brain data and enhances the utility of the BrainGlobe ecosystem by facilitating seamless integration and analysis across different datasets and tools.This will entail: 

    1) Analyzing the OpenMINDS SANDS schema to understand its structure and requirements for representing different atlas components (e.g., regions, hierarchies, metadata).

    2) Developing a modular Python function (openminds_wrapup) that will take the internally processed atlas data from the existing packaging scripts and transform it into the OpenMINDS SANDS JSON format.This function will involve mapping BrainGlobe's internal data structures to the corresponding OpenMINDS SANDS entities and properties.

    3) Adapting the packaging script for the Allen Mouse Atlas to integrate this new openminds_wrapup function, ensuring that the resulting atlas data adheres to the SANDS standard. 

    4) Creating comprehensive unit and integration tests to validate the correctness and schema compliance of the OpenMINDS SANDS output.

    5) Updating the BrainGlobe Atlas API documentation to guide users on generating and utilizing OpenMINDS SANDS-compliant atlases.

    By implementing this functionality, the project will empower researchers with more interoperable and standardized brain atlas data.

- **Implementation timeline**
    1.Modify existing atlas packaging code to output atlas data conforming to the OpenMINDS SANDS standard.This will involve creating a new modular function for the data transformation.

    2.Adapt at least one packaging script (e.g., the Allen Mouse Atlas script) to incorporate this new functionality, ensuring it produces OpenMINDS SANDS-compliant output.

    3.Develop comprehensive tests covering all new and modified features, specifically validating the generated JSON against the OpenMINDS SANDS schema.

    4.Update the documentation to guide users on how to generate and utilize OpenMINDS SANDS‑compliant atlases, using exmaples using current atlases like the Allen mouse atlas.

    - Additional **stretch goals** 
    1.Extend support for generating OpenMINDS SANDS output for additional existing atlases within the BrainGlobe ecosystem.

    2.Integrate schema validation using a Python library like jsonschema within the openminds_wrapup function to automatically ensure the generated JSON strictly adheres to the OpenMINDS SANDS schema.
    
    3.Create a utility script or function to facilitate the conversion of newly generated BrainGlobe atlas data (in the current standard format) to the OpenMINDS SANDS format. This would focus on converting newly added atlases.

    3. A detailed **weekly timeline**: 
        I will be devoting 30-35 hours per week towards this GSoC project.

        | **Week** | **Dates (Approx.)** | **Tasks & Deliverables (Estimated Hours)** |
|---|---|---|
| **1-2** | May 5 - May 18 | Immerse myself in the BrainGlobe Atlas API, current packaging scripts, and OpenMINDS SANDS documentation. Engage with mentors to clarify requirements and set up a focused development environment. | 30 |
| **3-4** | May 19 - June 1 | Map the existing atlas data to the OpenMINDS SANDS schema. Design a modular function (e.g., `wrapup_atlas_to_openminds`) and create clear wireframes for the conversion workflow. | 30 |
| **5-6** | June 2 - June 15 | Develop the new `wrapup_atlas_to_openminds` function in a separate module (e.g., `openminds_wrapup.py`). Adapt the Allen mouse atlas packaging script to integrate this function and produce the new output. | 35 - 40 |
| **7-8** | June 16 - June 29 | Enhance error handling, refine the field mappings, and write initial unit tests. Begin documenting the new process and gather early feedback from mentors and community members. | 35 - 40 |
| **9-10** | June 30 - July 13 | Develop comprehensive tests to validate the JSON output against the OpenMINDS SANDS schema. Incorporate community and mentor feedback, addressing any emerging issues. | 30 - 35 |
| **11-12** | July 14 - July 27 | Finalization: Polish the code and documentation, complete remaining tests, and prepare a final demo video. Reserve extra time to resolve unforeseen challenges and ensure high-quality deliverables. Create similar wrappers for other high-priority atlases and follow through on the process of testing and documenting if time permits. Try to create a universal wrapper function to convert the packaging script of ANY atlas to conform to the OpenMINDS SANDS schema so that this functionality is extended to any newly added atlases. | 30 - 35 |

- **Communication plan**
    
    I plan to maintain an open line of communication with my mentors through daily updates on Zulip and weekly video calls to discuss progress and challenges. I’ll also post regular status updates on GitHub issues and pull requests, ensuring transparency and timely feedback throughout the project.

## Personal statement


- **Past experience.** 

    I am well-suited for this project due to my solid programming background and my practical experience working on neuroscience projects during my studies at IIIT Delhi. I started learning Python and SQL in high school and have since developed small projects, such as a simple password manager and various data analysis scripts. In my coursework, I completed three neuroscience projects that involved processing and visualizing complex experimental data. For example, I created raster and peri-stimulus time plots to analyze neuronal activity across different stimuli, statistically analyzed behavioral data from decision-making experiments, and generated figures that brought experimental results to life. 
    
    While I have not directly worked on image data processing or data schema prcoessing in a professional context, these coursework have given me a strong foundation in handling neurophysiological data.I believe my coursework in data structures would come on handy in creating a wrapper for updating the existing data schema .My experience in coursework related to algorithms, operating systems, and embedded systems has taught me to approach problems methodically and learn collaboratively while still learning on my own. I’m genuinely excited about the opportunity to contribute to the BrainGlobe Atlas API project and I am eager to learn and grow through this experience.
- **Motivation: why this project?**

   The intersection of neuroscience and open source has always been a source of fascination for me since its where where rigorous science meets accessible technology. During a course on neuroscience with Prof. Mrinmoy Chakroborty, I experienced firsthand the frustration researchers face when working with diverse and incompatible data formats. This project excites me because it tackles a real, pressing issue: enhancing the interoperability of neuroanatomical atlases by standardizing data output. By modifying the Atlas API to output data in a more comprehensive and consistent format, I believe we can unlock new possibilities for integrating brain atlas data with microservices and other research tools.
- **Match: why you?**

    I am currently a third-year undergraduate student at IIIT Delhi with a deep passion for programming and neuroscience. My journey began in class 11 when I first learned Python, networking, and SQL—a foundation that quickly evolved as I secured 94% in my Class 12 Computer Science board exam. Over the years, I have built several projects, including an elementary password manager using Python and SQL, and in my first year, I worked on diverse projects such as solving equations using RREF and extensive file handling in Python. In addition to Python, I have a solid background in C++ and have successfully completed courses in data structures, algorithms, and operating systems. I also pursued courses in embedded systems using open source software like Yosys, Vivado, and GTKWAVE simulator. More recently, I used Python for data analysis in a neuroscience project where I analyzed cortical neuron activity from different brain regions using experimental datasets. These experiences have not only strengthened my technical expertise and built my experience in image and data processing but have also instilled a passion for applying programming to solve real-world problems in neuroscience and beyond.
- **Availability**

    I have a flexible schedule with no conflicting commitments during the GSoC period.I am curretly attending my college IIIT Delhi but have a low course load this sememster which will allow me a lot of time to meaningfully contribute to the project. I can reliably dedicate approximately 30-35 hours per week to this project, with additional time available on weekends if needed.I also have my summer break starting from April where I could contribute upto 40-45 hours per week. I plan to integrate my work seamlessly with my academic and personal responsibilities, ensuring consistent progress throughout the program.

## GSoC


- **GSoC experience**

    I view GSoC as an opportunity to collaborate with open source developers and to deepen my technical expertise by working in a real‑world project. I expect to gain valuable insights into best practices for scientific software development and contribute meaningfully to a project .I aim to enhance my image and data processing experience and programming skills through real-world software development on this project.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    While I have also applied to Fedora, BrainGlobe is my organization of choice for GSoC 2025. My strong interest in neuroscience and scientific programming makes this project my primary focus. I am fully committed to dedicating my efforts to this project and ensuring its successful completion.
