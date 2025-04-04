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

(https://github.com/neuroinformatics-unit/gsoc/pull/38#issue-2961522261)

## Project proposal 

- **Synopsis**
Cellfinder currently relies on a ResNet-based classifier to distinguish true cells from non-cells in large, 3D whole-brain images. However, deep learning architectures have significantly advanced since ResNet’s introduction. The project aims to replace the current ResNet-based classifier in Cellfinder with at least one modern 3D deep learning architecture. I will start considering EfficientNet 3D and a ResNet variant (e.g., SEResNet, ResNeXt, ResNet-RS), as these architectures are expected to provide a better speed–accuracy trade-off than the current ResNet baseline. If time permits, I will also explore a 3D Transformer-based approach or a U-Net variant, to further investigate potential gains in accuracy, even though these alternatives tend to be slower and more computationally demanding. The project will also include writing tests, creating user-friendly documentation, and publishing a technical blog post to share the results with the community. A more modern or faster model can help neuroscientists reduce false positives, increase detection speed, and train more efficiently on large volumetric datasets. By merging the new code, tests, and documentation into the open-source cellfinder repository, this work will directly benefit the BrainGlobe community and strengthen the ecosystem for high-throughput neuroscience research. 

Goals and deliverables: (1) integration of at least one novel deep learning architecture in cellfinder; (2) quantitative comparison with the current ResNet classifier, including metrics such as accuracy, F1-score, and inference speed; (3) unit and integration tests for the added functionality; (4) updated documentation on usage, training, and fine-tuning; (5) a blog post presenting the new architecture and analyzing its strengths and limitations.

- **Implementation timeline**

I plan to dedicate \~30 hours/week over 12 weeks, prioritizing thorough model development and testing. Documentation and comparison come later but remain essential final deliverables.

| **Phase**                       | **Tasks**                                                                                                                                                                                                                                                                                                                                                       | **Notes**                                                                                                                                  |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Community Bonding** (4 weeks) | - Explore modern 3D CNN architectures (e.g., EfficientNet V2 (3D), SEResNet (3D), ResNeXt (3D), ResNet-RS (3D)), if time permits, assess a 3D Transformer or U-Net.- Discuss approach with mentors- Gather and examine training data- Finalize model choice and project plan based on feasibility and mentor feedback- Familiarize with the cellfinder codebase and study BrainGlobe “Development guidelines for specific languages and frameworks” | Emphasis on background research, codebase familiarity, and planning.                                                                       |
| **Week 1–2**                    | - Implement the chosen architecture(s) in PyTorch, ensuring correct integration with cellfinder’s pipeline- If feasible, prototype multiple architectures in parallel (starting with EfficientNet 3D and one of SEResNet (3D), ResNeXt (3D), ResNet-RS (3D))- Set up an initial training loop and consider basic data augmentation                                                                                    | Heavy coding work to establish a functional model pipeline.                                                                                |
| **Week 3–4**                    | - Write initial tests to check performance and reliability- Finish any pending tasks from Weeks 1–2 (e.g., unresolved implementation details)- Refine hyperparameters (batch size, LR) and validate performance on sample data                                                                                                                                  | Maintain test coverage early for code quality. Ensure stable training and correct data flow.                                               |
| **Week 5–6**                    | - Compare the new model(s) with ResNet in terms of accuracy, F1-score, inference speed, and resource usage- Adjust hyperparameters as needed (regularization, augmentation)- Decide whether to implement a second architecture based on time/resources                                                                                                          | Mid-term milestone: gather key metrics, refine or expand the approach.                                                                     |
| **Week 7–8**                    | - If time allows, implement a second architecture (e.g., DenseNet3D)- Otherwise, continue development/improvement based on mid-term results- Possibly begin planning or drafting documentation and blog                                                                                                                                                         | Further iteration and improvements based on comparison outcomes.                                                                           |
| **Week 9–10**                   | - Draft user-facing documentation (usage, training, fine-tuning)- Continue or refine the technical blog post detailing approach and results- Make any minor performance tweaks if necessary                                                                                                                                                                     | Focus shifts to documentation and knowledge transfer. If I take a short vacation here, tasks can be redistributed beforehand or afterward. |
| **Week 11–12**                  | - Final code refinements and thorough test coverage- Complete and publish the blog post- Merge PRs, finalize comparisons vs. ResNet, and address any mentor feedback                                                                                                                                                                                            | Code freeze, polishing, and final release. Buffer for unplanned delays or minor bug fixes.                                                 |

Note on availability:

- If I take a 1-week vacation between Weeks 9 and 11, I will compensate by working ahead or shifting tasks as needed.
- "The implementation and validation of new architectures on real 3D data will likely require more time compared to later tasks such as comparison, documentation, and blog writing, and the timeline is structured accordingly."

- **Communication plan**

I propose to organize communication as follows:

- Asynchronous updates on Zulip, approximately 2–3 times per week, or whenever I complete a new step, need feedback, or encounter a relevant issue. This way, the mentor will always be updated on my progress.

- Check-in call,  (via Meet, Zoom, or similar platforms) approximately once every 10–14 days, preferably when I complete or start working on a key part of the project, or in case of particularly complex problems. These meetings will allow us to review results, address any difficulties, and plan the next steps.

However, I remain flexible regarding the frequency and format of meetings, depending on the mentor’s availability and the needs of the project. If an additional call or more frequent updates on Zulip are needed, I’ll be happy to adapt to ensure better communication.

## Personal statement

- **Past experience.** 
I am a second-year undergraduate student in Mathematical Sciences for AI at Sapienza University of Rome. My coursework includes linear algebra, calculus, fundamentals of neuroscience, machine learning, and optimization (the latter two to be completed by the end of May).I have built some deep-learning demos in Python (NumPy, PyTorch), mainly focused on image classification tasks. Although I am relatively new to open source, I have already contributed to cellfinder (issue #464) and have rapidly learned to use Git, GitHub, and Zulip. In parallel, I have explored theoretical aspects of machine learning—including backpropagation, neural net (like CNNs, and RNNs)—and I am continuously deepening my knowledge of PyTorch and deep learning frameworks.

- **Motivation: why this project?**
I have a strong interest in combining my background with practical applications in computational neuroscience. The BrainGlobe suite, and cellfinder in particular, presents an exciting opportunity to puts the hands on deep learning applied to neuroscience, and directly contribute by integrating advanced network architectures into the project. believe that improving the classification algorithm with a more advanced network architecture will benefit both current and future users, ultimately enhancing the reliability of whole-brain cell detection.

- **Match: why you?**
I am highly motivated and eager to tackle new challenges with determination. Over the past few weeks, I dedicated myself to understanding cellfinder’s codebase, resolved a beginner-friendly issue, and studied the relevant literature on 3D cell detection (include the recommended paper "A deep learning algorithm for 3D cell detection") and modern architectures like EfficientNet. My quantitative background in mathematics and computer science, along with my commitment to continuous learning and adaptability, makes me confident in my ability to contribute effectively to improving cellfinder’s classification algorithm.

- **Availability**
From June onward, I plan to dedicate around 30 hours per week to the GSoC project. Although I may have exams in June/July, I will prioritize GSoC tasks and manage my schedule accordingly (potentially sitting exams at alternative dates). I might take a one-week vacation in August, but I will coordinate with mentors to ensure minimal disruption by either working ahead or making up for any missed time.

## GSoC

- ** GSoC experience
I look forward to challenging myself by working on real-world tasks, implementing solutions, and refining them under the mentorship from experienced developers. I am eager to deepen my knowledge of neural network architectures and best practices for open-source development—both in terms of technical skills (testing, documentation, CI) and collaborative workflows. I’m also excited to learn how to effectively communicate progress, analyze results, and present findings in a clear, compelling way.

- **Are you also applying to projects with other organisations in GSoC 2025?
I am currently focusing my GSoC application on this cellfinder project. Should I consider other GSoC proposals, this one remains my top priority.

*Thank you for considering my application! I look forward to collaborating with the NIU community and mentors on cellfinder.*
