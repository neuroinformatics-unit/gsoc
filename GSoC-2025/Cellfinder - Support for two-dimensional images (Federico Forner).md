## Cellfinder: Improve classification algorithm (Federico Forner)

## Personal details

- **Full name**: Federico Forner
- **Email**: federico.forner.f@gmail.com
- **GitHub username**: Fede2717
- **Zulip username**: Federico
- **Location & time-zone**: Rome, Italy (UTC+1)
- **Personal website / project portfolio**: [LinkedIn](https://linkedin.com/in/federico-fo)

### Code contribution

- [Pull Request #464 on brainglobe/cellfinder](https://github.com/brainglobe/cellfinder/pull/503#issue-2956706833) – expose GPU/CPU choice and other parameters to pytorch cellfinder version

### Proposal discussion link

(https://github.com/neuroinformatics-unit/gsoc/pull/59#issue-2972616901)

## Project proposal 

- **Synopsis**
Cellfinder currently relies on three-dimensional pipelines for detecting and classifying cells in whole-brain images. However, many neuroscientists capture data as two-dimensional brain slices. This project will extend Cellfinder’s functionality to 2D images by refactoring its 3D pipeline and implementing a dedicated 2D neural network, ensuring consistent behavior across different dimensional inputs. Specifically, I will adapt the image processing code to robustly handle both 2D and 3D data and implement a new neural network architecture optimized for classifying cell candidates in two-dimensional slices. By broadening Cellfinder’s capabilities, the neuroscience community (often working with 2D slices) will be able to leverage the tool’s automated cell detection and classification features more effectively.

Goals and Deliverables
1. Modified blob detection algorithm: Update the existing 3D pipeline to handle 2D image slices. This includes adjusting parameter settings and ensuring correct labeling of cell candidates in 2D vs. 3D.  
2. New 2D CNN: A Python-based neural network (e.g., a 2D ResNet or EfficientNet) for classifying 2D cell candidates.  
3. Tests: Thorough unit and integration tests covering all new functionality.  
4. Documentation: Updated user guides explaining how to train, fine-tune, and use the 2D pipeline.  
5. Blog Post: A technical write-up demonstrating the 2D workflow and comparing its performance to the current 3D approach.


### **Implementation Timeline**

I plan to dedicate approximately 30 hours/week. Recognizing that adapting the blob detection code and develop a new 2D CNN will be more time-consuming, I will allocate extra effort there early on.

| **Phase**                          | **Tasks**                                                                                                                                                                                                                                                                                               |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Community Bonding** (4 weeks) | - Familiarize with Cellfinder’s current 3D pipeline. <br/> - Explore suitable 2D CNN architectures (e.g., ResNet, EfficientNet). <br/> -  Discuss approach with mentors. <br/> - Review BrainGlobe development guidelines. <br/> - Gather and examine training data for 2D slice experiments. |
| **Week 1–3**                       | - Refactor the existing pipeline to handle both 2D and 3D inputs, ensuring correct integration with cellfinder’s pipeline. <br/> - Implement basic tests to confirm cell candidate detection works consistently for 2D/3D.                                                                                      |
| **Week 4–5**                       | - Begin implementing a 2D CNN classifier (e.g., ResNet or EfficientNet). <br/> -Set up an initial training loop and consider basic data augmentation.                                               |
| **Week 6–7**                       | - Finish any pending tasks (e.g., unresolved implementation details). <br/> - Train and fine-tune the 2D classifier on sample data (adjust batch size, learning rate, augmentations). <br/> - Begin writing tests for the classifier (data flow, forward pass, etc.).                 |
| **Week 8–9**                       | - Continue refining the 2D architecture based on mid-phase results. <br/> - Conclude testing tasks. <br/> - Evaluate the network in terms of accuracy and speed (precision-recall for cell vs. no-cell detection, and inference speed) and, if necessary, implement improvements. <br/> - Begin drafting the blog post or user-facing documentation. |
| **Week 10–11**                      | - Continue refining the technical blog content. <br/> - Conclude user-facing documentation. <br/> - Prepare any performance benchmarks for inclusion in the blog post.                                                                                 |
| **Week 12**                     | - Finalize all code, ensuring extensive test coverage. <br/> - Publish the blog post, including relevant performance observations. <br/> - Merge PRs, address mentor feedback, and prepare for project conclusion.    


Note on availability:

- If I take a 1-week vacation between Weeks 9 and 11, I will compensate by working ahead or shifting tasks as needed.

- **Communication plan**

I propose to organize communication as follows:

- Asynchronous updates on Zulip, approximately 2–3 times per week, or whenever I complete a new step, need feedback, or encounter a relevant issue. This way, the mentor will always be updated on my progress.

- Check-in call,  (via Meet, Zoom, or similar platforms) approximately once every 10–14 days, preferably when I complete or start working on a key part of the project, or in case of particularly complex problems. These meetings will allow us to review results, address any difficulties, and plan the next steps.

However, I remain flexible regarding the frequency and format of meetings, depending on the mentor’s availability and the needs of the project. If an additional call or more frequent updates on Zulip are needed, I’ll be happy to adapt to ensure better communication.

## Personal statement

- **Past experience.** 
I am a second-year undergraduate student in Mathematical Sciences for AI at Sapienza University of Rome. My coursework includes linear algebra, calculus, fundamentals of neuroscience, machine learning, and optimization (the latter two to be completed by the end of May).I have built some deep-learning demos in Python (NumPy, PyTorch), mainly focused on image classification tasks. Although I am relatively new to open source, I have already contributed to cellfinder (issue #464) and have rapidly learned to use Git, GitHub, and Zulip. In parallel, I have explored theoretical aspects of machine learning—including backpropagation, neural net (like CNNs, and RNNs)—and I am continuously deepening my knowledge of PyTorch and deep learning frameworks.

- **Motivation: why this project?**
This project offers a unique chance to make a practical impact by extending cellfinder’s capabilities to a broader range of neuroscience data. Supporting 2D brain slice images addresses a concrete need for cellfinder and presents an engaging challenge that involves both the modified implementation of the image processing pipeline and the design of a dedicated neural network for 2D classification. I’m particularly interested in combining neuroscience with machine learning, and this project would allow me to deepen my skills while contributing to an open-source tool that supports real-world neuroscience research.

- **Match: why you?**
I am very driven and enthusiastic about taking on new challenges with determination. Over the past few weeks, I have immersed myself in understanding cellfinder’s codebase, resolved a beginner-friendly issue, and explored neural network for images. My strong quantitative background in mathematics and computer science, combined with my commitment to continuous learning and adaptability, makes me confident in my ability to contribute effectively to enable cellfinder to work with 2D images as well.

- **Availability**
From June onward, I plan to dedicate around 30 hours per week to the GSoC project. Although I may have exams in June/July, I will prioritize GSoC tasks and manage my schedule accordingly (potentially sitting exams at alternative dates). I might take a one-week vacation in August, but I will coordinate with mentors to ensure minimal disruption by either working ahead or making up for any missed time.

## GSoC

- **GSoC experience**

Participating in GSoC offers a distinct opportunity to test my abilities by addressing real-world challenges and making a meaningful impact through an open-source project like Cellfinder. I am enthusiastic about collaborating with skilled mentors on an initiative that benefits the neuroscientific community. Along the way, I plan to elevate my proficiency in testing, documentation, and continuous integration practices. Moreover, I am excited to develop practical solutions, track my progress, and actively share insights with the community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

Yes, I have also submitted a proposal for another BrainGlobe-related project. However, I am fully committed, with a strong determination to deliver all features and documentation for whichever project I am accepted to.

*Thank you for considering my application! I look forward to collaborating with the NIU community and mentors on cellfinder.*