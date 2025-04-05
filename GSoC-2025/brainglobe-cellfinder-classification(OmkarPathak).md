

## Brainglobe: Cellfinder Classification (Omkar Pathak)



## Personal details
Please include the following information:
- **Full name** Omkar Pathak
- **Email** pathak.omkar@gmail.com  
- **GitHub username** omk42
- **Location & time-zone** Washington State, USA (PST)
- **Personal website / project portfolio** https://omk42.xyz
- **Code contribution**

    1. PasteOnEth open source project- https://pasteoneth.com/ 

    Independently created a DApp to host code snippets on Ethereum compatible chain, featuring Metamask wallet integration. Pastes are OpenZeppelin ERC1967Proxy behind a UUPSUpgradeable smart contract implementation. Successfully deployed on Sepolia testnet with 10+ active and pseudonymous users.

    Solo contributer on all repos below- 
    - https://github.com/PasteOnEth/PasteOnEthChain
    - https://github.com/PasteOnEth/PasteOnEthWeb

    2. CloudStation contribution

    Contributed to a CloudStation research project that is a cloud-based ground control station for Ardupilot drones. The web app is designed to be easily scalable so users can control multiple drones at the same time. As part od this PR, I onboarded AWS CloudDeploy, a deployment service that automates application deployments to Amazon EC2 instances, to the project so that web-based application can be full CI/CD. 


    - https://github.com/CloudStationTeam/cloud_station_web/pull/10
    
    

- **Proposal discussion link**
    TBD

## Project proposal 

- **Synopsis**

   This project is focused on significantly improving the deep learning classifier utilized in the BrainGlobe cellfinder tool, which is designed to detect and analyze cells within large-scale brain microscopy images. Currently, the architecture relies on ResNet, a well-established model; however, given the rapid advancements in deep learning technologies, exploring alternative architectures could yield superior performance outcomes.

    **Why cellfinder?** The ability to accurately detect and map cells in three-dimensional mammalian brain images is crucial for advancing our understanding of brain function and facilitating developments in the field of neuroscience. The traditional method of manual segmentation is not only labor-intensive and time-consuming but also susceptible to variability based on the individual expertise.

    **Why this project?** By investigating and implementing alternative deep learning techniques, we can potentially surpass the performance of the existing architecture, ResNet, which, while effective, may not fully leverage the latest advancements in deep learning. Alternatives such as EfficientNet, which optimizes both accuracy and computational efficiency, or Vision Transformers (ViTs), which have shown remarkable performance in image classification tasks, could be explored. These models can provide better feature extraction capabilities and improved generalization, leading to faster, more robust, and ultimately more reliable cell detection and classification for neuroscientists. This can be achieved by systematically addressing the limitations of the current approach, enhancing the dataset through the application of both existing models and generative models, experimenting with single input channel usage, and striving to minimize false positives as much as possible. The goal is to evaluate and integrate state-of-the-art models, ensuring that cellfinder remains at the forefront of technology and continues to provide significant value to neuroscience research.

    **The Open-Source Community Benefits:**
    1. Collaborative Development: This project encourages collaboration among developers, researchers, and data scientists, fostering a community-driven approach to improving the tool.
    2. Knowledge Sharing: By documenting the development process and results, the project will serve as a valuable resource for others looking to implement similar deep learning techniques in their own projects.
    3. Increased Visibility: Enhancements to the cellfinder tool can attract more contributors and users, increasing the project's visibility and encouraging further innovation within the community.
    4. Educational Resources: The project can provide tutorials, example use cases, and best practices, helping newcomers to the field of deep learning and neuroscience to learn and contribute effectively.
    5. Interoperability: By adhering to open standards and practices, the project can facilitate integration with other tools and frameworks, enhancing the overall ecosystem of neuroscience research tools.
    6. Enhanced Tools: By improving the accuracy and speed of cellfinder, we can accelerate brain research efforts globally, making significant contributions to the field.
    7. Reproducible Benchmarks: Providing clear comparisons between models will assist researchers in selecting the most suitable architectures for similar tasks, fostering a more efficient research environment.
    8. Extensible & Well-Documented Code: The project will produce code that is not only extensible but also well-documented, ensuring it aligns with the rapid advancements in deep learning.
    

