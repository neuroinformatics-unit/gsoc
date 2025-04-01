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
_Length: max 1 page_

- **Synopsis**

    Briefly explain: what is the project about? Why is it important? What are the goals? What are the deliverables? How would the open source community benefit from this project?


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

        | **Phase**             | **Week & Dates**        | **Tasks**                                                                                                                                                                                                                              | **Hours/Week**                                |
        |----------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
        | **Community Bonding** | **Week 1 (May 8 – May 14)**  | Study neuroscientific background: How are cells manually identified? Study how cell candidates are extracted and classified. Explore datasets. Start reading literature on state-of-the-art cell classification networks. | **15-20** |
        |                       | **Week 2 (May 15 – May 21)** | Deep dive into cellfinder codebase (module by module). Investigate possible preprocessing improvements. Identify potential bottlenecks in the pipeline. Define evaluation criteria (F1-score, speed, memory usage, etc.). | **10** (final exams) |
        |                       | **Week 3 (May 22 – June 1)** | Shortlist deep learning architectures for the classification task (ResNet alternatives). Discuss findings with mentors and finalize strategy. Evaluate transfer learning vs. training from scratch. | **10** (final exams) |
        | **Coding Phase 1**    | **Week 4 (June 2 – June 8)** | Implement preprocessing improvements if needed. Implement Baseline Model (ResNet-based) and start training experiments to set benchmark results. Hyperparameter tuning. | **15-20** (NASA trip may affect availability) |
        |                       | **Week 5 (June 9 – June 15)** | Implement First Alternative Model. Train on dataset and log initial results. Optimize hyperparameters. Implement unit tests for data loading and preprocessing. Ensure pipeline efficiency. | **30-40** (compensating for travel) |
        |                       | **Week 6 (June 16 – June 22)** | Compare Baseline vs. New Model. Identify speed vs. accuracy trade-offs. Perform error analysis. Explore Vision Transformers (ViTs) or EfficientNet if viable. Work on documentation of model changes. | **25** |
        |                       | **Week 7 (June 23 – June 29)** | Implement Second Alternative Model if needed. Train and compare with previous models. Conduct further error analysis. Assess potential improvements for better generalization. | **25-30** |
        |                       | **Week 8 (June 30 – July 6)** | Prepare Midterm Evaluation report. Finalize comparison of models. Ensure experimental results are well-documented for mentors. | **25-30** |
        | **Coding Phase 2**    | **Week 9 (July 7 – July 13)** | Implement final refinements based on mentor feedback. Optimize inference speed and memory usage. Expand unit tests for the entire pipeline. | **25-30** |
        |                       | **Week 10 (July 14 – July 20)** | Work on paper/blog documenting findings. Prepare tutorials for future contributors. Run final tests and make any necessary optimizations. | **20-25** |
        |                       | **Week 11 (July 21 – July 27)** | Address final feedback from mentors. Ensure open-source release is well-documented. Start preparing final GSoC submission report. | **20** |
        |                       | **Week 12 (July 28 – August 3)** | Submit final code, documentation, and report. Present findings to mentors and the community. Wrap-up and reflections. | **15-20** |
        | **Finalization**      | **Week 13 (August 4 – September 1)** | Final refinements, mentor discussions, and community engagement. Contribute to open-source improvements beyond my project scope. | **15-20** |

- **Communication plan**

   I will establish weekly check-ins with the mentor, either via video meetings or written updates to address any feedback or suggestions. Depending on the project’s needs, we can adjust the frequency of meetings (e.g., every two weeks if the mentor prefers).

    If any issues arise throughout the week or if I need insights, I will reach out via Zulip or WhatsApp after attempting to resolve the problem on my own.

    The plan is flexible and open to refinements based on the mentor preferences. 



