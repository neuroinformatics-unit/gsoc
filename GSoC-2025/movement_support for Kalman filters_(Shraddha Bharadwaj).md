

## Project title

movement: support for Kalman filters (Shraddha Bharadwaj)

## Personal details
Please include the following information:
- **Full name** Shraddha Bharadwaj
- **Email** shraddha5bharadwaj@gmail.com
- **GitHub username** shraddha5bharadwaj
- **Zulip username** https://neuroinformatics.zulipchat.com/#user/896544
- **Location & time-zone** Atlanta, Georgia, United States, EST
- **Personal website/project portfolio** https://github.com/shraddha5bharadwaj


## Project proposal 


- **Synopsis**

     - The aim of the project is to implement a mathematical model such as the Kalman Filter to smooth trajectories using movement metadata and to implement accurate trajectory estimation for each animal concerned in trajectory tracking. 

     - It very often happens that the way the behavior data is processed can vary the inference, I propose a workflow-based wrapper where the user can choose how the data will be processed and the model.

        - Kalman Filter for trajectory prediction of a single animal, options of adapted Kalman Filters with features to accept latent features to be fed to the model. Compare the Adaptive Kalman Filter and variations of the same model.
        - Create a data aggregator that can use all the input data and feed it to a single adapted Kalman filter that is essentially trained on all movements but can predict smoothened trajectory for a single animal. Allow for latent factor Modeling.
         
        - Run a customized trajectory prediction for each animal in consideration by feeding in the context of other animals as input to the model and infer trajectories for all animals from a stacked set of filters. 
        - I propose we can bias the initialization of the filters for a single animal in a multi-animal environment with the position of other animals. A form of latent factor modeling. 
    - The final deliverable would be a callable module where you can choose how the data will be treated, the latent factors that can shape the model, and the type of model that will be used for prediction. Allows the user more flexibility and an opportunity to truly experiment with the data.
    

- **Implementation timeline**

  
    1. Deliverables
    - Implement a Modified Kalman Filter that predicts trajectory for a single animal, given the movement features.
    - Experiment with an adapted Kalman Filter, with different introduced latent, to increase the accuracy of prediction
    - Implement stacking multiple trajectory filters/predictors interlinked to each other.
    - Incorporate relative positions of animals being tracked, to each individual estimation which can help in cases where animals interact.
    - Creating a Data Wrapper that can accommodate multiple animal features and data engineering as required for downstream analysis using the Kalman Filter.
   
    2. A detailed **weekly timeline**: when do you plan to do what? 
        - May 8 June 1 
            - I would like to take the community bonding period to familiarize myself with the movement code repository and plan the design patterns and deliverable objects and their functionality. Conduct a Literature survey on what method can be used to engineer the multiple animal contexts and adaptations that can be done to the Kalman Filter. I want to present this plan to my mentors to gather approval and corrections
        - June 2 - June 9 
            - Code the data wrapper classes required for single and multiple animal contexts. Implement a basic Kalman Filter for trajectory prediction. Create a module that can take in the latent factors that can be used to model the filters.
        - June 9 - June 16 
            - Work on adaptive Kalman filtering models to apply to each animal trajectory individually. Simultaneously the data manager and loader for handling multiple animal contexts.
        - June 9 - June 23 
            - Work on a model that can integrate the data from all animal contexts and implement a single trajectory predictor. Build an interface that can create the workflow for how the data can be aggregated and fed to the second model proposed.
        - June 9 - June 20 
            - Implement modeling the relative positions of animals for each animal into the filter initialization ( biasing the filter as a way to incorporate more information by manipulating Q and R and adjusting F and H through Latent factors that can be modeled) and build the corresponding trajectory prediction algorithm, which can be applied to all animals. The third model is proposed.
        - July 1 - July 7 
            - Implement the workflow of all possible data wrappers and methods that can be called. Compare all model Performances. If a proposed method is not feasible find alternate solutions.
        - July 8 - July 14 
            - Extensive testing, bug tracking, and release generation and documentation. Test the solution with Benchmarked datasets and make the required changes to the plan.
        - July 14 - July 18th Mentors and GSoC contributors can begin submitting midterm evaluations 
        - July 14 - July 21 
            - Generate quantitative proof that adapted Kalman Filter and trajectory predictions are accurate. Make implementation and algorithm changes as required.
        - July 22 - July 27 
            - Test the solution with Benchmarked datasets. If any caveats fix the issues or find solutions.
        - July 28 - Aug 3 
            - Fix any workflow or implementation issues that will arise.
        - Aug 3 - Aug 11 
            - Fix any workflow or implementation issues that will arise.
        - Aug 12 - Aug 18 
            - Test the data wrapper, data aggregator and engineering algorithms, and the Kalman Filter and prepare for release.
        - Aug 19 - Aug 25 GSoC contributors submit their final work product and their final mentor evaluation.


