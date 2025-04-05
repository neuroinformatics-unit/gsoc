# Cellfinder: 2D Image Support for Cell Detection (Arif Sultan)

#### Full name: Arif Sultan
#### Email: b24bs1058@iitj.ac.in
#### GitHub username: msp99000
#### Zulip username: arif_sultan
#### Location & time-zone: Jodhpur, India (IST, UTC+5:30)

---

## Code contribution

I solved an issue in BrainGlobe related to Windows CI by optimizing the TEMP path to improve performance and prevent disk space issues. The pull request is [#141](https://github.com/brainglobe/brainglobe-workflows/pull/141), and it has been merged.

---

## Proposal discussion link

[Discussion on Github](https://github.com/neuroinformatics-unit/gsoc)

---

## Project proposal

### Synopsis

This project aims to extend the BrainGlobe tool `cellfinder`, which currently detects cells in large 3D brain images, to also support two-dimensional brain slice images commonly used by neuroscientists. While the existing pipeline uses a 3D ResNet-based classifier, adapting it for 2D data will involve developing a new neural network architecture and modifying the image processing (blob detection) code to handle both 2D and 3D formats. The deliverables include updated algorithms, a new 2D classifier, test coverage, documentation, and a blog post showcasing the use of `cellfinder` on 2D images. This enhancement will significantly broaden `cellfinder`’s usability, enabling researchers with simpler imaging setups to automate cell detection, and strengthen its role as a versatile tool within the open-source neuroimaging community.

---

## Implementation timeline

### Minimal set of deliverables

- **2D blob detection support**: Implement dimension-agnostic preprocessing steps, create parallel pipelines based on input dimensionality, and ensure consistent output formats.
- **2D neural network classifier**: Build a lightweight PyTorch model (e.g., U-Net or modified ResNet) tailored to detect cellular structures in 2D slices.
- **Integration into `cellfinder`**: Modify classification logic for dual 2D/3D support while maintaining backward compatibility.
- **Testing and documentation**: Add unit tests and write developer/user documentation.
- **Outreach**: Publish a blog demonstrating 2D pipeline results with visuals and examples.

---

### Timeline & Weekly Plan

| **Phase**             | **Week & Dates**           | **Tasks**                                                                                                                                           | **Hours/Week** |
|-----------------------|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| **Community Bonding** | Week 1 (May 8 – May 14)     | Study `cellfinder` architecture. Analyze blob detection pipeline. Plan 2D adaptation strategy.                                                       | 25–30          |
|                       | Week 2 (May 15 – May 21)    | Research 2D neural architectures. Prototype simple CNNs. Prepare datasets and evaluation metrics.                                                    | 25–30          |
|                       | Week 3 (May 22 – June 1)    | Finalize architecture choice. Design dev and test setup. Prepare roadmap.                                                                           | 20–25          |
| **Coding Phase 1**    | Week 4 (June 2 – June 8)    | Adapt blob detection to 2D. Write dimension-agnostic preprocessing logic. Set up initial unit tests.                                                | 30–35          |
|                       | Week 5 (June 9 – June 15)   | Finalize blob detection pipeline. Add routing for 2D/3D differentiation. Improve test coverage.                                                      | 30–35          |
|                       | Week 6 (June 16 – June 22)  | Implement 2D classifier model. Set up training and validation loops. Begin running benchmarks.                                                       | 30–35          |
|                       | Week 7 (June 23 – June 29)  | Finish model training. Validate accuracy. Compare with 3D baseline where applicable.                                                                 | 30–35          |
|                       | Week 8 (June 30 – July 6)   | Integrate classifier with blob detection and preprocessing. Build end-to-end 2D pipeline.                                                            | 25–30          |
|                       | Week 9 (July 7 – July 13)   | Optimize integration. Refactor for clarity. Add more 2D tests and expand CI coverage.                                                                | 30–35          |
| **Coding Phase 2**    | Week 10 (July 14 – July 20) | Complete testing and model tuning. Write API and integration documentation.                                                                          | 30–35          |
|                       | Week 11 (July 21 – July 27) | Finalize all deliverables. Polish code and user guides.                                                                                              | 25–30          |
|                       | Week 12 (July 28 – Aug 3)   | Start writing demo blog post. Prepare figures, code snippets, and tutorials.                                                                        | 25–30          |
| **Finalization**      | Week 13 (Aug 4 – Sept 1)    | Finalize documentation and blog. Address feedback. Submit final report and wrap up contributions.                                                    | 20–25          |

---


## Time commitment

**25–35 hours per week**. I can dedicate full-time effort to this project throughout the GSoC coding period.

---

## Communication plan

To ensure transparency and collaboration, I will:

- Share regular updates via GitHub issues and pull requests
- Participate in biweekly mentor sync-ups via video calls
- Stay active on Zulip for daily communication and quick clarifications
- Write clear, maintainable code with thorough documentation

---

## Personal statement

### Past experience

I have a solid foundation in Python and NumPy, with practical experience using PyTorch and Keras for building deep learning models. At IIT Jodhpur, I’ve worked on academic and personal projects involving image classification, medical imaging, and real-time systems. I won a hackathon organized by IIT Jodhpur and AIIMS Jodhpur by developing a real-time blood coagulation monitoring system using deep learning. ([Certificate link](https://drive.google.com/file/d/1GnRyScF5NUHh62EgA0NvaPuFcARD37tb/view?usp=drivesdk))

I am also proficient with Git and collaborative workflows, regularly contributing to structured codebases. My ability to grasp unfamiliar code, refactor logic, and build testable components makes me confident in successfully delivering this project.

---

## Motivation: Why this project?

This project intersects my passion for machine learning, image processing, and neuroscience. Extending `cellfinder` to support 2D data significantly lowers the barrier to entry for many neuroscience labs. I’m deeply motivated to contribute to a widely used open-source tool that directly supports scientific research and reproducibility. Being part of this effort excites me because of its real-world impact and technical depth.

---

## Match: Why you?

I bring a strong background in Python, deep learning, and image processing. I’ve contributed to BrainGlobe's CI workflows and am familiar with the development stack. My experience with training models, handling image data, and writing maintainable code aligns well with the scope of this project. I am proactive, collaborative, and passionate about contributing to research-oriented open-source tools.

---

## Availability

I am available full-time for GSoC and have no other major commitments. I can dedicate 25–35 hours per week consistently and adjust based on mentor availability or project needs.

---

## GSoC experience

I see GSoC as a chance to grow as a developer while contributing to a meaningful open-source project. I hope to deepen my skills in collaborative software development, learn from experienced mentors, and make long-lasting contributions to the BrainGlobe community. I aim to continue contributing beyond GSoC and expand my involvement in neuroinformatics tools.

---

## Other applications

I am applying **exclusively** to this BrainGlobe project for GSoC 2025. My full focus will be on successfully completing and delivering all milestones of this proposal.
