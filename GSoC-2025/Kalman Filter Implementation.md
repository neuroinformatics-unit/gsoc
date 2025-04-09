# GSoC 2025 Proposal: Kalman Filter Implementation for NIU's Movement

**Name:** Thao Tran  
**University:** Western Governors University  
**Email:** ttran143@gmail.com  
**LinkedIn:** https://www.linkedin.com/in/thao-tran-/  
**Telephone:** 780 772 7686  
**Country of Residence:** Canada  
**Primary Language:** English  
**Github:** https://github.com/thao-1  
**Credly:** https://www.credly.com/users/thao-tran.6dfe6bb6/edit  

## Personal Background

As a recent computer science graduate with open-source systems and artificial intelligence majors, I gained considerable experience in Python programming, machine learning methodologies, and Linux system administration. While I was a student, I specifically focused on open-source projects and participated in AI-based research projects, which influenced my skills in log analysis, state-space modeling, and time-series data filtering.

I'm currently looking for an internship where I can interact with other people and learn from them and gain more experience. If I am chosen, I can definitely do 40 hours a week's worth of work on the project, and I am willing to do extra work if the project requires it.

I have carried out an extensive review of the NIU movement library and its intention to unify pose-estimation pipelines in open science, and this has resulted in a complete understanding of its benefits, underlying principles, and areas of potential future innovation. In my view, the movement's uncompromising support for free and open-source software, combined with its clear roadmap and emphasis on reproducibility, is of specific interest.

My studies in machine learning and artificial intelligence provided me with in-depth knowledge of various methodologies and algorithms that can be utilized in an intelligent manner in time series smoothing, Kalman filtering, and multi-source trajectory estimation. I am also interested in the research that movement is doing to enable growth in these domains and look forward to working on projects that involve utilizing artificial intelligence for improving data quality, tracking identities, and signal estimation for behavioral neuroscience.

## Why This Project?

The "Kalman Filtering for Data Cleaning in Movement" project interested me because it focuses on a crucial issue in the analysis of behavior data and pose-estimation: enhancing trajectory data reliability and quality. Strong filtering and identification correction techniques are essential with ever-growing dataset sizes and complexity across neuroscience and studies of behavior. This project provides an ideal opportunity to apply machine learning techniques —state-space models like Kalman filters—to solve real-world issues in an open-source, research-based environment.

What I'm most looking forward to is the chance to contribute to a tool with a tangible impact on the scientific community by enhancing data tracking accuracy and value for behavior understanding. I'm most drawn to the movement's goal of building flexible, reproducible workflows within open science, and I consider this project a perfect intersection of my artificial intelligence and time-series modeling technical skills and passion for open-source collaboration in scientific computing.

## Technical Knowledge

I've recently graduated in Computer Science specializing in AI. I've also taken additional courses in AI and programming on Udemy which gave me lots of knowledge regarding AI and open sources. I also finished the Data Science course which I needed to complete 8 projects through WorldQuant University. Please check the projects I have done through WorldQuant University on Credly: https://www.credly.com/badges/5d394740-c3c2-4c24-85bd-2502e2a24fe1/public_url

My technical background includes:

- **Programming Languages:** Proficient in Python, with experience using NumPy, pandas, and xarray for time-series and scientific data analysis.
- **Machine Learning/AI:** Hands-on experience with scikit-learn, PyTorch, TensorFlow, and state-space models (e.g., Kalman filters) for anomaly detection and smoothing.
- **Data Processing:** Strong understanding of working with time-series data, filtering techniques, and model optimization for accurate trajectory and position estimation.
- **Linux & Development Tools:** Comfortable in Linux environments; proficient with Git, CI/CD pipelines, and containerization for reproducible development workflows.

## Project Details

### Project Abstract

The purpose of this project is to add Kalman filtering techniques to the movement library in order to enhance the quality of behavioral data analysis, specifically in pose estimation and trajectory smoothing. The primary task is to use a Kalman filter to smooth position, velocity, and acceleration time-series data, which will address noise and inconsistencies that are typical in behavioral datasets. In addition, the project will solve the issue of identity switches in multi-animal tracking data, aiming to improve the consistency of animal identity across frames.

