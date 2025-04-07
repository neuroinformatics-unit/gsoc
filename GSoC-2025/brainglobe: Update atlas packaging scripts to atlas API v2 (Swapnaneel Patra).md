
## brainglobe: Update atlas packaging scripts to atlas API v2 (Swapnaneel Patra)

## Personal details

- **Full name**: Swapnaneel Patra
- **Email**: <swapnaneel06@gmail.com>
- **GitHub username**: thisisrick25
- **Zulip username**: Swapnaneel
- **Location & time-zone**: Kolkata, India, GMT+5:30
- **Personal website / project portfolio**: [github.com](https://github.com/thisisrick25)
- **Code contribution**: [https://github.com/brainglobe/brainglobe-atlasapi/pull/555](https://github.com/brainglobe/brainglobe-atlasapi/pull/555)
- **Proposal discussion link**: https://github.com/neuroinformatics-unit/gsoc/pull/56

## Project proposal

_Length: max 1 page_

- **Synopsis**

This project aims to update the BrainGlobe Atlas API by integrating the OpenMINDS SANDS standard for neuroanatomical atlases.
This project will facilitate the collaboration between different neuroinformatics tools.
By improving how atlas data is shared and used, researchers and developers can collaborate more effectively, sparking innovations in neuroanatomical research.
This standardization is critical for improving data accessibility and integration within the neuroinformatics community.
The deliverables include modifications to the Atlas packaging Python code, adaptation of at least one packaging script to use the new functionality,
comprehensive tests, and updated documentation.
The open source community will benefit through improved data interoperability, ease of integration for new atlases,
and enhanced reproducibility in neuroanatomical research.

- **Implementation timeline**

    1. A bullet point list with **minimal set of deliverables**
        - Update atlas packaging Python code to output OpenMINDS SANDS compliant files.
        - Adapt at least one existing packaging script to utilize the new functionality.
        - Develop and run unit and integration tests covering the updated functionality.
        - Update and expand documentation to reflect new usage and features.

    2. Additional **stretch goals** or "if time allows" deliverables
        - Update more of the existing BrainGlobe atlas packaging scripts (beyond the minimally required one) to generate output compliant with OpenMINDS SANDS. The ideal goal would be to update all major scripts.
        - Add checks within the updated packaging code to validate the generated output against the OpenMINDS SANDS schema, ensuring correctness and compliance.
        - Create detailed example notebooks or tutorials showcasing how to use the updated packaging scripts for different atlases and potentially demonstrating how to query/use the resulting OpenMINDS SANDS data structure.

    3. A detailed **weekly timeline**: when do you plan to do what?

| Week       | Tasks                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Community Bonding**| Become familiar with the BrainGlobe Atlas API and OpenMINDS SANDS spec; set up development environment; initial discussions with mentors.      |
| Week 1     | Investigate current packaging scripts; analyze differences between existing format and OpenMINDS SANDS; draft initial design ideas.          |
| Week 2     | Prepare a detailed design document outlining required code changes and data schema adjustments; start initial code modifications with accompanying unit tests.            |
| Week 3     | Implement core modifications in the packaging code for OpenMINDS SANDS support; begin writing unit tests.                                     |
| Week 4     | Adapt one selected packaging script to use the new functionality; write unit tests and initial integration tests for the script adaptation.             |
| Week 5     | Integrate mentor feedback; refine code and tests; update documentation draft with examples and usage instructions.                           |
| Week 6  **Mid-term**     | Verify core SANDS writing code, first adapted script, and initial passing tests (unit & integration) are functional. Address major blockers.              |
| Week 7     | Refine core implementation based on mid-term feedback. Improve test coverage (unit & integration). Address bugs.                             |
| Week 8     | Polish code; ensure high test coverage; update documentation based on test outcomes.                        |
| Week 9     | Finalize additional features; Finalize test suite (unit & integration); conduct peer reviews with mentors and community contributors.              |
| Week 10    | Address stretch goals (e.g., adapt another script, add validation), ensuring tests accompany any new code. Begin code freeze process; focus on bug fixes, documentation polishing, and ensuring all deliverables meet the OpenMINDS SANDS standard.      |
| Week 11    | Final refinements; complete any remaining tests; draft the final report and submission documentation.                              |
| Week 12    | Finalize the project deliverables; ensure all documentation, tests, and code are up-to-date; prepare for final project submission and review. |

I plan to dedicate approximately 30 hours per week throughout the program.

- **Communication plan**
  
  - Github: Issue tracking and PR review
  - Zulip: Regular weekly updates/questions related to day-to-day activity
  - Email: if needed
    
  Progress will be tracked via regular updates and PRs. If significant delays occur approaching the mid-term, I will proactively communicate with mentors to diagnose issues and, if needed, collaboratively adjust the project scope or plan to ensure successful completion of core goals.



## Personal statement

_Length: max 0.75 page_

- **Past experience**: I graduated in 2023 and have worked on multiple personal projects. Until November 2024, I worked as a Junior Software Engineer. I have a strong background in programming languages such as C/C++, Python, JavaScript, and TypeScript. I also have experience working with medical imaging formats (such as NIfTI and DICOM) while working on the [cardiac image segmentation](https://github.com/thisisrick25/heart-image-segmentation) project.

- **Motivation: why this project?**: 
    - I am very intrigued by neuroscience and see this project as a perfect opportunity to combine my interest in the field with open-source development.
    - I am motivated by the chance to improve the BrainGlobe Atlas API, a critical tool for standardizing neuroanatomical data, by integrating the OpenMINDS SANDS standard.
    - Working on this project will help me develop my skills in Python, data standards, and collaborative coding, which are essential for my professional growth and will establish a foundation for future academic pursuits in neuroscience.
    - I envision this project benefiting the open-source community by making neuroanatomical data more consistent and usable, encouraging greater collaboration and innovation in neuroscience research.

- **Match: why you?**: My experience as a software engineer, combined with my academic background, has equipped me with practical skills in developing well-documented, production-quality code. I enjoy tackling unfamiliar concepts, learning them on the job, and implementing innovative ideas.
  
- **Availability**: I am fully available for the complete duration of GSoC in its entirety, with no major conflicting commitments.


## GSoC

_Length: max 0.25 page_

- **GSoC experience**

    What do you expect from the program?
  
    I'm excited to be participating in GSoC for the first time. I've always been passionate about neuroscience, I see this program as an opportunity to break into the field while getting hands-on experience with open-source development and collaborative coding. I hope to learn valuable insights about pursuing a career in neuroscience and create software that makes a difference in scientific research. I'm eager to contribute meaningful improvements to the project and pick up best practices for maintaining and advancing scientific software tools, and I believe this experience will also be a great asset in my graduate studies.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, I am not applying to any other projects with other organisations.
