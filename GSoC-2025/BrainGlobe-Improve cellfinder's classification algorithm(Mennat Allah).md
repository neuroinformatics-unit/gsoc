# Project Title: "BraniGlobe: Improve Cellfinder's classification algorithm"
_______________________________________________________________________________________________

# Personal Details: 

- **Full name: Mennat Allah Khalifa Hasab Elnabi** 
- **Email: chanmenna@gmail.com**
- **GitHub username: Menna1812**
- **Zulip username: Mennat Abdelfattah**
- **Location & time-zone: Cairo, Egypt  && GMT+2**
_______________________________________________________________________________________________

# **Code contribution**

[Pull Request: Implementing Issue #295 - "Check Location of Detected Cells in Tests" #509](https://github.com/brainglobe/cellfinder/pull/509)

This PR introduces a feature to validate detected cell locations by comparing them against a reference dataset. It ensures that detected cells align with expected locations, improving accuracy in cell detection tests.

**proposal discussion link** 

[BrainGlobe: Improve cellfinder's classification Algorithm(Mennat Allah Khalifa)](https://github.com/neuroinformatics-unit/gsoc/pull/28)
_______________________________________________________________________________________________
# Project proposal 

## Synopsis  

Given the growing need for fast and accurate cell detection in neuroscience research, optimizing cellfinder's classification model would significantly benefit the field. This project aims to enhance the model—used for detecting cells in large-scale brain images by implementing a more efficient deep learning architecture to replace **ResNet**. While **ResNet** remains a functional convolutional neural network, its high computational cost can slow down large-scale neuroscience workflows.

Deep learning has evolved with modern architectures like **Vision Transformer (ViT)** and **EfficientNet**, which offer improved performance and reduced computational costs compared to older models. The primary objective of this project is to determine whether these modern deep learning models can outperform **ResNet** in terms of **speed and accuracy** for cell classification. Ultimately, by releasing these improvements under an **open-source** license, the project will serve as an inspiration for applying advanced deep learning techniques to image analysis.

**Deliverables**  
- **Implementation** of a new deep learning algorithm within **cellfinder**.  
- **Comprehensive testing** to validate its performance.  
- **Detailed documentation** and a **blog post** explaining the new model, its advantages, and how it was integrated.  

## **Implementation timeline**: 

#### minimal set of deliverables: 
- **Python implementation** of a deep learning classification algorithm to replace ResNet. This implementation will be done in the classify.py and a new ".py" file will be added with the new model just like the "resnet.py" file in the "cellfinder/core/classify" directory. The new model will be using the EfficientNetB0 architecture which achieves 77.1% with 5.3M parameters compared to ResNet that achieves 76% with 23M parameters. For cellfinder's cell detection tasks, this dramatic efficiency improvement would significantly accelerate processing of large-scale brain imaging datasets without sacrificing accuracy.

I believe EfficientNetB0 is the best architecture for this project given its superior parameter efficiency and performance metrics. However, if it doesn't perform well with cellfinder's specific datasets and requirements, I will implement and evaluate alternative architectures like Vision Transformer (ViT). I'll study different algorithms to explore and determine which one delivers the optimal balance of accuracy, speed, and memory usage for cellfinder's unique needs.

- **Testing methods** to evaluate the algorithm’s performance. All the tests will be submitted as ".py" files in the "cellfinder/tests/core" directory. The tests will include metrics like accuracy, f1-score and will use cross validation. Also, testing the time it takes to train the model and classify an image. and comparing each of these outputs to those of resNet. 

- **Comprehensive documentation** The documentation will include installation instructions for any new dependencies, configuration steps for the new model, and examples of usage. This documentation will be a markdown file that explains every single detail related to the implementation and usage of the model. Its weaknesses, strengths and a comparison between the performance of the classification algorithm and that of resnet.   

- **Blog post** explaining the new model and providing a step-by-step guide on its integration. The blog post could walk through the process of choosing the model, implementing it, and the performance gains observed.

#### stretch goals (if time allows):
- **Implement a third deep learning algorithm** and compare its performance with ResNet and the newly implemented model.  
- **Expand testing methods** to ensure robustness and explore additional evaluation techniques to improve classification performance.  
- **Enhance the new algorithm** by addressing any weaknesses identified during testing, applying optimization techniques, or improving computational efficiency.  
  
#### Detailed weekly plan: 
- **Initial commitment:** 5 hours per day, 25 hours per week (Fridays and Saturdays off).  
- **Final exams:** From **July 17 to June 1**, limited availability during this period.  
- **Post-exams:** 30+ hours per week dedicated to the project.


| **Week Number** | **Tasks** |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **Community Bonding Period** | Engage with the **cellfinder** community, study existing code, and discuss project goals with mentors. Discuss the dataset with the mentors and understand how the current model is trained and used. Study cellfinder's preprocessing pipeline to adapt B0's input requirements. |
| **Week 1-3** | In this period, I will start implementing the EfficientNet architecture using PyTorch or Keras with a PyTorch backend (to match the existing code). The implementation will utilize transfer learning from ImageNet pre-trained weights, which will be fine-tuned on neuroanatomical cell datasets. Then, initial testing will be conducted using a small subset of the data to ensure compatibility with the workflow. |
| **Week 4-6** | Full training of the model using cellfinder's dataset. For the sake of fair comparison, I will use the same hyperparameters as ResNet. Run 5-fold cross-validation to assess accuracy (F1-score) and overfitting risks. Measure per-batch inference time and GPU memory usage vs. ResNet50. |
| **Week 7-9** | Conduct thorough **testing** and refine the model based on results. I will start using hyperparameter tuning by experimenting with different learning rates and batch sizes to optimize the performance of the model. Evaluate impact of input resolution on speed/accuracy. Validate performance on low-quality or artifact-heavy images from the dataset. |
| **Week 10-11** | Freeze the model's architecture and begin integrating findings into the final documentation and blog post. Explain B0's architecture, compound scaling principles, and benchmarking results. |
| **Week 12** | Complete final documentation and submit the blog post. Address any final feedback and ensure that the project meets all deliverables. If time permits, explore stretch goals. |



## Communication plan
I plan to maintain daily communication with my mentors through Zulip, where I will report tasks, receive feedback, and confirm alignment with project objectives. In-depth discussions will be held during video calls made weekly, which will act as problem-solving and strategy-enhancement checkpoints.
I will also utilize email as a secondary channel for providing detailed progress reports or for arguing complex matters that need formal documentation. My updates will be in a brief format: a title with key points, a summary of priorities, and proof points demonstrating progress. My progress will be measured against mentor feedback, work completion, and adaptability, to ensure effectiveness in completing the project.
_______________________________________________________________________________________________

# Personal Statement

I am a student of Biomedical Engineering at Cairo University with a strong foundation in several programming languages such as Python, Java, C#, and C++. My current interest lies in machine learning and deep learning, specifically in computer vision, which has led me to pursue courses such as CS229 and other relevant resources. My recent project focused on [modeling brain tumor growth](https://drive.google.com/file/d/1aZClwKU_jZ2V5uw-S7rgG5VXgRIAWg19/view?usp=sharing), where I applied partial differential equations and image segmentation to simulate tumor growth. In this project, I was introduced to handling medical image data, employing libraries such as PIL, Matplotlib, and pydicom, and using the U-Net architecture for segmentation. This experience also deepened my understanding of medical imaging terminology, such as voxels and working with DICOM data. Through this, I gained proficiency with Keras and other deep learning libraries, which will be highly valuable in my work on the Cellfinder project.

The Cellfinder project aligns perfectly with my interests in computer vision and biomedical imaging. Contributing to brain cell detection and classification excites me, as it has the potential to advance neuroscience research. Improving the classification algorithm, which is central to the project, motivates me because it will optimize the system's effectiveness, accuracy, and usability. This project offers a great opportunity to apply my skills in image processing, deep learning, and model evaluation in a real-world scenario, while contributing to an open-source project with tangible impact in the field.

My background in medical image segmentation using U-Net, along with my practical experience applying computer vision and deep learning techniques, makes me well-suited to contribute to improving Cellfinder’s classification algorithm. My previous work, such as the brain tumor growth modeling project, provided hands-on experience in tackling similar challenges. Additionally, my expertise with Keras and other relevant tools has enabled me to refine models and evaluate their performance effectively. This combination of technical knowledge and passion for the field positions me as a strong candidate to contribute meaningfully to this project.

During the GSoC period, I will have my final exams which will conclude in june. Afterward, I will be able to dedicate more time to the project. I am confident in my ability to manage my time effectively, ensuring consistent progress on the project throughout the GSoC period.


_______________________________________________________________________________________________
# GSoC

- **GSoC experience**
I expect to learn more from dealing with my mentors and interacting with them as I know how much valuable their experience is in the field I am interested in. Their guidance will be invaluable in enhancing my technical skills and deepening my understanding of open-source contributions and real-world problem-solving. Additionally, I am eager to gain hands-on experience contributing to an open-source project that has a meaningful impact in neuroscience. Working on Cellfinder will allow me to develop practical skills in algorithm improvement, while contributing to a tool that benefits researchers worldwide.
    
- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, I am not applying to another organization. 