To this purpose, I will design and implement a robust Python solution by either implementing a Kalman filter from scratch or wrapping a pre-existing Python implementation. The project will be followed by thorough testing, proper documentation, and an example use case demonstrating its utility in real behavioral research. The project will be in accordance with the movement's philosophy of providing reproducible, open-source software augmenting pose-estimation pipelines in neuroscience and behavioral research.

The execution will be focused on modularity, flexibility, and ease of integration in a way that the Kalman filter is easily adapted and applied to numerous data sources and uses throughout the movement ecosystem.

### Technical Details

**Primary Project: Kalman Filtering for Data Cleaning in Movement**

For this project, I will implement and incorporate a Kalman filter to improve the quality of position, velocity, and acceleration time-series data in the movement library. This will minimize data noise, correct inconsistencies in behavioral datasets, and identity-switch issues in multi-animal tracking. The following outlines the approach, architecture, and example code for key components of this project.

**Architecture Overview:**

The project will be modular with the following key components:

- **Kalman Filter Implementation:** Core module to execute Kalman filters on time-series data (position, velocity, acceleration).
- **Identity Correction Module:** Helper module to rectify identity flips in multi-animal tracking data using Kalman smoothing.
- **Data Preprocessing Pipeline:** This handles normalizing and preparing input data before subjecting it to the Kalman filter.
- **Testing Framework:** Ensure the filter implemented works well on various datasets and edge cases.
- **Documentation & Example Use Case:** Thorough guides and examples of how to use the new feature.

**Kalman Filter Implementation:**

The core of this project is to code out the Kalman filter, which will be used to filter time-series data, such as position, velocity, and acceleration. I will either code the filter from scratch or wrap up some existing Python implementation as per requirements.

Kalman filter will be used to filter out noise from tracking data and enhance the precision of continuous-time system estimates. The filter will work efficiently on noisy, partial data, especially for multi-animal tracking.


**Identity Correction Module**

There are identity switches in multi-animal tracking that result in incorrect identity assignments between frames. To address this, I will expand the use of the Kalman filter implementation to track identities by connecting observed positions and propagating according to the filter's state estimate.

The module will take advantage of the ability of the Kalman filter to predict the future state and correct multiple input sources of identity errors.


**Data Preprocessing Pipeline**

The data preprocessing module will prepare the input data for Kalman filtering. This will include normalization, interpolation, and missing value or outlier treatment. It will ensure that the data is in the proper format and range for accurate Kalman filtering.


**Testing Framework**

To ensure that the Kalman filter and associated modules work as expected, I will write a series of unit tests using pytest. The tests will cover edge cases like missing data, identity swaps, and noisy data scenarios.


I already pushed my sample code if you want to check: https://github.com/thao-1/movement-data-cleaning.git

### What I'll Do Next

- I will proceed from here after getting feedback from NIU's mentors by finishing the Kalman filter design and optimizing it for different datasets.
- Then, I will implement additional filtering methods for multi-animal tracking and identity correction. The filter performance will be optimized for real-time behavioral research applications.
- I will create a comprehensive test suite to ensure stability and functionality, along with thorough documentation of the new features afterward.
- Finally, I will add an example use case in the movement gallery to demonstrate the value of Kalman filtering for data cleaning of behavioral data.

## Enhanced Project Ideas for Kalman Filter Integration in Movement

Apart from the goal I outlined for this project, I will follow additional improvements that not only enhance the Kalman filtering capabilities but also make them more beneficial to the broader community of behavioral and neuroscience researchers.

**Federated Filtering for Collaborative Data Enhancement**

Develop a privacy-preserving solution where multiple research institutions or labs collaborate to improve tracking information using Kalman filters without sharing sensitive information. Each institution would operate on a local basis, apply the Kalman filter to improve tracking quality, and share aggregated updates (model parameters or filtered outputs) only. This ensures data privacy and yet exploits collective wisdom.

**Contextual Trajectory Correction Engine**

