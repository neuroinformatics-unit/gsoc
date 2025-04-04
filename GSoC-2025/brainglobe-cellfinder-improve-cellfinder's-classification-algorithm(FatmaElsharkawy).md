## Project title

`brainglobe-cellfinder:improve-cellfinder's-classification-algorithm (FatmaElsharkawy)` 

## Personal details
Please include the following information:
- **Full name** Fatma Elsharkawy
- **Email** fatma.elsharkawy03@eng-st.cu.edu.eg
- **GitHub username** FatmaElsharkawy
- **Zulip username** FatmaElsharkawy
- **Location & time-zone** Cairo (GMT+2)
- **Personal website / project portfolio** [Resume](https://drive.google.com/file/d/1bc4Yg1LuYDoU28bitd9_uP_SvJfGp0Kz/view?usp=sharing)
- **Code contribution**
    [Fix progress bar text in cell detection widget](https://github.com/brainglobe/cellfinder/pull/510)

- **Proposal discussion link**
    [#43: brainglobe-cellfinder:improve-cellfinder's-classification-algorithm (FatmaElsharkawy)](https://github.com/neuroinformatics-unit/gsoc/pull/43) 

## Project proposal 

- **Synopsis**

    This project aims to enhance the deep learning classifier in the BrainGlobe cellfinder tool, which detects cells in large-scale brain microscopy images. The current architecture use ResNet, and with the fast evolution in deep learning, experiementing other architectures can give better performance.

    **Importance of cellfinder:** Detecting and mapping cells in 3D mammalian brain images is important for faster brain understanding and developments in neuroscience. Manual segmentation is both a difficult and slow task that can be affected by human expertise and fatigue.
    
    **Importance of this project:** other DL techniques may outperform the current architecture making cell detection and classification faster, robust, and hence more reliable by neuroscientists. This is acheivable by addressing weaknesses of current approach, enhancing dataset using current model and generative models, try use one input channel only, and decreasing false positive as much as possible. Trying state-of-art models performance, so cellfinder can be up-to-date to add a true value for neuroscience research. 

    **The Open-Source Community Benefits:**
    1. Better Neuroscience Tools: Enhances cellfinder’s accuracy/speed, accelerating brain research worldwide.
    2. Reproducible Benchmarks: Clear model comparisons help researchers choose optimal architectures for similar tasks.
    3. Extensible & Well-Documented Code that is harmonized with DL rapid advancements.
    4. Blog posts and tutorials help newcomers in bioimage analysis and deep learning.
    5. Addressing weaknesses published in cellfinder paper.


- **Implementation timeline**

    1. **Minimal set of deliverables**
       - Complete review of image analysis steps for cell detection. 
  
       - According to my plan, python implementation of three new Deep Learning approaches for cell classification (Required minimum of one.) Three approaches are: use 3D U-Net, R-CNN, Swim 3D transformer. Also, try primary channel only as input while second channel can be used as auxilary input (this is more demonstrated on timeline)

       - Quantitative comparison between the current and new architectures based on criteria (mentioned in timeline)

       - Tests to cover any added functionality.

       - Documentation for the new functionality.

       - A blog explaining the new network and its advantages and disadvantages.

    2. Additional **stretch goals** or "if time allows" deliverables: 
       - Writing a paper that document the technicallities and be an extension to the cellfinder original paper.
       - Make a UML diagram for the cellfinder package, as this will extremely facilitate the navigation of the contributers between classes and make them understand code faster to add contribution easily. 
       - Trying to be beyond by adding active learning module for continual learning and improvment
       - If data is available, try multi class DL model for multi-class cell classification.

     ## Weekly Timeline Project Plan


 

    | Week & Dates                        | Tasks                                                                                                 | Hours/Week                                           |
    |-------------------------------------|-------------------------------------------------------------------------------------------------------|------------------------------------------------------|
    | **Community Bonding Start**         |                                                                                                       |                                                      |
    | **Week 1 (May 8 – May 14)**         | - Study neuroscientific background: Study how cell candidates are extracted and classified.           | 15-20                                                |
    |                                     | - Explore dataset (check biases for certain cell types as this may be used later for cell type detection) |                                                      |
    |                                     | - Make sure of fully understand the cellfinder paper (I already read it)                               |                                                      |
    |                                     | - Start reading literature on state-of-the-art cell classification networks.                          |                                                      |
    | **Week 2 (May 15 – May 21)**        | - Deep dive into cellfinder codebase (module by module).                                               | 10 (shorter time allocated due to my final exams in the college) |
    |                                     | - Investigate possible preprocessing improvements.                                                     |                                                      |
    |                                     | - Identify potential bottlenecks in the pipeline.                                                     |                                                      |
    |                                     | - Define evaluation criteria (F1-score, speed, etc.)                                                   |                                                      |
    | **Week 3 (May 22 – June 1)**        | - Full understanding of current model performance with limitations                                    | 10 (shorter time allocated due to my final exams in the college) |
    |                                     | - Decide deep learning candidate architectures for the classification task (ResNet alternatives)       |                                                      |
    |                                     | - Evaluate transfer learning vs. training from scratch.                                               |                                                      |
    |                                     | - Discuss findings with mentors and finalize strategy.                                                |                                                      |
    | **Coding Phase 1**                  |                                                                                                       |                                                      |
    | **Week 4 (June 2 – June 8)**        | - Implement improvements for pre-processing/ classical image processing step, and make sure input data is standardized. | 15-20 (NASA trip may affect availability) |
    |                                     | - Develop tests for preprocessing to ensure consistency and correctness.                               |                                                      |
    |                                     | - Data Augmentation using GANs and baseline model (3D ResNet). This step will need verification of data from neuroscientist. |                                                      |
    |                                     | - Discuss the generalization of the dataset, i.e., can this model be used for microscope brand used for imaging? |                                                      |
    | **Week 5 (June 9 – June 15)**       | - Plan for efficient input data pipeline, e.g., data loader and on fly augmentation and store data as TFRecord. | 30-40 (compensating for travel) |
    |                                     | - Enhancement of the existing model to use single channel and secondary channel will fed as auxiliary input. (3D ResNet with Auxiliary Input). |                                                      |
    |                                     | - Comparison between both models based on speed and accuracy to check if the second method is promising, then we can experiment with other models using one channel. |                                                      |
    |                                     | - Train on dataset and log initial results. Optimize hyperparameters.                                 |                                                      |
    |                                     | - Based on the results, we can go with another approach to use one channel input, e.g., knowledge distillation (student and teacher models) |                                                      |
    | **Week 6 (June 16 – June 22)**      | - Implement another model (I prefer to start with 3D U-Net). Can be implemented using one channel only or experiment with two scenarios (with one channel and then with two channels) based on previous week results. | 25-30 |
    |                                     | - Make a comparison analysis based on: F1 score, False Positives, model size, and training time.       |                                                      |
    |                                     | - Discuss whether neglecting one channel as input is a good choice to continue with or not.            |                                                      |
    | **Week 7 (June 23 – June 29)**      | - Implement Second Alternative Model. I prefer to experiment Swin Transformer 3D.                       | 25-30                                                |
    |                                     | - Train and compare with previous models. Conduct further error analysis. Assess potential improvements for better generalization. |                                                      |
    |                                     | - Analyze: Does it give good performance vs. complexity tradeoff? Are more complex models for this problem more promising or just waste of resources? |                                                      |
    | **Week 8 (June 30 – July 6)**       | - Continue any delayed work from previous weeks.                                                     | 25-30                                                |
    |                                     | - Prepare Midterm Evaluation report. Finalize comparison of models.                                    |                                                      |
    |                                     | - Ensure experimental results are well-documented for mentors.                                         |                                                      |
    | **Coding Phase 2**                  |                                                                                                       |                                                      |
    | **Week 9 (July 7 – July 13)**       | - Implement refinements based on mentor feedback.                                                     | 25-30                                                |
    |                                     | - Optimize inference speed and memory usage if needed                                                |                                                      |
    |                                     | - Expand unit tests for the entire pipeline.                                                           |                                                      |
    |                                     | - Based on previous results: try implementing another model, I prefer this time to use R-CNN.          |                                                      |
    | **Week 10 (July 14 – July 20)**     | - Work on paper/blog documenting findings                                                              | 30-40                                                |
    |                                     | - Continue any remaining comparison analysis.                                                         |                                                      |
    |                                     | - Complete any remaining tests.                                                                        |                                                      |
    |                                     | - Going further, either by:                                                                            **1.** Use graph Neural Networks (GNNs) to detect relation between detected cells.                    **2.** Add a napari module for active learning to keep improving model performance.                    |                                                      |
    | **Week 11 (July 21 – July 27)**     | - Address final feedback from mentors.                                                                 | 25-30                                                |
    |                                     | - Continue working on code documentation and paper.                                                   |                                                      |
    |                                     | - Continue working on further deliverables (either the GNN or active learning)                        |                                                      |
    | **Week 12 (July 28 – August 3)**    | - Submit final code, documentation, and report. Present findings to mentors and the community. Wrap-up and reflections. | 20-25 |
    | **Week 13 (August 4 – September 1)**| - Final refinements, mentor discussions, and community engagement.                                     | 20-25                                                |
    |                                     | - Continue working on any remaining additional work.                                                   |                                                      |



- **Notes** 
  1. I will have a backup plan for risk mitigation. 
  2. I am open to experimenting with more than three models if needed, as deep learning requires extensive experimentation. From past experience, I understand that even within the same architecture, refining and tuning hyperparameters is crucial. My approach will be guided by both literature and hands-on experimentation, ensuring we explore the most promising architectures and reaching the optimum classifier.  
  3. For paper writing and stretch goals, if time ended while still working on them, I have no problem to keep improving them with the community. 


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
  
    I already came from a biomedical background that combines biological and technological aspects for benefiting science and healthcare sector. I also worked on similar project (ChestQuest, mentioned above) that was doing very similar task: classification of medical images. In addition, I have neuroscience background from both college courses and Neuromatch academy where I worked on neural data (allen dataset) from mice. I have strong research skills and I was a research assistant in Assistive technologies lab in my college. Moreover, I have strong communication and presentation skills with flexibilty in both dealing and learning.

- **Availability**
    
    There will be an overlap between my final exams and community bonding period. I may also have a travel to Washington in the very first week of coding phase for NASA celebration. Surely, I will work during this period as mentioned in the timeline, but I will dedicate longer hours from the second week to compensate for any delays. For other weeks, generally in normal conditions, I work +50 hours per week, so I will give GSoc from 25 to 35 hours on average, and for remaining time, I will check for any other responsibilities or self-development. 

## GSoC

- **GSoC experience**

    I expect the program will:
  1. Enhance my coding skills and make me professional in open-source contributions. 
  2.	Make me dive deeper in DL, hopefully become professional into DL  
  3.	Enahnces my neuroscience knowledge and enable me to benefit the neuroscience community, since I want to be join them :) 
  4.	Great opportunity for networking and mentoring


- **Are you also applying to projects with other organisations in GSoC 2025?**
  
   No.






