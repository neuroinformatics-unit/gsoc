## brainblobe : cellfinder support for 2-D images brain images 

# Personal details 

**Full Name:** Archan Sureja 
**Email:** archansureja1@gmail.com
**GitHub Username:** ArchanSureja
**Location & time-zone:** India, (GMT+5:30)
**Code Contribution:**
I am currently working on adding freeze functionality for the retraining in the cellfinder model ,Here is the issue on which i am working [issue #355](https://github.com/brainglobe/cellfinder/issues/355), Initially Added the Freeze flag for the command line , as per the suggestion currently working on the benchmarking script for tessting the improvement in retraining , Here is [PR #496](https://github.com/brainglobe/cellfinder/pull/496)

---

# Project Proposal

# Synopsis
CellFinder is a powerful tool used for detecting cells in large whole-brain images using traditional image processing combined with deep learning classification. However, it currently only supports three-dimensional images, which limits its usability for neuroscientists working with two-dimensional brain slices. 

This project aims to adapt CellFinder to support two-dimensional images by implementing a new neural network optimized for 2D classification and refactoring image processing code. The final outcome will expand the usability of CellFinder to a broader range of neuroscience research applications.

**Implementation timeline** 

**Deliverables**
- Modified image processing algorithm to support both 2D and 3D images.
- A new neural network optimized for classifying 2D brain images.
- Comprehensive unit and integration tests to validate the new functionality.
- Detailed documentation and example use cases.
- A blog post showcasing the updated functionality and its impact.

**Weekly Timeline** 

| **Week** | **Task Summary** |
|----------|----------------|
| Community Bonding | Familiarize with codebase, research 2D medical imaging models, engage with mentors. |
| Week 1-2 | Research & select best 2D image classification model. |
| Week 3-4 | Modify blob detection to support both 2D and 3D images. |
| Week 5-6 | Implement and train a neural network for 2D image classification. |
| Week 7-8 | Integrate model with CellFinder and optimize performance. |
| Week 9-10 | Write and execute unit tests, validate accuracy with real-world datasets. |
| Week 11 | Write documentation and address feedback. |
| Final Week | Write a blog post and submit the final implementation. |

**Community Bonding Period (Before Coding Starts)**
- Familiarize with CellFinder's existing codebase and documentation.
- Engage with mentors and community members to understand project scope.
- Review research papers on 2D medical image classification.
- Identify state-of-the-art deep learning models for 2D brain image classification.

**Week 1-2: Research & Model Selection**
- Study different neural networks used for 2D medical image classification (e.g., ResNet, EfficientNet, VGG16).
- Compare performance, efficiency, and interpretability of various architectures.
- Select a suitable model based on accuracy, speed, and computational requirements.
- Plan integration of the selected model into CellFinder.

**Week 3-4: Modifying Image Processing Pipeline**
- Refactor blob detection algorithm to process both 2D and 3D images.
- Implement unit tests for modified blob detection pipeline.
- Verify performance on sample datasets.
- Optimize preprocessing steps to ensure compatibility with 2D images.

**Week 5-6: Neural Network Implementation for 2D Images**
- Implement a neural network suitable for 2D brain image classification.
- Train the network using publicly available brain slice datasets.
- Conduct experiments to fine-tune hyperparameters.
- Evaluate model accuracy using standard metrics (F1-score, precision, recall).

**Week 7-8: Integrating Model with CellFinder**
- Integrate the trained model into the CellFinder pipeline.
- Implement functions to classify detected cell candidates in 2D images.
- Ensure compatibility with existing 3D classification functionality.
- Optimize inference speed and memory usage.

**Week 9-10: Testing & Validation**
- Write unit and integration tests for the new functionalities.
- Validate the implementation using real-world datasets.
- Perform benchmarking and performance comparisons.
- Document challenges and optimizations applied.

**Week 11: Documentation & Final Improvements**
- Write detailed documentation on installation, usage, and architecture.
- Create example notebooks showcasing 2D image classification.
- Address any mentor or community feedback.

**Final Week: Blog & Final Submission**
- Write a blog post summarizing the project, findings, and contributions.
- Submit final code and documentation.
- Ensure a smooth handover for future maintainability.

I estimated that minimum number of hours required to complete this project is between 300-350 hours. I plan to dedicate the 30-35 hours per week and approx. 5-6 hours daily.

**Communication plan**
    To communicate with the mentors,I use zulip chats and zoom meetings.I will communicate with my mentors daily on Zulip chat for guidance and continuous feedback. To review the progress from the previous week and discuss plans for the upcoming week.

## Personal statement 

**past exprience** 

    I have programming experince in python for 1.5 years,Enrolled in the Machine Learning course in My Computer Science & Engineering degree course in My University as part of my academic curriculum, currently in third-year of Degree course,Also exprience with NumPy,pytorch and keras,understanding and experince(academic purpose) of different CNN model architectures like VGG16,VGG19,ResNet(Currently used in this project),Inception and MobileNet

**Motivation** 

I am always interseted in Computer vision and Deep learning real-world applications , and this project provides the great opportunity to do that.And my technical background and my interset mathches the skill required to complete this project,Moreover this project's focus on the neuroscientists which are the potential users of this project , indirectly by working on this project i can contribute and help them to do better research in neuroscience field.  

**Match:Why me** 
    I am currently contributing to the project for making improvements in the retrainig of the current model,that helped me to understand the current working of the model and made me fimilar & comfortable with the codebase and also i am connected to the mentor on the zullip chat , that shows my dedication to this project and I am confident enough that i will effeciently compelete this project 

**Availabilty** 
    I will be fully avaible during the working period , as i will have my summer break in college during that time 

## GSoC

- **GSoC experience**

   For me,GSOC is great way to start the open source contribution. and their very diverse orginizations with very diverse project statements,It Gives us opprotunity to work on the real world projects that makes impact from research,engineering,economics,creative arts,humnities and many more fields 

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am 100% dedicated to Brainglobe's project and have no plans to submit a proposal to any other organization.