Enlargen the Kalman filter to detect and correct interdependencies in position, speed, and acceleration data from different sources, e.g., different cameras or tracking systems. Using graph-based or probability-based methods, the system can identify and resolve conflicts between multiple data streams, making trajectory estimates more accurate and helping scientists to synchronize results from multiple tracking systems.

**Interactive Feedback Loop for Filtering Optimization**

Develop a user interface or CLI program by which researchers can provide feedback on the Kalman filter output (e.g., false tracking or filtering corrections). This feedback would be used to update the model in real time, progressively improving its accuracy. Researchers could mark false positives (e.g., incorrectly smoothed data) or negatives, and the system would use this feedback to dynamically update its filtering parameters.

**Integration with Pose Estimation Frameworks (DeepLabCut, SLEAP)**

Integrate the Kalman filter implementation with popular pose-estimation libraries like DeepLabCut or SLEAP. By providing plug-and-play functionality with these libraries, researchers can seamlessly apply Kalman filtering to their time-series tracking data. Such integration would facilitate the use of the movement library within real-world experiments and encourage its usage in complex tracking scenarios.

**Explainable Kalman Filtering for Data Transparency**

Insert explainability features so that researchers can view how the Kalman filter is making its corrections. For example, add a feature that signals the reason behind each correction (e.g., the percentage of the correction based on the previous state relative to the current noisy measurement). This transparency would allow researchers to believe and fine-tune the filtering process, especially in high-stakes uses where accuracy counts.

**Collaborative Data Validation and Benchmarking**

Develop a community platform through which users of the movement library can share their filtered datasets for benchmarking performance. This platform could use the output of the Kalman filter as a reference to compare different configurations or techniques for data cleaning so that the research community can confirm the effectiveness of their tracking systems.

## Timeline

**Pre-GSoC: Preparation**
- Read the movement library and its existing data structures.
- Familiarize oneself with Kalman filters, with a focus on their application to time-series data, i.e., position, velocity, and acceleration smoothing.
- Familiarize oneself with pose estimation pipelines like DeepLabCut and SLEAP, and the corresponding workflows for tracking and data analysis.
- Set up the development environment (Python, Git, any necessary libraries like NumPy, xarray, pytest).
- Learn the movement repository and contribution practices.

**Week 1-2: Research and Setup**
- Finalize architecture design of Kalman filter integration to movement.
- Define primary components: Preprocessing data, implementation of Kalman filter, multi-animal identity compensation, and integration with existing workflows.
- Define project repository organization and documentation scheme
- Define the configuration system for input data types, filter options, and results.
- Add a Continuous Integration/Continuous Deployment (CI/CD) pipeline to maintain code quality and testing.

**Week 3-4: Core Implementation - Kalman Filter**
- Implement a basic Kalman filter for smoothing the position, velocity, and acceleration time series.
- Gradually start from minimalist implementation to enhance performance and accuracy.
- Add preprocessing pipeline for handling input data (time-series, noise filtration, etc.) and preprocessing data before Kalman filtering.
- Implement a unit test framework using pytest to ensure the Kalman filter and preprocessing functions are stable.
- Display filter run on example DeepLabCut or SLEAP data.

**Week 5-6: Multi-Animal Identity Correction and Optimizations**
- Implement the Multi-Animal Kalman Filter to fix identity flips in multi-animal tracking data.
- Apply the Kalman filter to smooth out tracks and eliminate identity errors between tracking sources.
- Test the Kalman filter on real datasets from multi-animal tracking (e.g., from DeepLabCut or SLEAP output).
- Enhance the data preprocessing pipeline to support different input formats (e.g., integration with xarray for multi-dimensional time-series data).

**Week 7-8: Integration and Testing**
- Port the Kalman filter into the movement library, with support for existing tools and workflows.
- Implement unit tests and integration tests to ensure the Kalman filter works on different datasets and scenarios.
- Enhance the performance of the Kalman filter on large data (guarantee that the filter operates well for a range of different animal quantities and time-series sizes).
- Create example scripts and cases to demonstrate the behavior of the Kalman filter in the movement gallery.

