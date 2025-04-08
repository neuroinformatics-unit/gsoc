# ethology: OCTRON (Laurel Humphrey)

## Personal details
- **Full name:** Laurel Humphrey
- **Email:** laurelhumphrey24@gmail.com
- **GitHub username:** laurelhumphrey
- **Zulip username:** Laurel Humphrey
- **Location & time-zone:** USA (UTC-05:00)
- **Personal website / project portfolio:** [Project OCTRON](https://github.com/horsto/OCTRON)
- **Code contribution:** [Pull request](https://github.com/horsto/OCTRON/pull/12)
  
## Project proposal 

**Synopsis**

[OCTRON](https://github.com/horsto/OCTRON) is a pipeline designed for markerless segmentation and tracking of animals in behavioral experiments. While there are numerous options for markerless key point tracking available, such as [DeepLabCut](https://github.com/DeepLabCut/DeepLabCut) and [SLEAP](https://github.com/talmolab/sleap), there is a notable lack of analysis workflows that support instance segmentation in videos. This limitation restricts tracking to species with body plans suitable for anchor point-based tracking and confines the types of analyses to purely positional data. However, the diversity of non-classical model organisms is vast, including species like hydra and cephalopods, which have highly morphable body plans that elude standard key point tracking. Behavioral quantification for these species benefits from analyses on segmented regions rather than just positional data. OCTRON is built as a napari plugin and utilizes the advanced segmentation [Segment Anything (SAM) 2](https://github.com/facebookresearch/sam2) for rapid training data generation over video frames. It can then be used to train custom segmentation models (using [YOLO, Ultralytics](https://github.com/ultralytics/ultralytics)) for unsupervised segmentation and tracking of single or multiple animals per behavioral video. Currently in early development, OCTRON is envisioned as an extension of the [ethology](https://neuroinformatics.dev/get-involved/gsoc/projects_2025/ethology.html) project within the NIU GSoC initiative. Although we have a working version, several improvements are needed to make it a maintainable and usable open-source community contribution. These improvements include code maintainability, documentation, a test suite, and further development of core OCTRON functions.

Below is a depiction of the OCTRON GUI used for annotation (a cuttlefish in this example) on the left and application of a custom trained model (trained on a marine worm) on the right. See [here](https://github.com/horsto/OCTRON/blob/main/pics/cuttlefish_octron.gif) and [here](https://github.com/horsto/OCTRON/blob/main/pics/tomopteris_long_swim.gif) for GIF of the figure below. 

<img width="1247" alt="Screenshot 2025-04-07 at 8 52 19 PM" src="https://github.com/user-attachments/assets/43f40a7b-5278-4adf-963e-700ac73ff146" />


**Implementation timeline**

**Minimal deliverables:**

Code maintainability
* Structure of the repository and organization of the codebase.
* Code test suite for unit testing and PyTest.
* Contribution guidelines and onboarding for new contributors.

Documentation
* Complete code documentation website, for example hosted on GitHub via MkDocs.

Usability improvements and further development 
* Together with OCTRON main developer Horst Obenhaus: Utilities for analysis video generation and other useful features for processing OCTRON     segmentation and tracking outputs.
* Utilities for curating OCTRON output, such as stitching/merging tracks that have been artificially separated.

Stretch goals (if time allows)
* Integration of key point tracking into YOLO training.
* Integration of OCTRON with existing tools in the NIU codebase, like movement.


**Weekly timeline:**
*   **Total duration:** 10 weeks (~90h small project size)
*   **Estimated weekly hours:** 8-10 hours/week

|      Week     |                                                                                                              Task                                                                                                              |
|:-------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Before start  | Community bonding. Introduce OCTRON to mentors and discuss potential improvements.                                                                                                                                             |
| 1-3           | Create code documentation website. Streamline codebase and introduce new features for visualizing and working with tracking and segmentation output from YOLO, such as automated video generation and track merging/splitting. |
| 4-7           | Create a testing suite for OCTRON.                                                                                                                                                                                             |
| 8-10          | Stretch goals: Have a look at integrating key point tracking into YOLO training. Integrate OCTRON with other tools in the NIU codebase, like movement.                                                                         |

**Communication plan**

I am flexible to communicate with my mentor regularly as needed. Weekly video call meetings would be helpful to give progress updates as I move through my deliverables and to ask questions on areas where I need more guidance. [Horst Obenhaus](https://github.com/horsto), the main developer of OCTRON, has agreed to lend full support to the project development during GSoC and will be available for discussions and feedback. I will also be available via Zulip chat to ask for troubleshooting help and work through errors as needed throughout the week. 

## Personal statement

**Past experience:** 
    
So far, I have been working with the OCTRON developer Horst Obenhaus to test its usage on various animal behavior videos and evaluate the results. This involves annotating videos of various animal species behaviors and training custom models through the OCTRON GUI, working through errors, and evaluating the effectiveness of the model. I hope to contribute further improvements to this tool with the help of GSoC and NIU mentorship.

My past programming experience includes using Linux, high-performance computing, Python, and R to conduct bioinformatics research assembling and annotating the genomes of endangered species for comparative analysis. I am involved in ongoing publications to document the novel genome assemblies of corals and other organisms, and have contributed to the testing of an open source genome assembly pipeline Argonaut on GitHub.
   
**Motivation: why this project?**

I am interested in this project because I believe OCTRON will be a valuable alternative to existing key point tracking algorithms and a resource for various scientists to further study animal behavior tracking. I was drawn to Horst's research goals of tracking octopus sleep patterns through video data and how this napari plugin could improve the efficiency and effectiveness of his research, as well as the research of others in the open source community. This opportunity relates to my own goals of exploratory research on marine animal behaviors, while also developing my bioinformatics skills through open source code development and refinement.

**Match: why you?**

My experience with testing OCTRON so far on various datasets as well as my previous computational biology background and passion for this project make me a great fit for this opportunity. Through working on this project and others I have gained skills in troubleshooting errors, building code, improving user experience, and science accessibility which I hope to build upon by bringing this new tool to the GSoC community.
  
**Availability:**

I am a research assistant at the [Marine Biological Laboratory](https://www.mbl.edu/) in Woods Hole, Massachusetts, and during GSoC I will be working a regular job 40 hours per week. I plan to allocate around 2 hours after each work day to my GSoC work.

## GSoC

**GSoC experience**

I hope to gain valuable experience from this program related to code testing, development, and documentation in order to improve the available resources for tracking animal behavior data. This mentorship and hands-on experience related to biological coding will benefit my professional goals while helping to contribute open source resources for other scientists in the community.

**Are you also applying to projects with other organisations in GSoC 2025?**

This is the only project and organization I am applying to in GSoC 2025.
