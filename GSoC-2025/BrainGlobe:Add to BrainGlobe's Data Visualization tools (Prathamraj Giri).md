# BrainGlobe: Add to BrainGlobe's Data Visualization Tools

## Personal Details
- **Full Name:** Prathamraj Giri
- **Email:** [prathamraj2409@gmail.com]
- **GitHub Username:** [Pratham-ji]
- **Zulip Username:** [Prathamraj Giri](https://neuroinformatics.zulipchat.com/#user/889295) USER ID- 889295
- **Location & Timezone:** Dehradun, Uttarakhand, India (Asia/Kolkata)  UTC +5:30
- **Personal Website / Portfolio (optional):** [(https://prathame.netlify.app/)]

## Code Contribution
I have been exploring the `brainrender-napari` codebase to understand its architecture and functionality. While I have not yet submitted a pull request, I have identified areas where I can contribute, particularly in integrating additional atlas-registered datasets for enhanced visualization capabilities.

## Proposal Discussion Link
(https://neuroinformatics.zulipchat.com/#narrow/channel/405740-General/topic/Google.20Summer.20of.20Code/near/505966200)

## Project Proposal

### Title
Add to BrainGlobe's Data Visualization Tools

## Synopsis

The BrainGlobe `brainrender` tool is widely used to visualize brain data within a common coordinate space defined by a "brain atlas." To make this functionality more accessible to users without programming expertise, `brainrender-napari` was developed as a plugin for the `napari` image viewer. However, some publicly available atlas-registered datasets, particularly for mouse and fish brains, are not yet integrated into `brainrender-napari`. This project aims to implement code that enables users to download and visualize these datasets seamlessly within the `brainrender-napari` interface, thereby broadening the tool's applicability and user base.

## Benefits to the Community

By integrating additional atlas-registered datasets into `brainrender-napari`, this project will:

- **Enhance Accessibility:** Allow researchers without programming skills to visualize complex brain data effortlessly.
- **Broaden Applicability:** Support a wider range of species, facilitating comparative studies across different models.
- **Promote Open Science:** Provide open-source tools that encourage collaboration and reproducibility in neuroscientific research.

## Deliverables

1. **Napari Widget Implementation:** Develop a Python-based `napari` widget that facilitates the downloading and visualization of atlas-registered data for mouse and fish brains.
2. **Testing Suite:** Create comprehensive tests to ensure the reliability and accuracy of the new functionalities.
3. **Documentation:** Provide detailed documentation covering the usage, integration, and technical aspects of the new features.
4. **Gallery Example:** Develop an example use case to be included in the `brainrender-napari` gallery, demonstrating the practical application of the new functionalities.

## Technical Approach

1. **Data Source Identification:** Identify and catalog publicly available atlas-registered datasets for mouse and fish brains.
2. **API Integration:** Implement functionality to fetch and download these datasets directly within the `napari` interface.
3. **Visualization Pipeline:** Develop rendering pipelines to accurately display the downloaded datasets, ensuring compatibility with existing `brainrender` functionalities.
4. **User Interface Design:** Design an intuitive UI within `napari` to allow users to select, download, and visualize the datasets seamlessly.

## Timeline

| **Phase**                | **Dates**                | **Planned Tasks & Deliverables**                                             |
|--------------------------|--------------------------|------------------------------------------------------------------------------|
| **Community Bonding**    | May 20 – June 16         | - Engage with the BrainGlobe community and mentors.<br>- Deepen understanding of `brainrender-napari` and its integration with `napari`.<br>- Review relevant atlas datasets and existing visualization tools. |
| **Week 1**               | June 17 – June 23        | - Design the architecture for the `napari` widget.<br>- Begin development of the widget's core functionalities. |
| **Week 2**               | June 24 – June 30        | - Continue widget development focusing on data downloading capabilities.<br>- Implement initial visualization features. |
| **Week 3**               | July 1 – July 7          | - Integrate the widget with `brainrender-napari`.<br>- Conduct preliminary testing and debugging. |
| **Week 4**               | July 8 – July 14         | - Develop comprehensive tests for the new functionalities.<br>- Begin drafting user documentation. |
| **Week 5**               | July 15 – July 21        | - Refine the widget based on testing feedback.<br>- Finalize user documentation and prepare the gallery example. |
| **Week 6 (Final Week)**  | July 22 – July 28        | - Conduct final testing and debugging.<br>- Submit the completed project and present findings to the BrainGlobe community. |

## Expected Outcomes

- A fully functional `napari` widget integrated into `brainrender-napari` that allows users to download and visualize atlas-registered data for mouse and fish brains.
- Comprehensive test coverage ensuring the reliability of the new features.
- Detailed documentation and a gallery example to assist users in utilizing the new functionalities effectively.

## Future Work

- **Support for Additional Species:** Extend the widget's capabilities to include atlas-registered datasets from other species.
- **Advanced Visualization Features:** Implement features such as interactive data exploration and customizable rendering options to enhance user experience.

## Skills Required

- **Essential:**
  - Proficiency in Python programming.
  - Familiarity with version control systems, particularly Git.
- **Desirable:**
  - Experience with data visualization techniques.
  - Experience working with image data.
  - Familiarity with the `napari` image viewer and plugin development.


## Commitment

I am committed to dedicating approximately 30 hours per week to this project. I have no prior commitments during the GSoC period and can allocate the necessary time and effort to ensure the project's success.

## Communication

I plan to maintain regular communication with mentors and the BrainGlobe community through:

- **Weekly Video Calls:** To discuss progress, challenges, and next steps.
- **Zulip Chat:** For daily updates, quick questions, and asynchronous discussions.
- **GitHub Issues/PRs:** To manage tasks, report bugs, and review code collaboratively.

### Project Length
Medium-sized (175-hour) project


## Personal Background

I am Prathamraj Giri, currently pursuing a B.Tech in Computer Science and Cybersecurity. My interests lie in software development, cloud computing, and AI, with a particular enthusiasm for neuroinformatics. I have been actively working on open-source projects and have experience with Python, JavaScript, and cloud-based systems. One of my ongoing side projects involves wildlife tracking and surveillance, utilizing trackers and silent drones to monitor animal activity in protected areas. Through this, I have gained hands-on experience in data collection, integration, and security—skills I believe are highly relevant to the Neuroinformatics Unit's mission. I am particularly interested in contributing to projects that involve data-driven neuroscience, machine learning workflows, and real-time analytics. I look forward to collaborating with the BrainGlobe community and learning from all of you.

### Motivation
The intersection of neuroscience and computational tools is a field that deeply interests me. The opportunity to contribute to the BrainGlobe initiative, particularly by enhancing `brainrender-napari`, aligns with my passion for developing tools that facilitate scientific research. By making complex data more accessible and interpretable, I aim to support neuroscientists in their quest to understand the brain's intricacies.

### Match
My technical background in Python development, coupled with experience in data visualization and user interface design, positions me well for this project. I have a track record of developing plugins and integrating disparate data sources into cohesive visualization tools. My proactive approach to learning and adaptability ensures that I can navigate the complexities of this project effectively.

### Availability
I have no prior commitments during the GSoC period and can dedicate the necessary time and effort to this project. I am committed to meeting deadlines and maintaining open communication with mentors and the community.

## GSoC

### GSoC Experience
This is my first time participating in GSoC. I view this program as an invaluable opportunity to immerse myself in open-source development, contribute meaningfully to a project I am passionate about, and learn from experienced mentors in the field.

### Other Applications
I am exclusively applying to the BrainGlobe project under NIU for GSoC 2025, as it aligns perfectly with my interests and career aspirations.