**Week 9-10: Documentation and Sample Usage**
- Complete user-consumable documentation to outline Kalman filter's usage and implementation.
- Insert installation guide, API documentation, and sample usages.
- Provide detailed explanations of Kalman filter parameters (e.g., noise covariances, process models).
- Provide complete example usage scripts demonstrating how the Kalman filter can be applied to time-series tracking data on community-provided example datasets.

**Week 11-12: Finalization and Advanced Features**
- Implement any advanced features based on community feedback or other stretch goals (e.g., more sophisticated Kalman filter implementations, improved multi-animal tracking).
- Conduct intense performance testing and tuning to ensure the system works with large-scale tracking datasets.
- Develop a training pipeline for parameter optimization of Kalman filters using experimental datasets and infer evaluation metrics.
- Finish all documentation, including informative user guides and API documentation.
- Release the completed project as a GitHub release, with installation, usage, and sample case guides.

**Post-GSoC: Future Work**
- Explore Federated Learning to optimize Kalman filter performance without privacy loss between research institutions.
- Expand Kalman filter functionality towards more advanced pose estimation systems and multi-modal sensing sources.
- Work together on ongoing development on the movement library, assisting in bringing more advanced filtering techniques and further enhancements.

## Outcome

Upon completion of this program, I will deliver:

**Kalman Filter Integration into Movement Library**
- Complete source code for Kalman filter implementation within movement repository in GitHub.
- Extensive documentation, including installation instructions, usage instructions, and configuration details for deploying Kalman filters on time-series tracking data (position, velocity, acceleration).
- Example usage cases demonstrating how to use Kalman filters with data from DeepLabCut, SLEAP, and other pose-estimation systems.
- Unit testing and integration testing to ensure the stability and accuracy of the Kalman filter code on various datasets and tracking scenarios.
- Extensible or adaptable modularized Python code for any eventual filtering and trajectory adjustment needs.

**Multi-Animal Tracking Enhancements**
- Kalman filter code for multi-animal tracking to mitigate identity switches and improve trajectory estimations across animals.
- API documentation explaining how to utilize multi-animal tracking capabilities and incorporate them into user-dependent workflows.
- Performance optimization for handling larger tracking datasets so that it can scale for multi-animal tracking applications.

**Documentation and Tutorial Materials**
- Comprehensive documentation such as:
  - How to port the Kalman filter to existing pose estimation projects.
  - Detailed explanation of Kalman filter parameters, how-to guides, and how to tailor them.
  - Example scripts that demonstrate common workflows, e.g., filtering and correcting tracking data from pose-estimation pipelines.
  - Tutorial guides for researchers explaining how to use the Kalman filter on their own data analysis needs.
  - Tutorials or videos for the community on how to apply and use the Kalman filter in their own experiments.

**Additional Contributions to the Movement Library**
- A GitHub repository containing the complete project code, with simple installation and integration instructions.
- Discussion of future additions to the Kalman filter, as proposed by the community and as volunteered contributions.
- Community contributions such as discussions, pull requests, and proposals to increase Kalman filtering functionality or to integrate it with other tracking infrastructures.

**Overall Outcomes**
- Test suite for ensuring correctness and validity of the Kalman filter, especially against noisy data as well as across multiple animals.
- Evaluating criteria used to determine the efficiency of the Kalman filter against tracking-related activities.
- Suggestions for future improvements to the movement library, namely on data filtering, multi-animal tracking, and algorithmic optimization.
- Documentation for developers who are interested in learning about or extending the Kalman filter implementation.
- Materials for demonstrating at appropriate conferences, workshops, or community events, enabling researchers to apply the solution in their research.

## Personal Motivation

I'm really excited at the possibility of being able to contribute to the Neuroinformatics Unit (NIU) and collaborate with the team on this GSoC project. I'm eager to be able to assist the movement's vision of enhancing pose-estimation pipelines through the application of Kalman filters to improve data-cleaning performance. This project is an excellent opportunity for me to learn, grow, and be able to contribute to something meaningful that will enable researchers to get the most out of their data.

