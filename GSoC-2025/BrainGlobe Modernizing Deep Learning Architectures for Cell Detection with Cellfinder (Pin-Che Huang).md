## BrainGlobe: Modernizing Deep Learning Architectures for Cell Detection with Cellfinder (Pin-Che Huang)

### Personal Details

- **Full name**: Pin-Che Huang (Prefer name: Jerry) 
- **Email**: jerry40902@gmail.com  
- **GitHub username**: PinChe69 
- **Zulip username**: PinChe (ID: 894498)
- **Location & Time-zone**: Taiwan (GMT+8)  

---

### Code Contribution 
I have submitted a draft PR to `cellfinder`, where I begin integrating a modern deep learning architecture to replace ResNet. 
Link: https://github.com/brainglobe/cellfinder/pull/520


---

### Proposal Discussion Link
Link: https://github.com/neuroinformatics-unit/gsoc/pull/48#issue-2970062488

---

## Project Proposal

### Synopsis
`cellfinder` is a deep learning tool used to detect cells in large-scale brain imaging datasets. It currently uses a ResNet classifier to differentiate between cells and non-cells. Since ResNet was introduced, newer architectures like EfficientNetV2, ConvNeXt, and MobileNetV3 have proven to be more efficient and accurate in various image classification tasks.

This project proposes replacing or augmenting the current model in `cellfinder` with at least one modern architecture, then benchmarking performance against ResNet in terms of accuracy, speed, and memory usage. The aim is to improve precision and computational efficiency for labs using `cellfinder` on large datasets.

Deliverables include the new model implementation, integration into the training pipeline, performance evaluation, unit tests, documentation, and a user-facing blog/tutorial.

### Implementation Timeline (Large Project ~350 hours)

| Week | Dates | Tasks |
|------|-------|-------|
| **Community Bonding** | May 8 – June 1 | Familiarize with the `cellfinder` codebase, run ResNet training, explore EfficientNet structure, and discuss integration plans with mentor |
| **Week 1** | June 2 – June 8 | Add basic EfficientNet model structure in PyTorch and integrate it into the `cellfinder` model pipeline |
| **Week 2** | June 9 – June 15 | Refine data flow and preprocessing for the new model; begin small-scale training and confirm output compatibility |
| **Week 3** | June 16 – June 22 | Add evaluation metrics (accuracy, speed) and implement simple logging for model comparison |
| **Week 4** | June 23 – June 29 | Add CLI/config support for switching between ResNet and EfficientNet; begin initial documentation |
| **Week 5** | June 30 – July 6 | Clean up codebase, write internal comments and developer notes for future maintainers |
| **Week 6** | July 7 – July 13 | Midterm preparation: run benchmarks, generate model plots or metrics, finish initial documentation |
| **Week 7** | July 14 – July 21 | Midterm Evaluation: Submit models, benchmarks, and documentation for mentor review |
| **Week 8** | July 22 – July 28 | (Military service begins) Weekend: begin writing tutorial/blog post and test scripts |
| **Week 9** | July 29 – August 4 | Weekend-only: Improve model training settings and documentation polish |
| **Week 10** | August 5 – August 11 | Weekend-only: Finalize blog post, prepare user-facing CLI documentation |
| **Week 11** | August 12 – August 18 | Code freeze; final bug fixes and testing clean-up |
| **Week 12** | August 19 – August 25 | Submit final report and ensure mentor feedback is addressed |
| **Final Submission** | August 25 – September 1 | Submit deliverables to GSoC portal |
| **Week 13** | September 2 – September 8 | Extension: Experiment with input shape changes or additional model tweaks |
| **Week 14** | September 9 – September 15 | Extension: Add support for default config file improvements and better error handling |
| **Week 15** | September 16 – September 22 | Write a follow-up blog post reflecting on the EfficientNet implementation journey |
| **Week 16** | September 23 – September 29 | Help close remaining PRs and review other contributors' questions or related issues |
| **Week 17–18** | September 30 – October 13 | Continue light weekend maintenance, improve usability, test on real datasets if possible |
| **Week 19–20** | October 14 – October 27 | Final polish, assist in writing integration summary, and document post-GSoC transition plan |


**Weekly Hours**: ~28 hrs/week before July 21 and after September 16, ~6-8 hrs/week during July 22 to September 15 (weekends only)

### Communication Plan
- Weekly mentor meetings via Zoom/Google Meet  
- Weekly asynchronous check-ins via Zulip  
- Code progress tracked through GitHub Issues and PRs

---

## Personal Statement

I am an undergraduate at National Tsing Hua University (Taiwan), majoring in Medical Science, with strong interests in neuroscience and computational systems. I’m currently learning neural modeling in a computational neuroscience lab and studying core machine learning concepts.

Recently, I joined the Computational Neuroscience Lab in National Tsing Hua University (Taiwan), where I have begun exploring biologically realistic spiking neural network models based on Drosophila brain connectomics. Our lab focuses on fruit fly brain simulation and neuromorphic computing, using large-scale spiking models with detailed membrane and synaptic dynamics. Although I’m still early in my training, this environment is helping me understand how information encoding, recurrent network structures, and biologically grounded simulations intersect with neural data analysis and AI system design.

I have experience in Python (NumPy, OpenCV, Tkinter), C, C++, HTML/CSS/JS, and exposure to RISC-V. I’ve built Arduino-based bio-sensing systems, worked with fluorescence imaging, and assisted in experiments including neuron culture and ELISA.

In 2024, I interned at Stanford’s Wu Tsai Neurosciences Institute, contributing to EasyEVO—a hardware-software platform for directed evolution. I worked on circuit design, embedded debugging, and lab automation.

As vice captain of NTHU’s iGEM team, I oversee the coordination between wet and dry lab teams. In our 2024 project “Pandage,” I led dry lab modeling: building an ODE system inspired by Lotka–Volterra to simulate the interaction of Gram bacteria, probiotics (L. lactis), and antimicrobial peptides. I used Python for simulation and trained an MLP neural network with >3600 synthetic datasets to recommend personalized drug dosing strategies. I also ran Ansys simulations for drug diffusion and modeled discrete hydrogel contraction for dosage control.

This project deepened my understanding of how modeling and machine learning can drive personalized biomedical applications—insight I hope to bring to `cellfinder`.

I am excited about this project because it bridges neuroscience and applied deep learning. Enhancing `cellfinder` will benefit labs worldwide by improving performance and flexibility. My hands-on experience, leadership in iGEM, and ability to work across software and biology make me a strong fit for this work.

---

### Availability
I am fully available (~20 hrs/week) from June 2 to July 21. From July 22 to September 15, I will be on military service but can continue work during weekends (~6–8 hrs/week). I plan to complete major deliverables early and stay in regular contact with mentors throughout.

---

## GSoC Experience
This is my first time applying to GSoC. I am applying only to BrainGlobe, as the project strongly aligns with my interests in computational neurobiology. I see GSoC as a valuable opportunity to learn from mentors and contribute meaningful code to the neuroscience community.
