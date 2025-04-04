
# brainglobe: Update atlas packaging scripts to atlas API v2 (Swapnaneel Patra)

## Personal details

Please include the following information:

- **Full name**: Swapnaneel Patra
- **Email**: <swapnaneel06@gmail.com>
- **GitHub username**: thisisrick25
- **Zulip username**: Swapnaneel
- **Location & time-zone**: Kolkata, India, GMT+5:30
- **Personal website / project portfolio**: [github.com](https://github.com/thisisrick25)
- **Code contribution**: [https://github.com/brainglobe/brainglobe-atlasapi/pull/555](https://github.com/brainglobe/brainglobe-atlasapi/pull/555)

- **Proposal discussion link**

    https://github.com/neuroinformatics-unit/gsoc/pull/56

## Project proposal

_Length: max 1 page_

- **Synopsis**

This project aims to update the BrainGlobe Atlas API by integrating the OpenMINDS SANDS standard for neuroanatomical atlases.
Currently, atlas packaging scripts convert public atlas data to a limited standard format; by adapting these scripts to produce output compliant with OpenMINDS SANDS,
The project will enable consistent, interoperable data representations across BrainGlobe tools.
This standardization is critical for improving data accessibility and integration within the neuroinformatics community.
The deliverables include modifications to the Atlas packaging Python code, adaptation of at least one packaging script to use the new functionality,
comprehensive tests, and updated documentation.
The open source community will benefit through improved data interoperability, ease of integration for new atlases,
and enhanced reproducibility in neuroanatomical research.

- **Implementation timeline**

    Please include the following information:
    1. A bullet point list with **minimal set of deliverables**
        - Update atlas packaging Python code to output OpenMINDS SANDS compliant files.
        - Adapt at least one existing packaging script to utilize the new functionality.
        - Develop and run unit and integration tests covering the updated functionality.
        - Update and expand documentation to reflect new usage and features.

    2. Additional **stretch goals** or "if time allows" deliverables
        - Extend support to additional packaging scripts within the BrainGlobe ecosystem.
        - Develop conversion utilities for legacy atlas data.
        - Create example notebooks and tutorials demonstrating the new capabilities.

    3. A detailed **weekly timeline**: when do you plan to do what?

| Week       | Tasks                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Community Bonding**| Become familiar with the BrainGlobe Atlas API and OpenMINDS SANDS spec; set up development environment; initial discussions with mentors.      |
| Week 1     | Investigate current packaging scripts; analyze differences between existing format and OpenMINDS SANDS; draft initial design ideas.          |
| Week 2     | Prepare a detailed design document outlining required code changes and data schema adjustments; start initial code modifications.            |
| Week 3     | Implement core modifications in the packaging code for OpenMINDS SANDS support; begin writing unit tests.                                     |
| Week 4     | Adapt one selected packaging script to use the new functionality; continue developing tests and refining the conversion process.             |
| Week 5     | Integrate mentor feedback; refine code and tests; update documentation draft with examples and usage instructions.                           |
| Week 6  **Mid-term:**     | Ensure more than half of the project is complete; perform integration tests; address any major issues or blockers.              |
| Week 7     | Implement stretch goals (if feasible); extend test coverage; review and improve code performance and readability.                             |
| Week 8     | Polish code; perform extensive manual testing with various atlas datasets; update documentation based on test outcomes.                        |
| Week 9     | Finalize additional features; prepare comprehensive test suites; conduct peer reviews with mentors and community contributors.              |
| Week 10    | Begin code freeze process; focus on bug fixes, documentation polishing, and ensuring all deliverables meet the OpenMINDS SANDS standard.      |
| Week 11    | Final refinements; complete any remaining tests; draft the final report and submission documentation.                              |
| Week 12    | Finalize the project deliverables; ensure all documentation, tests, and code are up-to-date; prepare for final project submission and review. |

I plan to dedicate around 15 hours per week throughout the program.

- **Communication plan**
  
  - Github: Issue tracking and PR review
  - Zulip: Regular weekly updates/questions related to day-to-day activity
  - Email: if needed



## GSoC

_Length: max 0.25 page_

- **GSoC experience**

    What do you expect from the program?
    I'm excited to be participating in GSoC for the first time. I've always been passionate about neuroscience, I see this program as an opportunity to break into the field while getting hands-on experience with open-source development and collaborative coding. I hope to learn valuable insights about pursuing a career in neuroscience and create software that makes a difference in scientific research. I'm eager to contribute meaningful improvements to the project and pick up best practices for maintaining and advancing scientific software tools, and I believe this experience will also be a great asset in my graduate studies.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, I am not applying to any other projects with other organisations.