I appreciate the commitment of NIU to open-source development and its impact on the research community. Being able to collaborate with experienced mentors and developers in this community is something I'm particularly thrilled about. This project is the perfect opportunity to collaborate with like-minded individuals while learning from the experience and wisdom of the team. The sense of community and shared purpose at NIU is something I highly value.

What I'm most excited about is being able to contribute to tools that will have a direct impact on neuroscience research for years to come. The ability to help researchers by streamlining data-cleaning protocols and tracking mechanisms is something that I am very passionate about. I believe our efforts here will continue to evolve well beyond GSoC, and that's what it's so valuable to me.

For me, Google Summer of Code will be an amazing experience to grow both personally and professionally. I consider it an opportunity to form long-term connections with the NIU team while learning on a project that will be far-reaching. The guidance and criticism received from mentors and other contributors will help me grow, and I am gladly willing to go the extra mile and work the hours necessary to deliver a superior product.

It's the technical sophistication and the potential to reach out into the real world in the research community that make this project so interesting. I'm approaching this GSoC not just as an opportunity to write code but as the beginning of what I hope to be a long-term relationship with the NIU community, and I'm excited to see where this takes me.

## Previous Experience:

I've worked on several projects that are directly relevant to this GSoC proposal:

1. **AI-Powered Log Analysis Dashboard**  
   (Github link: https://github.com/thao-1/AI-Powered-Log-Analysis-Dashboard-Project.git)
   - Employed sophisticated machine learning techniques with scikit-learn to implement anomaly detection and clustering algorithms, using strong data science and algorithmic problem-solving capabilities.
   - Built a complete data pipeline from log ingestion and preprocessing to visualization, demonstrating proficiency in Python, pandas, and data transformation operations.
   - Designed and built an interactive web dashboard using Dash and Plotly, including front-end development skills and the ability to create readable data visualizations on complex data sets.

2. **RAG-Chatbot-for-Patient-Info**  
   (Github link: https://github.com/thao-1/RAG-Chatbot-for-Patient-Info.git)
   - Utilized the Retrieval-Augmented Generation (RAG) model through LangChain, FAISS vector database, and OpenAI embeddings to construct a context-aware medical info chatbot
   - Constructed end-to-end full-stack application with FastAPI backend and responsive front-end, emphasizing real-time question answering with source attribution
   - Designed strong data processing pipeline for medical information with custom document loaders, text chunking, and optimized vector similarity search

3. **Telco-Customer-Churn**  
   (Github link: https://github.com/thao-1/Telco-Customer-Churn.git)
   - Machine Learning Pipeline Development: Implemented an end-to-end ML solution using Random Forest classification with 79% accuracy, including data preprocessing, model training, and evaluation.
   - API Development with FastAPI: Implemented a production-grade REST API with robust input validation, error handling, and health checks for reliable model serving.
   - Software Engineering Best Practices: Demonstrated clean code architecture with modular design, proper logging, environment variable configuration, and adequate documentation.

4. **Build-a-multi-agent-system-with-Autogen**  
   (Githhub link: https://github.com/thao-1/Build-a-multi-agent-system-with-Autogen-.git)
   - Advanced LLM Integration: Designed a very sophisticated natural language to SQL conversion system based on OpenAI's GPT models, demonstrating expertise in prompt engineering and API integration for complex language understanding tasks.
   - Multi-Database Architecture: Designed a flexible system that supports SQLite, MySQL, and PostgreSQL dialects, demonstrating database architecture expertise and SQL familiarity across different database management systems.
   - Solid Evaluation Framework: Created effective evaluation metrics (Execution Accuracy, R-VES, Soft F1-Score), achieving 100% execution accuracy and 88.84% efficiency rates, demonstrating sound analytical skill and performance optimization care.

If you want to check all of my projects, which I pushed to Github, please follow this link: https://github.com/thao-1?tab=repositories)

## References
- https://www.mathworks.com/help/matlab/ref/kalman.html
- https://neuroinformatics.dev/get-involved/gsoc/projects_2025/movement.html
- https://www.neuroinformatics.org