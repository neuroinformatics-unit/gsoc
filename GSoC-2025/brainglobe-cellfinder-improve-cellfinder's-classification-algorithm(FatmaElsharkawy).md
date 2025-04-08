## Project title

`brainglobe-cellfinder:improve-cellfinder's-classification-algorithm (FatmaElsharkawy)` 

## Personal details
Please include the following information:
- **Full name** Fatma Elsharkawy
- **Email** fatma.elsharkawy03@eng-st.cu.edu.eg
- **GitHub username** FatmaElsharkawy
- **Zulip username** FatmaElsharkawy
- **Location & time-zone** Cairo (GMT+2)
- **Personal website / project portfolio** [Resume](https://drive.google.com/drive/folders/1WOk3H5r5wpUzTibd9RD0H8XHqcXupOkG?usp=drive_link)
- **Code contribution**
    [Fix progress bar text in cell detection widget](https://github.com/brainglobe/cellfinder/pull/510)

- **Proposal discussion link**
    [#43: brainglobe-cellfinder:improve-cellfinder's-classification-algorithm (FatmaElsharkawy)](https://github.com/neuroinformatics-unit/gsoc/pull/43) 

## Project proposal 

- **Synopsis**

    The project aims to improve BrainGlobe's cellfinder tool by enhancing its deep learning classifier for 3D brain cell detection. Detecting and mapping cells in brain images both quickly and reliably is crucial for neuroscience developments. The goal is to explore modern deep learning architectures beyond ResNet and solve limitations in original paper/architecture such as improving dataset quality, reducing false positives, and enabling single-channel input.

    **The Open-Source Community Benefits:**
    1. Better Neuroscience Tools: Enhances cellfinder’s accuracy/speed, accelerating brain research worldwide.
	2. Reproducible Benchmarks: Clear model comparisons help researchers choose optimal architectures for similar tasks.
	3. Extensible & Well-Documented Code with educational resources like blog posts and a potential research paper.

- **Implementation timeline**

    **Minimal set of deliverables**
	1. According to my plan, Python implementation of three new Deep Learning approaches for cell classification.
	2. Quantitative comparison between the current and new architecture with tests to cover any added functionality.
	3. Documentation for the new functionality with a blog explaining the new network with pros and cons.
   
 - **Additional stretch goals:**

	- Writing a paper extending original cellfinder paper –  Try active learning – Try multi-class classifier if data is available.


    ## Weekly Timeline Project Plan
| Week & Dates | Tasks |
|--------------|-------|
| Community Bonding Start (May 8 – June 1) | • Study neuroscientific background: how cell candidates are extracted and classified. • Explore dataset (check biases for certain cell types for future detection). • Understand the Cellfinder paper, codebase, and current limitations. • Read literature on state-of-the-art cell classification networks. • Evaluate transfer learning vs. training from scratch and define performance metrics. • Investigate preprocessing improvements. • Discussion and evaluation with mentors. |
| Coding Phase 1 – Week 4 | • Improve pre-processing/classical image processing steps with unit tests. • Perform data augmentation using GANs and a 3D ResNet baseline. (Need verification of data from neuroscientist) • Discuss dataset generalization. |
| Week 5 | • Plan efficient input data pipeline with on-the-fly augmentation and TFRecord storage. • Enhance model to use single channel and auxiliary input. • Compare both models and assess knowledge distillation for single-channel input. • Optimize hyperparameters and document results. |
| Week 6 | • Implement another model (start with 3D U-Net). Test single and dual channel input. • Analyze performance: F1 score, false positives, model size, training time. • Try implementing another model (e.g., R-CNN). |
| Week 7 | • Implement third model (e.g., Swin Transformer 3D). • Train and compare to previous models. • Conduct error analysis and assess performance vs. complexity tradeoffs. |
| Week 8 | • Finish any delayed work. • Prepare Midterm Evaluation report and finalize comparisons. • Ensure experimental results are documented for mentors. |
| Coding Phase 2 – Week 9 | • Implement refinements based on mentor feedback. • Optimize the whole pipeline and expand unit tests. • Add a Napari module for active learning. |
| Week 10–11 | • Work on blog or paper documenting findings. • Complete remaining testing, optimization, or experiments. • Address final mentor feedback. |
| Week 12 | • Finalize all deliverables. • Submit code, documentation, and report. • Present findings to mentors and community. |



-	Here, [A Simple Risk Mitigation Plan for the above timeline with worst case scenarios discussed](https://1drv.ms/w/c/b7d92fede098858e/Efwn0flAValKhC5wH7KADQcB8XdNcClUQ-0ZkXgTBSBwMA?e=1np4aA)

-	**Hours/week:** 25–35 on average. During university finals (2 weeks on community ponding), 10 hrs/week. Possible travel in first coding week—20 hrs that week, compensated with 40 hrs the following week.

-	**Communication plan:** weekly or Biweekly video meeting. Weekly WhatsApp updates. Flexible to change based on mentor.
  

## Personal statement

- **Past experience.** 
  
    **1.	Experience with Data science, Deep learning and machine learning:** 
    - **ChestQuest project:** A CT Chest CAD System to Classify between Pneumonia and Normal Scans using both ML and DL techniques. Over six experimental scenarios were done trying different CNN architectures: VGG19, LeNet, and "CT image pretrained" with final accuracy of 95%. The project achieved First Place in the 10th Undergraduate Research Forum at Cairo University, and Third Place in IEEE Egyptian Paper Contest 
    [paper link](https://drive.google.com/file/d/1sORzBD_7GoABaVTcCcn07FOwvXlW6thZ/view?usp=sharing) 
    - **Computational neuroscience project:** working on Allen dataset and analyzing the effect of rewards on SST neurons of mice using statistical methods. [presentation & colab notebook](https://docs.google.com/presentation/d/10W7KEmZ0A9hphuoi1j-SOEPv74073JGI92oNCkRbpuE/edit?usp=sharing)
    - **NASA space apps challenge**: I worked to implement a CNN-LSTM model to forecast future climate changes as part of terratales team project [link](https://terratalesjourney.netlify.app/). The team became **a global winner for 2024**

    **2.	Experience with software development:** Here is [a series of five python with Qt desktop apps](https://github.com/DSP-Projects) specialized in digital signal processing tools I contributed in. The org contains six projects, each repo has a readme with full demonstration of the application.

    **3. Experience with Image Processing:** Here is [an org for applications of image processing and computer vision](https://github.com/ComputerVision-Projects) implemented from scratch. It’s still under development and will be updated soon with three more projects.


- **Motivation: why this project?**
 
    Although I have navigated many gsoc orgs and projects, but I am interested in this project specifically due to three main reasons:

    1. I want to pursue a master’s degree related to AI and neuroscience, and this project aligns perfectly with my goals.
    2. I have been enhancing my skills in research, AI, software, neuroscience for over three years, so this will allow me to have hands-on experience in real project.
    3. I’m passionate about contributing to the neuroscience community by helping make brain research faster and more accessible 

- **Why Me?**
  
    I come from a biomedical background that bridges biology and technology to support scientific and healthcare advancements. I previously worked on a similar project, ChestQuest, which involved medical image classification—closely aligning with this project's goals. I have strong programming foundations, including OOP, data structures and algorithms (DSA), and SOLID principles, complemented by hands-on experience in data science and AI through four projects involving machine and deep learning. My neuroscience background includes both academic coursework and practical experience through the Neuromatch Academy, where I analyzed neural data from the Allen Brain Atlas. Additionally, I served as a research assistant in an Assistive Technologies Lab, enhancing my research capabilities. Currently, I’m expanding my expertise in advanced deep learning techniques like transformers and autoencoders. I also bring strong communication and presentation skills, along with adaptability and a continuous learning mindset. 

- **Availability**
    
    Generally, in normal conditions, I work +50 hours per week, so I will give GSoC from 25 to 35 hours on average, and for the remaining time, I will check for any other responsibilities or self-development. 


## GSoC

- **GSoC experience**

    I expect the program will:

  1. Enhance my coding skills and make me professional in open-source contributions. 
  2. Make me dive deeper in DL, hopefully become professional into DL  
  3. Enhance my neuroscience knowledge and enables me to benefit the neuroscience community, since I want to be join them 
  4. Be a great opportunity for networking and mentoring
   
   Briefly, GSoC offers me a unique opportunity to contribute meaningfully to the neuroscience open-source community while also learning and growing through the process. It's a two-way journey — as much as I hope to add value to the project, I know it will also add to my skills and help shape my career path in neuroscience and open science.


- **Are you also applying to projects with other organisations in GSoC 2025?**
     No, I am applying only to this project in GSoC 2025.





