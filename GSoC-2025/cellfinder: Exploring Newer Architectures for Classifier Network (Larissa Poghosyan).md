# cellfinder: Exploring Newer Architectures for Classifier Network (Larissa Poghosyan)

## Personal details
Please include the following information:
- **Full name** Larissa Poghosyan
- **Email** larissa.poghosyan@gmail.com
- **GitHub username** larissapoghosyan
- **Zulip username** Larissa Poghosyan (User ID 891828)
- **Location & time-zone** London, UK (GMT+1 British Summer Time)
- **Personal website / project portfolio** https://github.com/larissapoghosyan
- **Code contribution**
    - https://github.com/brainglobe/cellfinder/pull/495
      
      This Pull Request adds a significant part of the Vision 
      Transformers implementation for the classifier network in `cellfinder` project. It's completely compatible with the current abstractions of the library.

- **Proposal discussion link**
    - https://github.com/brainglobe/cellfinder/pull/495
      I used the same PR at the original repository to show the proof-of-concept implementation, list todos, and to invite the community to discussion.

## Project proposal 
_Length: max 1 page_

- **Synopsis**

    Accurate detection of labelled cells in whole mouse brain 3D microscopy images is a key step in understanding brain-wide neural circuits. While simple thresholding can be used to extract candidate cell locations, it typically yields a high false positive rate.

    Currently, `cellfinder` use this approach for candidate extraction, followed by a 3D ResNet-based classifier to distinguish true cells from artefacts using local image cuboids. However, recent advances in computer vision demonstrate that Vision Transformers (ViTs) outperform convolutional networks like ResNet in many biomedical image classification tasks.
    
    This project aims to replace cellfinder’s ResNet classifier with a ViT-based architecture, improving detection accuracy and robustness across brain regions without increasing computational cost.
    
    Additionally, it would be beneficial to implement the changes and new architectures with the same abstractions to ensure backward compatibility. This way, existing user workflows will remain unaffected, allowing seamless transitions to newer architectures and improved quality and performance.

- **Implementation timeline**

    - [x] Implement ViT in Keras
    - [x] Make sure backward compatibility, and have unified abstractions for classifier network 
    - [ ] Performance testing on CPUs and GPUs
    - [ ] Quantitative comparison with current ResNet classifier
    - [ ] Changes in BrainGlobe repo using Cellfinder to expose the new functionality
    - [ ] Add pre-train and fine-tune pattern 
    - [ ] Add support of pretrained backbone models (load backbone and continue fine-tune)
    - [ ] Add unit tests to cover all the changes
    - [ ] Add documentation
    - [ ] Write a blogpost
    - [ ] 2D support for ViT 

    ---

    | **Week**      | **Phase**         | **Dates**         | **Deliverables**   |
    |---------------|-------------------|-------------------|--------------------|
    | **Week 0**    | COMMUNITY BONDING | May  8  -  Jun  1 | - Refine the existing ViT implementation (current PR).<br>- Start testing on large-scale data.<br>- Finalize benchmarking plan and GPU setup.<br>- Monitor upstream PRs (e.g. #493) for compatibility. |
    | **Week 1**    |                   | Jun  2  -  Jun  9 | - Add ViT model configs to the training pipeline.<br>- Set up experiment tracking (e.g. with Weights & Biases) and create a public project board.<br>- Launch full-scale training runs on GPU. |
    | **Week 2**    |                   | Jun 10  -  Jun 16 | - Begin performance analysis on CPU vs GPU.<br>- Collect accuracy, loss, and training speed metrics.<br>- Compare with current ResNet model.<br>- Log results to experiment tracker. |
    | **Week 3**    |                   | Jun 17  -  Jun 23 | - Add support for loading pretrained 3D ViT backbones.<br>- Implement fine-tuning mechanism.<br>- Test with public pretrained ViTs (if available). |
    | **Week 4**    |                   | Jun 24  -  Jun 30 | - Modularize architecture selection in CLI, Python API, and Napari plugin.<br>- Continue benchmarking on multiple datasets.<br>- Polish training scripts/configs. |
    | **Week 5**    | PRE-MIDTERM PREP  | Jul  1  -  Jul  7 | - Finalize and analyze benchmarking results (ViT vs ResNet).<br>- Sync with mentors for midterm prep.<br>- Address any issues in API/plugin integration. |
    | **Week 6**    | MIDTERM           | Jul  8  -  Jul 14 | - Submit midterm evaluation.<br>- Share benchmarking summary and gather feedback.<br>- Plan next steps with mentor input. |
    | **Week 7**    |                   | Jul 15  -  Jul 21 | - Write unit tests for ViT classifier pipeline.<br>- Ensure compatibility with data loader refactor (`#493`).<br>- Begin writing user/developer documentation. |
    | **Week 8**    |                   | Jul 22  -  Jul 28 | - Finalize documentation (training, fine-tuning, CLI usage).<br>- Add lightweight support for 2D classification mode.<br>- Validate on small 2D image slices. |
    | **Week 9**    |                   | Jul 29  -  Aug  4 | - Add support for advanced ViT variants (DeiT, DINO, Swin).<br>- Integrate backbone selection cleanly into training pipeline.<br>- Run test training on at least one variant. |
    | **Week 10**   |                   | Aug  5  -  Aug 11 | - Complete variant model testing and collect comparison results.<br>- Final cleanup of codebase, refactor and organize files.<br>- Validate full test coverage and model switching. |
    | **Week 11**   |                   | Aug 12  -  Aug 18 | - **Code freeze**: finalize codebase for submission.<br>- Write and publish final blog post summarizing work, results, and next steps. |
    | **Week 12**   | FINAL WEEK        | Aug 19  -  Sep  1 | - Submit final GSoC report and code.<br>- Review and respond to mentor feedback.<br>- Ensure documentation is contributor-friendly and future-ready. |

- **Communication plan**

    I’d prefer to have **weekly video calls (around 20–30 minutes)** with my mentors to check in on progress, ask questions, and plan next steps. I think this cadence works well, but I’d be genuinely happy to meet more often if the mentors are available and open to it. For day-to-day communication and quick feedback, I’ll use Zulip, where I’ll stay active and responsive throughout the program.

## Personal statement

_Length: max 0.75 page_

- **Past experienc.** 

    Please describe your past experience with programming, open source, or any other experience you deem relevant for the project you are applying for. Any successful open source projects, published work or content of the like should definitely be highlighted.
- **Motivation: why this project?**

    Why are you interested in this specific project? What aspects of it motivate you to work on it? How does it link to your personal or professional interests? How do you envision its impact in the open source community?
- **Match: why you?**

    Why should we choose you for this project? What unique skills or experiences can you bring to the project and the community? Is there something you have worked on in the past that makes you particularly well-suited for this project?
- **Availability**

    I am fully available from **May 1 to October 1** with no academic or professional commitments during this time. I plan to dedicate **20–25 hours per week** throughout the program, in line with the **175-hour project** requirement. I’m also flexible to put in extra hours if needed to meet deadlines or polish the final deliverables.

## GSoC

_Length: max 0.25 page_

- **GSoC experience**

    I’m excited about GSoC as a way to contribute to meaningful open-source work and become part of a global community. Working on Cellfinder will allow me to collaborate closely with mentors and researchers, while learning how software can drive scientific discovery.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    I initially considered several organizations and explored PyDataStructs by Open Science Labs, where I authored a pull request and made some changes. However, I ultimately decided to focus solely on the Cellfinder project to ensure I have meaningful contributions and a strong proof of concept before applying.
    I will not be applying elsewhere within GSoC program this year.
