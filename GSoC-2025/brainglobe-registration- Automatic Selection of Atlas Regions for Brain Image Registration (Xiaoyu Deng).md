## Personal details

- **Full name**: Xiaoyu Deng
- **Email**: xiaoyudeng6@outlook.com
- **GitHub username**: X-Deng
- **Zulip username**: Xiaoyu Deng
- **Location & time-zone**: China, (UTC+8)

- **Code contribution**
	
	Add preprocessing script to apply annotation-based mask to atlas image:
	https://github.com/brainglobe/brainglobe-registration/pull/85


- **Proposal discussion link**

	https://github.com/neuroinformatics-unit/gsoc/pull/64



## Project Proposal

- **Synopsis**

	The `brainglobe-registration` tool is a core component of the BrainGlobe suite, enabling alignment of 2D and 3D microscopy data with standard brain atlases through image registration. Currently, the selection of the atlas subregion used as the registration target is manual, which is an error-prone and time-intensive step that introduces variability into downstream neuroscientific analyses.

	This project aims to automate the selection of registration regions using data-driven approaches such as adaptive grid search, Bayesian optimization, and ML-based heuristics. By doing so, we enhance both the accuracy and reproducibility of image alignment, enabling more robust comparisons across experiments.

- **Minimum Deliverables:**
	- Implement a preprocessing module to automatically select the relevant atlas region based on input data.
	- Develop an adaptive grid search method for atlas region selection.
	- Implement a Bayesian optimization approach as an alternative selection strategy.
	- Evaluate both methods using metrics like registration accuracy and runtime.
	- Ensure smooth integration with the existing brainglobe-registration workflow.
	- Write clear documentation with usage instructions and examples.
	- Add unit and integration tests for robustness and reproducibility.
	- Publish a blog post showcasing the feature and its impact.

- **Extended Deliverables (if time allows):**
	- Implement a third ML-based heuristic approach for intelligent region selection based on learned patterns.


- **Implementation Timeline:**

	(*~30 hours per week*)  

  | Time    | Goals    |
  |-------|---------------------|
  | Pre-GSoC (May 8 – Jun 1) | Community bonding, literature review, environment setup |
  | Week 1 (Jun 2 – Jun 8)   | Design preprocessing module, set up project structure                 
  | Week 2 (Jun 9 – Jun 15)  | Implement adaptive grid search method |                                 
  | Week 3 (Jun 16 – Jun 22) | Implement Bayesian optimization method |                                
  | Week 4 (Jun 23 – Jun 29) | Evaluate methods using accuracy and runtime metrics |                   
  | Week 5 (Jun 30 – Jul 6)  | Finalize core logic, integrate into brainglobe-registration |            
  | Week 6 (Jul 7 – Jul 13)  | Midterm evaluation, code cleanup |                       
  | Week 7 (Jul 14 – Jul 20) | Add configuration options, begin documentation |                        
  | Week 8 (Jul 21 – Jul 27) | Documentation, integration tests, refactor code |                           
  | Week 9 (Jul 28 – Aug 3)  | Begin ML-based heuristic, continue docs |                
  | Week 10 (Aug 4 – Aug 10) | Finalize ML method (if feasible), complete documentation |              
  | Week 11 (Aug 11 – Aug 17)| Code freeze, testing, write blog post |                                 
  | Week 12 (Aug 18 – Aug 24)| Submit final deliverables: code, docs, blog post |                      
  

- **Communication plan**

	I will communicate with my mentor via Zulip chat for daily discussions, with weekly Zoom meetings for progress updates and addressing challenges.


## Personal statement

- **Past experience** 

	I obtained my Master’s degree in Applied Mathematics from the University of Cambridge last year, where I specialized in mathematical statistics and machine learning. After that, I worked as a research assistant at the Cambridge Advanced Imaging Centre, focusing on 3D microscopy image analysis. Specifically, I employed advanced AI models such as SAM and MicroSAM for nuclei and membrane segmentation, fine-tuning these pre-trained models with custom 3D microscopy datasets to improve their performance. Additionally, I have implemented TV-L1 optical flow registration techniques to detect motion in embryos, enabling a deeper analysis of dynamic developmental processes.

	In addition to applied imaging work, I have a strong foundation in mathematical modeling and machine learning. My master essay at Cambridge explored modern techniques for high-dimensional statistical inference, including Approximate Message Passing (AMP), the Convex Gaussian Min-max Theorem (CGMT), and leave-one-out (LOO) methods. These approaches provide exact asymptotic risk estimates in settings where traditional inference breaks down, and are conceptually connected to techniques like Bayesian optimization.

	I program primarily in Python and have extensive experience with numerical and ML libraries including NumPy, SciPy, PyTorch, scikit-learn, and OpenCV. While this will be my first open-source contribution, I’ve worked extensively with collaborative codebases and follow best practices in modular design, version control, testing, and documentation. I’m confident in my ability to contribute high-quality, well-documented code to the community.



- **Motivation: why this project?**

	This project resonates deeply with my current research focus and technical interests. I have hands-on experience working with 3D microscopy images and understand the challenges of manual preprocessing and registration. Automating atlas region selection aligns with my broader goal of improving efficiency and reproducibility in biological image analysis. 
		
	BrainGlobe’s open-source mission and focus on neuroscience tools are especially meaningful to me. I am excited by the opportunity to contribute to a tool that enables large-scale, standardized brain analysis across labs. Making these tools smarter and easier to use helps democratize cutting-edge imaging research, which I find highly motivating.

- **Match: why you?**

	My academic background and research experience align closely with the technical and scientific goals of this project. I have extensive experience in biological image analysis, which has given me a strong understanding of the challenges involved in preprocessing, registration, and optimization of high-dimensional image data.

	In addition, I have a solid foundation in mathematical modeling and machine learning, with particular familiarity in techniques relevant to this project, such as adaptive search strategies and Bayesian optimization. My combined experience in both theoretical and applied research equips me with the skills needed to contribute meaningfully to the project and makes me a strong candidate for this role.


- **Availability**

	I am fully committed to the GSoC timeline and will dedicate around 35 hours per week to the project. I do not have any conflicting coursework, employment, or vacations planned during this period. I will be available for regular communication throughout the project.


## GSoC

- **GSoC experience**

	This will be my first time participating in GSoC. Although I am new to contributing to open-source projects, I have strong experience in programming, particularly in AI and machine learning, with a solid background in Python and libraries such as PyTorch, NumPy, and scikit-learn. I’m excited about the opportunity to apply my skills in a collaborative, real-world software development environment. Through GSoC, I hope to not only deepen my technical knowledge but also learn the workflows and practices of the open-source community while contributing to a tool that supports cutting-edge neuroscience research.



- **Are you also applying to projects with other organisations in GSoC 2025?**

	I am only applying to this project and would give it my full attention and priority.

