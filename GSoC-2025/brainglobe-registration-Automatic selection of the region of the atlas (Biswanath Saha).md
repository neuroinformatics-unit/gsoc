## Personal details

- **Name:** Biswanath Saha (preferred name: Saha)
- **Email:** bsaha0659@gmail.com
- **GitHub username:** Elsword016
- **Zulip username:** Biswanath Saha
- **Location & time-zone:** Japan, JST
- **Personal website / project portfolio** github.com/Elsword016 
- **Code contribution:** Pull request: [[Automatic atlas region selection with similarity metrics]](https://github.com/brainglobe/brainglobe-registration/pull/82) to contribute to the `brainglobe-registration` project.
- **Proposal discussion link:**: https://github.com/brainglobe/brainglobe-registration/pull/82

## Project proposal 
- **Synopsis**
  The `brainglobe-registration` tool currently requires manual atlas region selection, making the process error-prone and time-consuming. This project will automate the selection using similarity metrics, adaptive grid-search, and Bayesian optimization, significantly enhancing accuracy and efficiency.

- **Implementation timeline**

  I. **Minimal set of deliverables:**
  -	Implementation of automatic atlas region selection using similarity metrics (normalized cross-correlation) (PR review in progress)
  -	Adaptive grid-search algorithm for automated selection.
  -	Bayesian optimization-based approach for region selection.
  -	Comparative performance analysis and visualization tools.
  -	Comprehensive documentation and unit tests.
  
  II. **Stretch goals:**
  - Optimization of the entire workflow with GPU acceleration enabling faster large-scale registration.

  III. **Weekly Timeline:**

  | Time frame                          | Tasks and   milestones                                          |
  |-------------------------------------|-----------------------------------------------------------------|
  | Pre-GSoC (Mar 10   – May 8)         | Initial PR,   codebase study, literature review                 |
  | Community   bonding (May 8 – Jun 1) | Development setup,   experimental planning.                     |
  | Week 1-2 (Jun 2 –   Jun 17)         | Grid search   implementation, optimization, visualization       |
  | Week 3-5 (Jun 18   – Jul 10)        | Bayesian   optimization implementation, refinement, evaluation. |
  | Week 6 (Jul 11 –   Jul 18)          | Mid-term:   Finalized grid-search and Bayesian optimization     |
  | Week 7-9 (Jul 19   – Aug 11)        | ML methods   research, initial implementation, evaluation.      |
  | Weeks 10-11 (Aug   12- Aug 27)      | Optimization,   finalize documentation, begin final report      |
  | Week 12 (Aug 28 –   Sep 4)          | Final testing,   submit deliverables and final report           |

**Time commitment:** 15-20 hours per week approx ( I have a 28 hours per week work limit), 4 hours per day.
- **Communication plan**
  - Github issues and PR for tracking development and feedback.
  
  - Biweekly video calls to discuss progress/issues.
  
  - Weekly check-ins with mentors via Zulip.
 
## Personal statement
- **Past experience.**
  
I have a strong background in programming, particularly in image processing and large-scale data analysis. As a neuroscience PhD student, I have developed image processing pipelines for terabyte-sized neuron datasets, optimizing data alignment, stitching and segmentation for connectomics [[project synopsis]](https://sites.google.com/view/biswanathsaha/projects/lm-connectomics) My expertise includes Python, Pytorch, scikit-image, scikit-learn. My recent contribution includes a Nature Communication (2024) paper, "Automated neuronal reconstruction with super-multicolour fluorescence imaging,"(doi.org/10.1038/s41467-024-49455-y) where I helped in developing the clustering algorithm *dCrawler* and also wrote an Python implementation which is faster than the original MATLAB one.
  
- **Motivation: why this project?**

One of the biggest challenges in large-scale neuroscience imaging is achieving precise whole-brain registration, especially in light-sheet microscopy. This project directly addresses that issue, making it highly relevant to my research and the broader neuroscience community. I see great potential in this tool—not only in streamlining workflows but also in making image registration more user-friendly. Thus, I am eager to contribute to this project. By working on it, I hope to enhance the accessibility and efficiency of large-scale image registration, increasing adoption and ultimately benefiting the field of connectomics and beyond.

- **Match: why you?**

Our lab specializes in whole-brain imaging using light sheet microscopy, a technique that requires in whole-brain registration. These issues are a recurring hurdle in our work, making this project a natural and compelling choice for me to pursue. By contributing to this tool, I can directly support the neuroscience community in overcoming these obstacles while advancing my own research in brain connectomics, where efficient image registration for large datasets is essential. With strong expertise in Python, image processing, and machine learning, I am well-prepared to address these challenges. My ability to quickly adapt to new methods is complemented by practical experience—I have already implemented similarity-based registration methods and submitted a [pull request](https://github.com/brainglobe/brainglobe-registration/pull/82) and also communicating with the mentors. This prior contribution not only demonstrates my technical capability but also reflects my deep familiarity with registration complexities, positioning me to deliver robust solutions for this GSoC project.

- **Availability**

I will be fully available during the GSoC work period, with a flexible schedule to accommodate project requirements. While I am engaged in my PhD research, I have experience managing multiple projects simultaneously and can efficiently allocate time to ensure consistent progress. **I will be available to work from 10 am - 2pm [4 hours] (JST) (1 am -5 am UTC) every day except for Tuesday it will be from 12pm-4pm [4hours] (JST) (3 AM - 7 AM UTC). For communications via video calls it will be 10 pm - 3 am (JST) (1 PM - 6 PM UTC)**. But I am flexible to adjust whenver it needed.

## GSoC

- **GSoC experience**

I am participating in GSoC for the first time and look forward to gaining hands-on experience in open-source development. I hope to enhance my skills in collaborative coding, receive mentorship from experienced developers, and contribute meaningful improvements to the project and learning best practices for maintaining and improving scientific software tools. 

- **Are you also applying to projects with other organisations in GSoC 2025?**

No I haven't submitted to the any other organizations I want to solely focus on this project.
