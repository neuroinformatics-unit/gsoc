## Project title

`brainglobe-cellfinder:improve-cellfinder's-classification-algorithm (FatmaElsharkawy)` 

## Personal details
Please include the following information:
- **Full name** Fatma Elsharkawy
- **Email** fatma.elsharkawy03@eng-st.cu.edu.eg
- **GitHub username** FatmaElsharkawy
- **Zulip username** FatmaElsharkawy
- **Location & time-zone** Cairo (GMT+2)
- **Personal website / project portfolio** (optional)
- **Code contribution**
    [Fix progress bar text in cell detection widget](https://github.com/brainglobe/cellfinder/pull/510)

- **Proposal discussion link**
    [#43: brainglobe-cellfinder:improve-cellfinder's-classification-algorithm (FatmaElsharkawy)](https://github.com/neuroinformatics-unit/gsoc/pull/43) 

## Project proposal 

- **Synopsis**

    This project aims to enhance the deep learning classifier in the BrainGlobe cellfinder tool, which detects cells in large-scale brain microscopy images. Currently, cellfinder uses a ResNet-based model for classifying cell candidates, but newer architectures may offer better accuracy, speed, or efficiency. The goal is to implement and evaluate modern alternatives to ResNet, ensuring cellfinder remains at the cutting edge of cell detection. 
    
    **It's important because** other DL techniques may outperform the current architecture making cell detection and classification faster, robust, and hence more reliable by neuroscientists. With the very fast development of DL approaches, cellfinder has to be up-to-date to add a true value for neuroscience research. detecting and mapping cells in 3D throughout the entire mammalian brain is crucial for faster brain understanding and developments in neuroscience.

    **The Open-Source Community Benefits**
    1. Better Neuroscience Tools: Enhances cellfinder’s accuracy/speed, accelerating brain research worldwide.
    2. Reproducible Benchmarks: Clear model comparisons help researchers choose optimal architectures for similar tasks.
    3. Extensible & Well-Documented Code that is harmonized with DL rapid advancements.
    4. Blog posts and tutorials help newcomers in bioimage analysis and deep learning.


- **Implementation timeline**

    Please include the following information:
    1. A bullet point list with **minimal set of deliverables**
       - A Python implementation of at least one new Deep Learning network architecture in cellfinder

       - Quantitative comparison between the current and new architecture

       - Tests to cover any added functionality.

       - Documentation for the new functionality.

       - A blog explaining the new network and its advantages and disadvantages.

    2. Additional **stretch goals** or "if time allows" deliverables (optional)
   
       - Writing a paper that document the technicallities and be an extension to the cellfinder original paper.
       - Make a UML diagram for the cellfinder package, as this will extremely facilitate the navigation of the contributers between classes and make them understand code faster to add contribution easily. 

    3. A detailed **weekly timeline**: when do you plan to do what? 


        | **Phase**               | **Week & Dates**             |    **Tasks** | **Hours/Week** |
        |---------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
        | Community Bonding  | Week 1 (May 8 – May 14)  | Study neuroscientific background: How are cells manually identified? Study how cell candidates are extracted and classified. Explore datasets. Start reading literature on state-of-the-art (SOTA) cell classification networks. | 15-20 |
        |                     | Week 2 (May 15 – May 21) | Deep dive into cellfinder codebase (module by module). Undertand preprocessing. Identify potential bottlenecks in the pipeline. Define evaluation criteria (F1-score, speed, etc.). | 10 (shorter time allocated due to my final exams in the college) |
        |                     | Week 3 (May 22 – June 1) | Make a short research summary of SOTA architectures. Discuss findings with mentors and finalize strategy. Evaluate transfer learning vs. training from scratch. Understand documentation of current model performance. | 10 (shorter time allocated due to my final exams in the college) |
        | Coding Phase 1     | Week 4 (June 2 – June 8) | Investigate possible preprocessing improvements. Implement pre-processing improvements. Develop tests for preprocessing to ensure consistency and correctness. Evaluate changes on model performance. Ensure the preprocessing pipeline is efficient and well-documented. | 15-20 (NASA trip may affect availability, as I was global winner 2024 in Space Apps and may travel to attend celebration in Washington) |
        |                     | Week 5 (June 9 – June 15) | Implement First Alternative Model. Train on dataset and log initial results. Optimize hyperparameters. Implement unit tests for data loading and preprocessing. Ensure pipeline efficiency. | 30-40 (compensating for travel) |
        |                     | Week 6 (June 16 – June 22) | Compare Baseline vs. New Model. Identify speed vs. accuracy trade-offs. Perform error analysis. Explore Vision Transformers (ViTs) or other promising architecture. Work on documentation of model changes. | 25 |
        |                     | Week 7 (June 23 – June 29) | Implement Second Alternative Model if needed. Train and compare with previous models. Conduct further error analysis. Assess potential improvements for better generalization. | 25-30 |
        |                     | Week 8 (June 30 – July 6) | Prepare Midterm Evaluation report. Finalize comparison of models. Ensure experimental results are well-documented for mentors. | 25-30 |
        | Coding Phase 2     | Week 9 (July 7 – July 13) | Implement final refinements based on mentor feedback. Optimize inference speed and memory usage. Expand unit tests for the entire pipeline. Implement other model or experiment with transfer learning and check the results. | 25-30 |
        |                     | Week 10 (July 14 – July 20) | Work on paper/blog documenting findings. Prepare tutorials for future contributors. Run final tests and make any necessary optimizations. | 20-25 |
        |                     | Week 11 (July 21 – July 27) | Address final feedback from mentors. Ensure open-source release is well-documented. Start preparing final GSoC submission report. | 20 |
        |                     | Week 12 (July 28 – August 3) | Submit final code, documentation, and report. Present findings to mentors and the community. Wrap-up and reflections. | 15-20 |
        | Finalization       | Week 13 (August 4 – September 1) | Final refinements, mentor discussions, and community engagement. Contribute to open-source improvements beyond my project scope. | 15-20 |


- **Notes** 
  1. I will have a backup plan for risk mitigation. 
  2. I have already read the cellfinder paper and go through the cellfinder module, but I'll repeat this by diving more deeply during community bonding period.
  3. I am open to experimenting with more than three models if needed, as deep learning requires extensive experimentation. From past experience, I understand that even within the same architecture, refining and tuning hyperparameters is crucial. My approach will be guided by both literature and hands-on experimentation, ensuring we explore the most promising architectures and reaching the optimum classifier.  


- **Communication plan**

   I will establish weekly check-ins with the mentor, either via video meetings or written updates to address any feedback or suggestions. Depending on the project’s needs, we can adjust the frequency of meetings (e.g., every two weeks if the mentor prefers).

    If any issues arise throughout the week or if I need insights, I will reach out via Zulip or WhatsApp after attempting to resolve the problem on my own.

    The plan is flexible and open to refinements based on the mentor preferences. 

## Personal statement


- **Past experience.** 
  
    **1.	Experience with Data science, Deep learning and machine learning:** 
    - **ChestQuest project:** A CT Chest CAD System to Classify between Pneumonia and Normal Scans using both ML and DL techniques. After preprocessing pipeline, over six experimental scenarios were done trying different CNN architectures: VGG19, LeNet, and "CT image pretrained" models in DL and SVM classifier in ML with final accuracy of 95%. The project achieved **First Place in the 10th Undergraduate Research Forum at Cairo University, and Third Place in IEEE Egyptian Paper Contest**
    [paper link](https://drive.google.com/file/d/1sORzBD_7GoABaVTcCcn07FOwvXlW6thZ/view?usp=sharing) 
    - **Computational neuroscience project:** working with Allen dataset and analyzing the effect of rewards on SST neurons of mice using statistical methods.
    - **NASA space apps challenge**: I worked to implement a CNN-LSTM model to forecast future climate changes as part of terratales team project [link](https://terratalesjourney.netlify.app/). The team became **a global winner for 2024**

    **2.	Experience with software development:**

    Here is [a series of five python with Qt desktop apps](https://github.com/DSP-Projects) specialized in digital signal processing tools I contributed in. The org contains six projects, each repo has a readme with full demonstration of the application.

- **Motivation: why this project?**
 
    Although I have navigated many gsoc orgs and projects, but I am interested in this project specifically due to three main reasons:

    1. I want to pursue a master’s degree related to AI and neuroscience.
    2.	I have been enhancing my skills in research, AI, software, neuroscience for over three years, so this will allow me to have hands-on experience in real project that benefit whole neuroscience community.
    3.	The benefits to neuroscientists by facilitating brain exploration, which in turn make advancements faster.

- **Match: why you?**
  
    I already came from a biomedical background that combines biological and technological aspects for benefiting science and healthcare sector. I also worked on with similar project (ChestQuest, mentioned above) that was doing very similar task: classification of medical images. In addition, I have neuroscience background from both college courses and Neuromatch academy where I worked on neural data from mice. I have strong research skills and I was a research assistant in Assistive technologies lab in my college. Moreover, I have strong communication and presentation skills with flexibilty in both dealing and learning.

- **Availability**
    
    There will be an overlap between my final exams and community bonding period. I may also have a travel to Washington in the very first week of coding phase for NASA celebration. Surely, I will work during this period as mentioned in the timeline, but I will dedicate longer hours from the second week to compensate for any delays. For other weeks, generally in normal conditions, I work +50 hours per week, so I will give GSoc from 20 to 30 hours, and for remaining time, I will check for any other responsibilities or self-development. 

## GSoC

- **GSoC experience**

    What do you expect from the program?
1. Enhances my coding skills and make me professional in open-source contributions. 
2.	Makes me dive deeper in DL 
3.	Makes me have more knowledge in neuroscience 
4.	Great opportunity for networking and mentoring


- **Are you also applying to projects with other organisations in GSoC 2025?**
- 
   No.






