## Personal details
- **Full name**  Pranav Kapoor
- **Email** pranav33317@gmail.com
- **GitHub username** pranav33317
- **Zulip username** Pranav Kapoor 
- **Location & time-zone** New Delhi,India and IST (GMT+5:30)
- **Personal website / project portfolio** (optional) www.github.com/pranav33317
- **Code contribution**

    Please link a pull request, ideally submitted to your chosen project or one of the NIU tools. Applications without a code contribution won't be considered. It must be publicly visible and represent your own work, although you may have help from other developers in the community to further improve it. It must be meaningful code contribution (i.e. not just fixing a minor spelling mistake). While AI tools (such as Copilot etc) can be a very useful, contributions mostly created by AI are unlikely to be useful, and will not be accepted. You can link more than one pull request if desired.

    Ans.  PR : https://github.com/brainglobe/brainglobe-atlasapi/pull/546#pullrequestreview-2729541724
    I tried to disable parallel mesh creation in various files to simplify mesh creation and am simultaneosly working on https://github.com/brainglobe/brainglobe-atlasapi/issues/429. 

- **Proposal discussion link**

    Please link to the pull request where you discussed your project proposal with the community. 

    https://github.com/brainglobe/brainglobe-atlasapi/pull/554
    This is a closed PR where I created a new file which contained the wrapper function to convert atlas to OpenSANDS object and its file path.

## Project proposal 

    Briefly explain: what is the project about? Why is it important? What are the goals? What are the deliverables? How would the open source community benefit from this project?

    As someone deeply fascinated by the intricate workings of the brain, I have always admired how neuroanatomical atlases empower researchers to navigate complex brain structures with ease. BrainGlobe’s Atlas API stands out as a robust tool that consolidates atlas‑registered data into a unified Python interface. There is now an exciting opportunity to further enhance this system by adopting the OpenMINDS SANDS standard—a community‑driven format that delivers more interoperable brain data. This upgrade will enable researchers to derive deeper, more accurate insights.
    
    My project aims to enhance the utility of the BrainGlobe ecosystem by updating the atlas packaging scripts so they output data in the OpenMINDS SANDS format. This upgrade is critical for researchers who need consistent, comprehensive data to integrate findings across studies and species. By delivering a modular, well-documented solution complete with rigorous testing, I will enable both seasoned neuroscientists and new entrants in the field, making advanced neuroinformatics more accessible to all.

- **Implementation timeline**
        1.        
        Minimal Deliverables:
        Modify existing atlas packaging code to output atlas data conforming to the OpenMINDS SANDS standard.
        Adapt at least one packaging script (e.g., the Allen Human atlas script) to incorporate this new functionality.
        Develop comprehensive tests covering all new and modified features.
        Update the documentation to guide users on how to generate and utilize OpenMINDS SANDS‑compliant atlases.
        2.
        Stretch Goals (if time permits):
        Extend support for additional species or imaging modalities.
        Integrate schema validation using tools like jsonschema to ensure full compliance with OpenMINDS SANDS.
        Create a conversion utility for existing atlas packages to the new standard.
        3.
        I will be devoting 30-35 hours per week towards this GSoC project.
        Week 1–2 : Immerse myself in the BrainGlobe Atlas API, current packaging scripts, and OpenMINDS SANDS documentation. Engage with mentors to clarify requirements and set up a focused development environment.
        Week 3–4 : Map the existing atlas data to the OpenMINDS SANDS schema. Design a modular function (e.g., wrapup_atlas_to_openminds) and create clear wireframes for the conversion workflow.
        Week 5–6 :  Develop the new wrap‑up function in a separate module (e.g., openminds_wrapup.py). Adapt the Allen Human atlas packaging script to integrate this function and produce the new output.
        Week 7–8 : Enhance error handling, refine the field mappings, and write initial unit tests. Begin documenting the new process and gather early feedback from mentors and community members.	30
        Week 9–10 : Develop comprehensive tests to validate the JSON output against the OpenMINDS SANDS schema. Incorporate community and mentor feedback, addressing any emerging issues.
        Week 11–12	Finalization: Polish the code and documentation, complete remaining tests, and prepare a final demo video. Reserve extra time to resolve unforeseen challenges and ensure high-quality deliverables.

