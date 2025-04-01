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
    Please link to the pull request where you discussed your project proposal with the community. 

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
  2. I am open to experimenting with more than three models if needed, as deep learning requires extensive experimentation. From past experience, I understand that even within the same architecture, refining and tuning hyperparameters is crucial. My approach will be guided by both literature and hands-on experimentation, ensuring we explore the most promising architectures and reaching the optimum classifier.  


- **Communication plan**

   I will establish weekly check-ins with the mentor, either via video meetings or written updates to address any feedback or suggestions. Depending on the project’s needs, we can adjust the frequency of meetings (e.g., every two weeks if the mentor prefers).

    If any issues arise throughout the week or if I need insights, I will reach out via Zulip or WhatsApp after attempting to resolve the problem on my own.

    The plan is flexible and open to refinements based on the mentor preferences. 



