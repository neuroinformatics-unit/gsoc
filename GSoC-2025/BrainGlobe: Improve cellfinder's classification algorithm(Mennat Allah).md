# Project Title: "BraniGlobr: Improve Cellfinder's classification algorithm"
_______________________________________________________________________________________________

# Personal Details: 

- **Full name: Mennat Allah Khalifa Hasab Elnabi** 
- **Email: chanmenna@gmail.com**
- **GitHub username: Menna1812**
- **Zulip username: Mennat Abdelfattah**
- **Location & time-zone: Cairo, Egypt  && GMT+2**
_______________________________________________________________________________________________

# **Code contribution**

[Pull Request: Implementing Issue #295 – "Check Location of Detected Cells in Tests" #509](https://github.com/brainglobe/cellfinder/pull/509)

This PR introduces a feature to validate detected cell locations by comparing them against a reference dataset. It ensures that detected cells align with expected locations, improving accuracy in cell detection tests.

**proposal discussion link** 

[BrainGlobe: Improve cellfinder's classification Algorithm(Mennat Allah Khalifa)](https://github.com/neuroinformatics-unit/gsoc/pull/28)
_______________________________________________________________________________________________
# Project proposal 

## Synopsis  

Given the growing need for fast and accurate cell detection in neuroscience research, optimizing cellfinder's classification model would significantly benefit the field. This project aims to enhance the model—used for detecting cells in large-scale brain images—by implementing a more efficient deep learning architecture to replace **ResNet**. While **ResNet** remains a functional convolutional neural network, its high computational cost can slow down large-scale neuroscience workflows.

Deep learning has evolved with modern architectures like **Vision Transformer (ViT)** and **EfficientNet**, which offer improved performance and reduced computational costs compared to older models. The primary objective of this project is to determine whether these modern deep learning models can outperform **ResNet** in terms of **speed and accuracy** for cell classification. Ultimately, by releasing these improvements under an **open-source** license, the project will serve as an inspiration for applying advanced deep learning techniques to image analysis.

**Deliverables**  
- **Implementation** of a new deep learning algorithm within **cellfinder**.  
- **Comprehensive testing** to validate its performance.  
- **Detailed documentation** and a **blog post** explaining the new model, its advantages, and how it was integrated.  

## **Implementation timeline**: 

#### minimal set of deliverables: 
- **Python implementation** of a deep learning classification algorithm to replace ResNet. This implementation will be done in the classify.py and a new ".py" file will be added with the new model just like the "resnet.py" file in the "cellfinder/core/classify" directory.  
- **Testing methods** to evaluate the algorithm’s performance. All the tests will be submitted as ".py" files in the "cellfinder/tests/core" directory. 
- **Comprehensive documentation** covering the implementation details and usage of the model. This documentation will be a markdown file that explains every single detail related to the implementation and usage of the model. Its weaknesses, strengths and a comparison between the performance of the classification algorithm and that of resnet.   
- **Blog post** explaining the new model and providing a step-by-step guide on its integration.   
#### stretch goals (if time allows):
- **Implement a third deep learning algorithm** and compare its performance with ResNet and the newly implemented model.  
- **Expand testing methods** to ensure robustness and explore additional evaluation techniques to improve classification performance.  
- **Enhance the new algorithm** by addressing any weaknesses identified during testing, applying optimization techniques, or improving computational efficiency.  
  
#### Detailed weekly plan: 
- **Initial commitment:** 5 hours per day, 25 hours per week (Fridays and Saturdays off).  
- **Final exams:** From **July 17 to June 1**, limited availability during this period.  
- **Post-exams:** 30+ hours per week dedicated to the project.


| **Week Number**  | **Tasks**  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------|
| **Community Bonding Period** | Engage with the **cellfinder** community, study existing code, and discuss project goals with mentors. Gather feedback to refine the implementation approach. |
| **Week 1-3**  | Research different deep learning algorithms. Communicate with mentors, study various architectures, and finalize the most suitable algorithm for **cellfinder** classification. I think I will be using Keras, as it's already used in the implementation of resnet model in the cellfinder algorithm and it aligns with my skills.  |
| **Week 4-6**  | Implement the selected deep learning model. Define architecture, layers, and optimization techniques. Begin developing and integrating testing methods, test the model locally on a small dataset and  Seek feedback from mentors regularly. |
| **Week 7-9**  | Conduct thorough **testing** and refine the model based on results. Document the implementation process, including model selection and evaluation techniques. |
| **Week 10-11** | Finalize testing and make necessary refinements. Freeze the model's architecture and begin integrating findings into the final documentation and blog post. |
| **Week 12**   | Complete final documentation and submit the blog post. Address any final feedback and ensure that the project meets all deliverables. If time permits, explore stretch goals. |



## Communication plan
I plan to communicate with my mentors on a **daily basis** throughout the project. Each day will start with a **reporting message on Zulip**, summarizing my tasks for the day and receiving feedback on the previous day’s work.  
Additionally, we will hold a **weekly video call meeting** to review my progress, discuss any challenges, and ensure that I am on track. This will help assess whether I am performing well or need to adjust my approach to improve efficiency.  

_______________________________________________________________________________________________

# Personal Statement

I am a Biomedical Engineering student at Cairo University with a strong foundation in multiple programming languages, including Python, Java, C#, and C++. My recent interest in machine learning and deep learning, particularly in computer vision, has driven me to explore courses like CS229 and other related materials on YouTube.

One of my most significant research contributions was in [brain tumor growth modeling](https://drive.google.com/file/d/1aZClwKU_jZ2V5uw-S7rgG5VXgRIAWg19/view?usp=sharing), where I worked on a project focused on modeling tumor progression using partial differential equations and image segmentation. This project introduced me to working with medical image data, utilizing libraries such as **PIL, Matplotlib, and pydicom**. For segmentation, I implemented the U-Net architecture, which enhanced my proficiency with **Keras and deep learning frameworks**. Through this work, I also gained familiarity with medical imaging terminologies such as **voxels and handling DICOM data**. The Cellfinder project aligns perfectly with my interests in computer vision and biomedical imaging. The idea of detecting and classifying brain cells excites me, as it contributes to advancing neuroscience research. Improving the classification algorithm is particularly compelling because it directly enhances the system’s efficiency, accuracy, and usability.
Moreover, this project offers an opportunity to apply my skills in image processing, deep learning, and model evaluation, while also allowing me to contribute to an open-source initiative that has real-world applications. I strongly believe in the Cellfinder project and its potential impact in neuroscience. 
As mentioned above, My experience with medical image segmentation using U-Net and my knowledge of computer vision techniques make me well-prepared to tackle the challenges of improving Cellfinder’s classification algorithm. This makes me believe I am a strong candidate in contributing to this project. 

**Availability**:
During the GSoC period, I will have academic commitments as I am a student. However, my final exams will be completed by June, allowing me to dedicate more time to the project afterward. Aside from my exams, my only other commitment is the ALX Data Science course, which requires one hour every Monday. I believe that I have the ability to manage my schedule and ensure consistent progress on the project throughout the GSoC period.

_______________________________________________________________________________________________
# GSoC

- **GSoC experience**
I expect to learn more from dealing with my mentors and interacting with them as I know how much valuable their experience is in the field I am interested in. Their guidance will be invaluable in enhancing my technical skills and deepening my understanding of open-source contributions and real-world problem-solving. Additionally, I am eager to gain hands-on experience contributing to an open-source project that has a meaningful impact in neuroscience. Working on Cellfinder will allow me to develop practical skills in algorithm improvement, while contributing to a tool that benefits researchers worldwide.
    
- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, I am not applying to anyother organization. 
