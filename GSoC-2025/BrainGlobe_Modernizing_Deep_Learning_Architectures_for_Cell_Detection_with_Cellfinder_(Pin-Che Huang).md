## BrainGlobe: Modernizing Deep Learning Architectures for Cell Detection with Cellfinder (Pin-Che Huang)

### Personal Details

**Full name**: Pin-Che Huang  
**Email**: jerry40902@gmail.com  
**GitHub username**: PinChe69 
**Zulip username**: PinChe (ID: 894498)
**Location & Time-zone**: Taiwan (GMT+8)  

---

### Code Contribution
I am currently preparing a contribution to `cellfinder` by building a minimal PyTorch implementation of a modern deep learning architecture such as EfficientNet, and benchmarking it against the current ResNet model. This will be submitted as a draft pull request or issue during the community bonding period.

---

### Proposal Discussion Link
https://github.com/neuroinformatics-unit/gsoc/pull/48#issue-2970062488

---

## Project Proposal

### Synopsis
`cellfinder` is a deep learning tool used to detect cells in large-scale brain imaging datasets. It currently uses a ResNet classifier to differentiate between cells and non-cells. Since ResNet was introduced, newer architectures like EfficientNetV2, ConvNeXt, and MobileNetV3 have proven to be more efficient and accurate in various image classification tasks.

This project proposes replacing or augmenting the current model in `cellfinder` with at least one modern architecture, then benchmarking performance against ResNet in terms of accuracy, speed, and memory usage. The aim is to improve precision and computational efficiency for labs using `cellfinder` on large datasets.

Deliverables include the new model implementation, integration into the training pipeline, performance evaluation, unit tests, documentation, and a user-facing blog/tutorial.

### Implementation Timeline (Large Project ~350 hours)

| Week | Dates | Tasks |
|------|-------|-------|
| **Community Bonding** | May 8 – June 1 | Review codebase, run ResNet training, select alternative architectures, mentor discussion |
| **Week 1** | June 2 – June 8 | Implement EfficientNet or ConvNeXt; basic integration test |
| **Week 2** | June 9 – June 15 | Complete integration; begin training on sample data |
| **Week 3** | June 16 – June 22 | Benchmark initial results; tune hyperparameters |
| **Week 4** | June 23 – June 29 | Add CLI/config model selector; document model logic |
| **Week 5** | June 30 – July 6 | Implement optional second model (e.g., MobileNetV3) |
| **Week 6** | July 7 – July 13 | Finalize testing; prepare for midterm evaluation |
| **Week 7** | July 14 – July 21 | Midterm Evaluation: models, benchmarks, documentation submitted |
| **Week 8** | July 22 – July 28 | (Military service begins) Weekend: blog writing, bug fixes |
| **Week 9–10** | July 29 – August 11 | Weekend-only: finalize blog/tutorial, adjust documentation |
| **Week 11** | August 12 – August 18 | Code freeze; finalize testing, clean-up |
| **Week 12** | August 19 – August 25 | Submit final report and receive mentor feedback |
| **Final Submission** | August 25 – September 1 | Submit final deliverables to GSoC portal |
| **Extension (if needed)** | Sept 2 – Sept 15 | Optional polish/follow-up (weekends only) |

**Weekly Hours**: ~20 hrs/week before July 21, ~6–8 hrs/week after (weekends only)

### Communication Plan
- Weekly mentor meetings via Zoom/Google Meet  
- Weekly asynchronous check-ins via Zulip  
- Code progress tracked through GitHub Issues and PRs

---

## Personal Statement

I am an undergraduate at National Tsing Hua University (Taiwan), majoring in Medical Science, with strong interests in neuroscience and computational systems. I’m currently learning neural modeling in a computational neuroscience lab and studying core machine learning concepts.

I have experience in Python (NumPy, OpenCV, Tkinter), C, C++, HTML/CSS/JS, and exposure to RISC-V. I’ve built Arduino-based bio-sensing systems, worked with fluorescence imaging, and assisted in experiments including neuron culture and ELISA.

In 2024, I interned at Stanford’s Wu Tsai Neurosciences Institute, contributing to EasyEVO—a hardware-software platform for directed evolution. I worked on circuit design, embedded debugging, and lab automation.

As vice captain of NTHU’s iGEM team, I oversee the coordination between wet and dry lab teams. In our 2024 project “Pandage,” I led dry lab modeling: building an ODE system inspired by Lotka–Volterra to simulate the interaction of Gram bacteria, probiotics (L. lactis), and antimicrobial peptides. I used Python (`scipy.integrate.odeint`) for simulation and trained an MLP neural network with >3600 synthetic datasets to recommend personalized drug dosing strategies. I also ran Ansys simulations for drug diffusion and modeled discrete hydrogel contraction for dosage control.

This project deepened my understanding of how modeling and machine learning can drive personalized biomedical applications—insight I hope to bring to `cellfinder`.

I am excited about this project because it bridges neuroscience and applied deep learning. Enhancing `cellfinder` will benefit labs worldwide by improving performance and flexibility. My hands-on experience, leadership in iGEM, and ability to work across software and biology make me a strong fit for this work.

---

### Availability
I am fully available (~20 hrs/week) from June 2 to July 21. From July 22 to September 15, I will be on military service but can continue work during weekends (~6–8 hrs/week). I plan to complete major deliverables early and stay in regular contact with mentors throughout.

---

## GSoC Experience
This is my first time applying to GSoC. I am applying only to BrainGlobe, as the project strongly aligns with my interests in computational neurobiology. I see GSoC as a valuable opportunity to learn from mentors and contribute meaningful code to the neuroscience community.
