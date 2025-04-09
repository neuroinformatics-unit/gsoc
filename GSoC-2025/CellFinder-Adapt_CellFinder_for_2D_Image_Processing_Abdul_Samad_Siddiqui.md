## Project title : CellFinder- Adapt CellFinder for 2D Image Processing (Abdul Samad Siddiqui)

## Personal details
- **Full name**: Abdul Samad Siddiqui
- **Email**: abdulsamadsid1@gmail.com
- **GitHub username**: [samadpls](https://github.com/samadpls)
- **Zulip username**: [Abdul Samad Siddiqui](https://neuroinformatics.zulipchat.com/#user/890604)
- **Location & time-zone**: Pakistan & GMT +5:00 (PKT)
- **Personal website / project portfolio**: [GitHub Portfolio](https://github.com/samadpls/)
- **Code contribution**: 
  - [[ENH] Add progress bar for training widget](https://github.com/brainglobe/cellfinder/pull/500)
  - [[ENH] Fix internet connection check for global accessibility](https://github.com/brainglobe/brainglobe-atlasapi/pull/536)
- **Proposal discussion link**: https://github.com/neuroinformatics-unit/gsoc/pull/13

## Project proposal 
_Length: max 1 page_

### Synopsis
This project aims to extend the functionality of BrainGlobe’s CellFinder tool to support two-dimensional brain slice images. Currently, CellFinder relies on a ResNet-based classifier optimized for three-dimensional whole-brain images. This project will implement a neural network tailored for 2D image classification, refactor the image processing pipeline to support both 2D and 3D images, and enhance documentation and testing to ensure usability and reproducibility. The deliverables include a 2D neural network classifier, an updated image processing pipeline, comprehensive documentation, and a blog post demonstrating the new functionality.

### Implementation timeline
1. **Minimal set of deliverables**:
   - Implement a neural network for 2D image classification.
   - Refactor the image processing pipeline to support 2D data.
   - Develop tests and documentation for the new functionality.
   - Publish a blog post demonstrating CellFinder’s 2D processing capabilities.

2. **Stretch goals**:
   - Optimize the 2D classifier for edge-case handling.
   - Expand testing coverage to include diverse datasets.

3. **Weekly timeline**:
   | Weeks | Dates | Tasks | Hours/Week |
   |-------|-------|-------|------------|
   | 1-2   | June 2 - June 13 | Modify blob detection algorithm to support 2D images, refactor the image processing pipeline for 2D data | 35 |
   | 3-4   | June 16 - June 27 | Conduct initial testing and debugging for 2D compatibility, design and implement the 2D neural network classifier | 35 |
   | 5     | June 30 - July 4 | **Exam Break** (No work) | 0 |
   | 6-7   | July 7 - July 18 | Integrate the 2D classifier into CellFinder, conduct initial testing, optimize the 2D classifier for accuracy and efficiency | 45 |
   | 8-9   | July 21 - August 1 | Validate the model across multiple 2D brain slice datasets, ensure compatibility with existing 3D workflows in CellFinder | 45 |
   | 10-11 | August 4 - August 17 | Expand testing coverage, address bugs or performance issues, write comprehensive documentation for the new 2D functionality | 45 |
   | 12    | August 18 - August 22 | Develop user tutorials, publish a blog post, final testing | 45 |

### Communication plan
- **Frequency**: Biweekly video calls with mentors (or weekly, depending on mentor availability) for in-depth discussions and progress reviews.
- **Channels**: Regular updates via Zulip chat for daily communication and quick feedback.
- **Progress tracking**: GitHub updates and comprehensive documentation to ensure transparency and track progress effectively.

## Personal statement
_Length: max 0.75 page_

### Past experience
I am a final-year undergraduate student with three years of experience in AI, open-source development, and computational neuroscience. My experience includes:
- **AI Engineer at Radium**: Specializing in LLMs, generative AI, and machine learning, working on production-grade AI systems and Python APIs.
- **GSoC 2024 with INCF (HNN-core)**: Worked under a Brown University professor to enhance HNN-core for MEG/EEG data analysis, implementing batch simulations and SBI tutorials.
- **Intern at Linux Foundation (Open Mainframe Project)**: Contributed to Zowe Python SDK, improving enterprise integration.
- **Speaker at Open Source Summit Europe'2024**: Presented on AI and open-source collaboration at Austria’s Open Source Summit.
- **Open-Source Contributor**: Active for three years, contributing to AI, ML, and neuroscience-related projects.

### Motivation: why this project?
I am passionate about advancing neuroscience research through open-source tools. Adapting CellFinder for 2D image processing will make it more accessible to researchers working with 2D brain slice images, broadening its impact in the neuroscience community. This project aligns with my interests in deep learning and neuroinformatics, and I am excited to contribute to a tool that has the potential to accelerate discoveries in brain research.

### Match: why you?
My experience in deep learning, open-source development, and neuroscience makes me well-suited for this project. I have successfully contributed to complex AI systems and open-source projects, and I am confident in my ability to deliver high-quality results. My past work on HNN-core and Modularity AI has prepared me to tackle the challenges of adapting CellFinder for 2D image processing.

### Availability
I am fully committed to this project and will dedicate 35+ hours per week. I will be unavailable from June 30-July 4 due to final exams but will compensate by working extra hours afterward.

## GSoC
_Length: max 0.25 page_

### GSoC experience
I participated in GSoC 2024 with INCF, where I worked on enhancing HNN-core for MEG/EEG data analysis. This experience taught me the importance of collaboration, clear communication, and iterative development in open-source projects. I look forward to applying these lessons to the CellFinder project.

### Are you also applying to projects with other organisations in GSoC 2025?
No I haven't submitted to the any other organizations I want to solely focus on this project.