- **Implementation timeline**

    - **Minimal set of deliverables:**
        - A Python implementation of at least one new Deep Learning network architecture in cellfinder.
            - **Success Criteria:** The new architecture should be integrated into the existing cellfinder tool and should be able to process input data without errors. It should demonstrate improved performance metrics compared to the current architecture.
        - Quantitative comparison between the current and new architecture.
            - **Success Criteria:** A comprehensive report detailing the performance metrics (accuracy, precision, recall, F1 score) of both architectures on the same dataset, showcasing the improvements achieved with the new architecture.
        - Tests to cover any added functionality.
            - **Success Criteria:** Unit tests should be written and successfully pass for all new functionalities, ensuring that the new architecture behaves as expected and does not introduce any regressions in existing features.
        - Documentation for the new functionality.
            - **Success Criteria:** Clear and concise documentation should be provided, including installation instructions, usage examples, and API references, ensuring that users can easily understand and utilize the new features.
        - Integration with existing workflows:
            - **Success Criteria:** Ensure that the new architecture can be seamlessly integrated into existing workflows within the cellfinder tool, allowing users to switch between architectures without significant changes to their current processes.
        
    
    - **Stretch goals:**
        - User feedback mechanism:
            - **Success Criteria:** Implement a feedback mechanism to gather user insights on the new architecture's performance and usability, which can guide future improvements and iterations.
        - A blog explaining the new network and its advantages and disadvantages.
            - **Success Criteria:** A well-structured blog post should be published on a relevant platform, detailing the design choices, performance comparisons, and potential use cases of the new architecture, aimed at educating the community and encouraging feedback.
            - **Additional Stretch Goal:** Create a tutorial or video series demonstrating the implementation and usage of the new architecture, aimed at helping users understand its benefits and applications.



    | **Week** | **Tasks and Milestones**                                                                                     | **Hours per Week** |
    |----------|--------------------------------------------------------------------------------------------------------------|---------------------|
    | Week 1  | - Conduct a literature review on alternative deep learning architectures (EfficientNet, ViTs).             | 15                  |
    |          | - Begin initial implementation of the selected architecture in the cellfinder tool.                         |                     |
    |          | - Set up the development environment and ensure existing codebase is functional.                            |                     |
    | Week 2  | - Complete the implementation of the new architecture.                                                      | 15                  |
    |          | - Start testing the new architecture with sample datasets.                                                  |                     |
    |          | - Document the implementation process and initial findings.                                                  |                     |
    | Week 3  | - Perform quantitative comparisons between the current ResNet architecture and the new architecture.        | 15                  |
    |          | - Analyze performance metrics (accuracy, precision, recall, F1 score) and document results.                 |                     |
    | Week 4  | - Write unit tests for the new architecture to ensure functionality and prevent regressions.                | 15                  |
    |          | - Begin drafting documentation for the new functionality, including installation and usage instructions.   |                     |
    | Week 5  | - Integrate the new architecture into existing workflows within the cellfinder tool.                        | 15                  |
    |          | - Ensure seamless switching between architectures for users.                                                |                     |
    | Week 6  | - Mid-term evaluation: review progress and gather feedback from mentors.                                    | 15                  |
    |          | - Refine the implementation based on feedback and testing results.                                          |                     |
    | Week 7  | - Implement a user feedback mechanism to gather insights on the new architecture's performance.             | 15                  |
    |          | - Start drafting a blog post explaining the new architecture and its advantages.                            |                     |
    | Week 8  | - Finalize the blog post and prepare for publication.                                                      | 15                  |
    |          | - Create a tutorial or video series demonstrating the implementation and usage of the new architecture.    |                     |
    | Week 9  | - Conduct final testing and validation of the new architecture with various datasets.                       | 15                  |
    |          | - Document any remaining features and finalize all documentation.                                           |                     |
    | Week 10 | - Prepare a comprehensive report detailing the project outcomes and performance comparisons.                 | 15                  |
    |          | - Ensure all code is well-documented and adheres to open-source standards.                                  |                     |
    | Week 11 | - Freeze the code and complete any remaining tests or documentation.                                        | 15                  |
    |          | - Prepare for final submission and review with mentors.                                                    |                     |
    | Week 12 | - Submit the final report and all deliverables.                                                             | 15                  |
    |          | - Reflect on the project and gather insights for future improvements.                                       |                     |