- **Communication plan**

    - I would like to contact my mentors at the beginning and mid week to set a plan for the week and get guidance about the same.
    - Raising PRs for any feature addition is also a way I want to communicate with my mentors.

## Personal statement

- **Past experience.** 

    - Decoding Motor Behavior:  Kalman Filter for Trajectory Predictions
        - Developed a predictive model for motor behavior using neural activity and behavioral data of trajectories of a monkey solving mazes.
        - Worked with neural and behavioral data from a monkey performing center-out maze-reaching tasks (MC Maze dataset). Our goal was to predict the monkey’s hand/cursor trajectories using recorded neural activity. To do this, we implemented a Kalman Filter to estimate position and velocity over time.

        - While a basic Kalman filter typically uses arbitrarily assigned noise parameters, we modified and improved the model by biasing it with data-driven estimates. Specifically:

        - Biased the Kalman Filter using data-driven estimates of Q and R, enabling accurate, generalizable trajectory predictions across complex motor tasks.
        - Enhanced Kalman filtering by biasing the filter with known behavior values to enhance trajectory prediction.
        - Integrated neural operators for velocity modeling.
        - GitHub: https://github.com/shraddha5bharadwaj/ML_Neuro
        - Documentation of Results - https://drive.google.com/file/d/15_Hlfu4s0AmsD9cm0fqvcJZccsM7uBYB/view?usp=sharing
    - Trajectory sequence generation using diffusion models and their analysis.
        - Inspired by this paper https://arxiv.org/abs/1611.00094 I am working with a professor on using diffusion models to get better predictions using Generative Models for fly behaviour.
        - Code is currently private
    - Open Source work
        - Collaborated on developing scFlash, a PyPI-hosted ML tool for preprocessing single-cell RNA sequencing data with flexible support for PCA, t-SNE, and VAE. (https://pypi.org/project/scFlash/)
        - Designed a modular, scalable pipeline using PyTorch Lightning, improving denoising and dimensionality reduction for annotated multi-omics data.
        - Led testing, benchmarking, and documentation to ensure reliability and performance against industry-standard tools.
    - Have coauthored the paper  [A Graph-Based Relook Beyond Metadata for Music Recommendation](https://link.springer.com/chapter/10.1007/978-981-99-2602-2_17)

- **Motivation: why this project?**

    This project is a very good amalgamation of my interests in behavior and spike data analysis, computational tool development, and mathematical modeling and analysis. I have experience in working with niche data that requires specialized and accurate data processing and workflow building. Movement is one such package that can help beneficial inferences from data by allowing innovative features that will help in important inference and I want to be part of its community.
- **Match: why you?**

    I have worked in the past on using Kalman filters and also analysis of neuroinformatics data. I have transcriptomics and phylogenetics and I have realised how important data aggregation tools are. Biological data analysis requires multiple levels. Of analysis I myself search for the best tool that can help me process the data as I need. Being able to integrate multiple tools seamlessly for a scientifically significant analysis is any researcher's requirement and sometimes a cause for roadblocks when required tolls are not present I want to be part of a community that solves that and this is such an opportunity for me.

- **Availability**

    I am a student and I am really interested in taking up the project as a research enthusiast and will not be working on anything else during this time.

## GSoC


- **GSoC experience**

    - In-depth look into the workings of mathematical trajectory modeling.
    - Achieve clean data handling and aggregation.
    - Become an open source contributor for a tool
    - Experiment and learn integrations of latent factor modeling into computational frameworks.

- **Are you also applying to projects with other organizations in GSoC 2025?**

 Nothing else, I came across this package which is very close to what I have been working on in the past year, and am applying to this out of pure enthusiasm for behavior modelling