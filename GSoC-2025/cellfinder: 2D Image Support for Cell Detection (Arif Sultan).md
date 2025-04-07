# cellfinder - 2D Image Support for Cell Detection (Arif Sultan)

## Personal Details

- **Full name:** Arif Sultan
- **Email:** b24bs1058@iitj.ac.in 
- **GitHub username:** msp99000 
- **Zulip username:** arif_sultan 
- **Location & time-zone:** Jodhpur, India (IST, UTC+5:30) 

### Code contribution

- I worked on Issue [#140](https://github.com/brainglobe/brainglobe-workflows/issues/140) in [brainglobe-workflows](https://github.com/brainglobe/brainglobe-workflows) which optimzed the Windows CI performance. The pull request is [#141](https://github.com/brainglobe/brainglobe-workflows/pull/141), and it has been merged.


### Proposal discussion link

- [Discussion on Github](https://github.com/neuroinformatics-unit/gsoc/pull/66)

--- 

## Project proposal

### Synopsis

- #### What is the project about?
  The BrainGlobe cellfinder tool is used to detect cells in large whole-brain images. It uses traditional image processing to find possible cell candidates and passes them to a customisable classifier to split the candidates into cells and no-cells. cellfinder relies heavily on pytorch and keras.
  cellfinder currently uses a residual neural network (ResNet) to classify cell candidates. This network is designed for three-dimensional whole-brain images, but neuroscientists often take images of two-dimensional slices of the brain. This project is aimed at adapting cellfinder to support two-dimensional data which would involve implementing a new neural network suitable for two-dimensional images, as well as refactoring some of the image processing.

- #### Why is it important?
  For a normal neuroscientist in lab, visualizing 3D images is often done on good hardware systems which supports softwares for 3D rendering and this thing is often compute heavy and henceforth computationally expensive. Implementation in 2D is relatively simple for both the neuroscientists and the algorithms as well since neuroscientists can read on papers like MRI and the algortithms working in 2D will be comparitively less computationally intensive which will save cost and time for the department.

- #### What are the goals?
  The goals include:
  - Developing an effective 2D cell classifier neural network in PyTorch
  - Maintain backward compatibility with 3D workflows as well
  - Ensure that the algorithm accuracy is on par with the manual counting
  - Testing algorithm on multiple test cases

- #### What are the deliverables?
  Following are the deliverables:
    - A modified implementation of the existing image processing algorithm (blob detection) in cellfinder that detects cell candidates in both two- and three-dimensional images
    - A Python implementation of a neural network in cellfinder that classifies cell candidates from two-dimensional images.
    - Tests to cover any added functionality.
    - Documentation for the new functionality.
    - A blog showcasing the use of cellfinder on two-dimensional images of brain

- #### How would the open source community benefit?
  The open source community would benefit in multiple ways:
  - It will save time of the neuroscientists compared to the manual counting process
  - It will reduce the barrier to entry for neuroscienrists with limited equipments
  - It will strengthen BrainGlobe's ecosystem with new tools

### Implementation timeline

- ### i. Minimal set of deliverables

  - Support for 2D Blob Detection Algorithm in PyTorch (U-Net, ResNet etc.) alongside the 3D algortihm
  - Making sure the PyTorch model is on par accuracy with manually counting
  - Modify classification logic for dual 2D/3D support for cells/non-cells.
  - Add unit tests and write developer/user documentation.
  - Publish a blog demonstrating 2D pipeline results with visuals and examples.

- ### ii. Stretch Goals
  - A Web App for live image upload and get results, preferably, using Streamlit or Flask


- ### iii. Weekly Timeline

  | Phase | Dates | Planned Tasks | Hours |
  |------|-------|--------------|-------|
  | **Community bonding** | May 8-Jun 1 | • Study cellfinder codebase in depth<br>• Set up development environment<br>• Draft detailed implementation plan<br>• Discuss architecture decisions with mentors | 15-20 |
  | Week 1 | Jun 2-8 | • Fork initial implementation branches<br>• Begin refactoring blob detection to handle dimension input | 30 |
  | Week 2 | Jun 9-15 | • Complete dimension-agnostic preprocessing<br>• Start implementing 2D blob detection logic | 35 |
  | Week 3 | Jun 16-22 | • Finish blob detection algorithms<br>• Generate test datasets for validation | 35 |
  | Week 4 | Jun 23-29 | • Start developing 2D classifier architecture<br>• Research optimal CNN structures for cell detection | 30 |
  | Week 5 | Jun 30-Jul 6 | • Implement initial 2D classifier model<br>• Set up training pipeline | 35 |
  | Week 6 | Jul 7-13 | • Train and validate initial model<br>• Prepare mid-term evaluation materials | 30 |
  | **Mid-term** | Jul 14-18 | • Submit progress report<br>• Get feedback and adjust timeline if needed | - |
  | Week 7 | Jul 19-25 | • Optimize 2D classifier based on validation results<br>• Begin integration with main pipeline | 35 |
  | Week 8 | Jul 26-Aug 1 | • Complete integration of 2D and 3D pipelines<br>• Work on automatic dimensionality detection | 30 |
  | Week 9 | Aug 2-8 | • Implement final classifier improvements<br>• Add unit and integration tests | 35 |
  | Week 10 | Aug 9-15 | • Write user documentation<br>• Create tutorial notebooks | 30 |
  | Week 11 | Aug 16-22 | • Code freeze<br>• Bug fixes and performance optimization<br>• Finalize documentation | 35 |
  | Week 12 | Aug 23-29 | • Write blog post with examples<br>• Final testing and cleanup | 30 |
  | **Final evaluation** | Aug 30-Sep 1 | • Submit final deliverables<br>• Prepare project handover notes | - |

- ### Communication plan

  To ensure transparency and collaboration, I will:
  
  - Share regular updates via GitHub issues and pull requests
  - Participate in biweekly mentor sync-ups via video calls
  - Stay active on Zulip for daily communication and quick clarifications
  - Write clear, maintainable code with thorough documentation

---

## Personal statement

- ### Past experience

  I have good knowledge in working with Python, NumPy, Pandas, PyTorch, Scikit Learn and realted Machine Learning and Deep Learning tools. I also have a good hold over Git and Github and can work in a collaborative environment. At IIT Jodhpur, I have worked on academic projects involving image classification, medical imaging, and real-time systems. I also won a hackathon organized by IIT Jodhpur and AIIMS Jodhpur by developing a real-time blood coagulation monitoring system using deep learning. ([Certificate link](https://drive.google.com/file/d/1GnRyScF5NUHh62EgA0NvaPuFcARD37tb/view?usp=drivesdk))

- ### Motivation: Why this project?

  Since i've already worked on projects in medical imaging, this project aligns with my passion for medical image processing, and neuroscience. Working on `cellfinder` to support 2D data significantly will help lower the barrier to entry for many neuroscience labs and I’m deeply motivated to contribute to such a widely used open-source tool that directly supports scientific research and reproducibility.

- ### Match: Why you?

  I bring a strong background in Python, deep learning, and image processing. I’ve contributed to BrainGlobe's CI workflows and am familiar with the development stack. My experience with training models, handling image data, and writing maintainable code aligns well with the scope of this project. I am proactive, collaborative, and passionate about contributing to research-oriented open-source tools.

- ### Availability

  I am available full-time for GSoC and have no other major commitments. I can dedicate 25–35 hours per week consistently and adjust based on mentor availability or project needs.

- ### GSoC experience
  
  I see GSoC as a chance to grow as a developer while contributing to a meaningful open-source project. I hope to deepen my skills in collaborative software development, learn from experienced mentors, and make long-lasting contributions to the BrainGlobe community. I aim to continue contributing beyond GSoC and expand my involvement in neuroinformatics tools.

- ### Other applications

  I am applying **exclusively** to this BrainGlobe project for GSoC 2025. My full focus will be on successfully completing and delivering all milestones of this proposal.