- **Communication plan**

    I dont have a solid preference and can work with the mentor to identify the right cadence for meetings. Nonetheless, I will provide daily offline updates and schedule time to address any blockers. 

## Personal statement


- **Past experience.** 

    My programming experience spans various roles and technologies. At Amazon Web Services, I was a founding member of a hardware digitalization team, designing BPMN workflows that led to significant cost savings and reduced power demands. I also bootstrapped EC2 micro-services and implemented heuristics to enhance part allocations, exceeding a VP goal for repair efficiency. Previously, as a Software Engineer intern at Google, I developed an automated system on Google Cloud Platform for evaluating encoded videos for Google Nest devices, achieving a 95% reduction in test durations, and built end-to-end data pipelines using Python.

    I have a solid background in open source development, contributing to CloudStation, a cloud-based Ground Control System for drones, which set a world record for long-distance piloting. I co-authored a research paper on this project published in the IEEE Journal. Additionally, I contributed to the Digital Waste Bins project, developing software to display carbon footprints, and initiated CodeDeliver, a web application for managing software distribution. My independent open source project, PasteOnEth, allows users to host code snippets on the blockchain.

    My research at the Computational Vision Lab at UCI involved generating a synthetic dataset of shoe outsole tread, leading to an honor thesis. I also served as a Lead Mentor for AI at UCI, organizing workshops and discussions. As a UROP Fellow, I built a data-driven irrigation system and presented my findings at the UROP Symposium. 
    
    These experiences showcase my programming skills, active involvement in impactful open source projects, and research capabilities, all of which are highly relevant to this project.

- **Motivation: why this project?**

    I am interested in the cellfinder Deep Learning project because it provides an opportunity to deepen my expertise in Deep Learning by implementing a new network architecture, building upon my existing foundation in machine learning and prior work with Convolutional Neural Networks and ML-based perceptual encoding. My strong Python programming skills honed through projects like CloudStation, Digital Waste Bins, and data pipelines at Google are directly applicable to the implementation tasks. The requirement for quantitative evaluation aligns with my background in Computer Science and Statistics, and contributing to this open-source project would allow me to further my involvement in collaborative development. Furthermore, the project allows me to leverage my experience with image data and technical documentation and communication, while also offering a chance to expand my knowledge in popular Deep Learning frameworks.

- **Match: why you?**

    My experience aligns well with the requirements for the Deep Learning network architecture implementation role due to my strong Python programming skills demonstrated in projects like CloudStation, Digital Waste Bins, and Google data pipelines. I possess an understanding of machine learning algorithms, including training a classification model and implementing a Boosted Decision Tree, and have worked with concepts relevant to deep learning through training a ConvNet and ML-based perceptual encoding at Google. My direct experience with image data from the Computational Vision Lab and Google is particularly relevant, and my history of open source contributions and experience with documentation and communication through publications further solidify my suitability for this project.
    
- **Availability**

    I dont have any conflicting commitments. 

## GSoC

_Length: max 0.25 page_

- **GSoC experience**

    I expect the program to provide me with valuable mentorship and guidance as I work on implementing a new network architecture for the cellfinder project. I look forward to collaborating with experienced developers and gaining insights into best practices in deep learning and open-source development. Additionally, I hope to enhance my technical skills, contribute meaningfully to the project, and engage with a community of like-minded individuals who are passionate about advancing research in this field.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    Yes, im applying to HIC humanities projects. I believe i'm aligned to this project more.