- **Communication plan**

    Please explain: how do you plan to communicate with your mentor? How often? (e.g., daily or weekly stand-ups, longer meetings..?) What communication channels will you use? (e.g., video calls, Zulip chat...?)
    
    I plan to maintain an open line of communication with my mentors through daily updates on Zulip and weekly video calls to discuss progress and challenges. I’ll also post regular status updates on GitHub issues and pull requests, ensuring transparency and timely feedback throughout the project.

## Personal statement

- **Past experience.** 

    Please describe your past experience with programming, open source, or any other experience you deem relevant for the project you are applying for. Any successful open source projects, published work or content of the like should definitely be highlighted.

    I am well-suited for this project due to my solid programming background and my practical experience working on neuroscience assignments during my studies at IIIT Delhi. I started learning Python in high school and have since developed small projects, such as a simple password manager and various data analysis scripts. In my coursework, I completed three neuroscience projects that involved processing and visualizing complex experimental data. For example, I created raster and peri-stimulus time plots to analyze neuronal activity across different stimuli, statistically analyzed behavioral data from decision-making experiments, and generated figures that brought experimental results to life. 

   While I have not directly worked on mesh generation or image data processing in a professional context, these coursework have given me a strong foundation in handling and interpreting neurophysiological data. My experience in coursework related to data structures, operating systems, and embedded systems has taught me to approach problems methodically and learn collaboratively while still learning comprehensively. I’m genuinely excited about the opportunity to contribute to the BrainGlobe Atlas API project and I am eager to learn and grow through this experience.
- **Motivation: why this project?**

    Why are you interested in this specific project? What aspects of it motivate you to work on it? How does it link to your personal or professional interests? How do you envision its impact in the open source community?

   The intersection of neuroscience and open source has always been a source of fascination for me since its where where rigorous science meets accessible technology. During a course on neuroscience with Prof. Mrinmoy Chakroborty, I experienced firsthand the frustration researchers face when working with diverse and incompatible data formats. This project excites me because it tackles a real, pressing issue: enhancing the interoperability of neuroanatomical atlases by standardizing data output. By modifying the Atlas API to output data in a more comprehensive and consistent format, I believe we can unlock new possibilities for integrating brain atlas data with microservices and other research tools. I am driven by the opportunity to create a solution that not only supports innovative research but also empowers a global community of scientists to collaborate more effectively. This project perfectly aligns with my passion for making complex data accessible and impactful, and I am eager to contribute to it.
- **Match: why you?**

    Why should we choose you for this project? What unique skills or experiences can you bring to the project and the community? Is there something you have worked on in the past that makes you particularly well-suited for this project?
    I am currently a third-year undergraduate student at IIIT Delhi with a deep passion for programming and neuroscience. My journey began in class 11 when I first learned Python, networking, and SQL—a foundation that quickly evolved as I secured 94% in my Class 12 Computer Science board exam. Over the years, I have built several projects, including an elementary password manager using Python and SQL, and in my first year, I worked on diverse projects such as solving equations using RREF and extensive file handling in Python. In addition to Python, I have a solid background in C++ and have successfully completed courses in data structures, algorithms, and operating systems. I also pursued courses in embedded systems using open source software like Yosys, Vivado, and GTKWAVE simulator. More recently, I used Python for data analysis in a neuroscience project where I analyzed cortical neuron activity from different brain regions using experimental datasets. These experiences have not only strengthened my technical expertise but have also instilled a passion for applying programming to solve real-world problems in neuroscience and beyond.
- **Availability**

    Please state if you have any other plans for the work period (school work, another job, planned vacation)? If so, how do you plan to combine them with your GSoC work?

    I have a flexible schedule with no conflicting commitments during the GSoC period.I am curretly attending my college IIIT Delhi but have a low course load this sememster which will allow me a lot of time to meaningfully contribute to the project. I can reliably dedicate approximately 15 hours per week to this project, with additional time available on weekends if needed. I plan to integrate my work seamlessly with my academic and personal responsibilities, ensuring consistent progress throughout the program.

## GSoC


- **GSoC experience**

    What do you expect from the program?

     I view GSoC as a transformative opportunity to collaborate with seasoned open source developers and to deepen my technical expertise by working in a real‑world project. I expect to gain valuable insights into best practices for scientific software development, enhance my collaborative skills, and contribute meaningfully to a project with a significant impact in neuroinformatics. The program will not only refine my technical capabilities but also allow me to build lasting connections within the open source community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    If so, which ones? What would be your preference in case of a tie?
    I am focusing solely on this project with BrainGlobe for GSoC 2025, as it aligns perfectly with my interests and professional goals. This project is my top priority and I am fully committed to its success.
