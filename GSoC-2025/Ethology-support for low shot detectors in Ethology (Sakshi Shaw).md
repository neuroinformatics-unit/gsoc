# Project title

Ethology: Support for low-shot detectors in ethology (Sakshi Shaw)

# Personal details

• Full name : Sakshi Shaw
• Email : Sakshishaw2004@gmail.com
• GitHub username : SakshiGits
• Zulip username : https://neuroinformatics.zulipchat.com/#user/882571
• Location & time-zone : India , IST (Indian Standard Time)
• Code contribution : https://github.com/neuroinformatics-unit/ethology/pull/84
• Proposal discussion link

# Project proposal

• Synopsis
What is the project about?
This project is about developing support for low-shot detector for ethology, Python package which aims to facilitate the application of a wide range of computer vision tasks to animal behaviour research. Low-shot detection is a computer vision task that aims to detect objects in images with very few labelled examples (between 0 and 5).
Why is it Important?
It can be useful to researchers in animal behaviour, but it is still somewhat inaccessible to them. For example, it could be particularly useful for collective animal behaviour research, where it may be tedious to obtain large labelled datasets for training accurate detection models. It could also be useful for labelling large datasets collected in the lab, where the collected frames are relatively similar in appearance, as it is common to record videos of animals with static cameras and relatively uniform backgrounds.

# Minimal set of deliverables include:

- Developing backend functionality with a consistent and user-friendly API that allows users to load manually labeled bounding boxes for an object of interest, run inference using a low-shot detection model to identify identical instances across the dataset, allow user to review and refine the predicted annotations, and export the results as a structured ethology annotation dataframe.
- Designing a GUI using a Napari widget where users can load extracted video frames, annotate objects, trigger model inference, and interactively review or edit the results — all within an intuitive interface.
- Integrating Unit Tests and Documentation/Guide for all features added.
- Stretch goal: Integrate text-based prompting into the Napari widget, which will run inference using CountGD in text mode enabling users to specify target objects using descriptive text.

# Implementation Timeline

| Weeks     | Dates           | Planned Tasks                                                                                          |
| --------- | --------------- | ------------------------------------------------------------------------------------------------------ |
| (Phase 0) | April 8 – May 8 | Get familiar and experiment with Napari and PyTorch. Delve into GeCo and CountGD papers and codebases. |

| Community Bonding | May 8 – June 1 | Set up the development environment. Discuss and draft detailed backend logic and pseudocode. Create Napari widget wireframes. |

| Week 1 – Week 2 | June 2 – June 15 | Finalize backend API structure. Set up module layout and implement basic utilities for image loading and annotation parsing. Start developing Napari widget with image loading support. |

| Week 3 – Week 4 | June 16 – June 29 | Write unit tests for image loading and annotation functionality. Implement core inference logic for the low-shot detection model (GeCo). Add unit tests for it. |

| Week 5 – Week 6 | June 30 – July 13 | Integrate backend with Napari widget. Display predicted bounding boxes in the viewer. Add functionality for review/edit/delete of the output predicted boxes. |

| Midterm Evaluations | July 14 – July 18 | Submit midterm evaluation. Receive feedback from mentors. Refactor code based on suggestions. |

| Week 7 – Week 8 | July 14 – July 27 | Perform tests for Napari widget. Format model output datasets to ethology annotation dataframe. _Stretch goals:_ Add text-based prompting feature to widget. Refactor backend for CountGD. |

| Week 9 – Week 10 | July 28 – August 10 | Add tests for CountGD integration. Polish user-facing documentation (Napari usage, backend API guide). Begin end-to-end testing. |

| Week 11 – Week 12 | August 11 – August 25 | Final polish and cleanup by addressing mentor feedback. Fix final bugs. Prepare and submit final deliverables. |

# Communication plan

I aim to maintain regular and proactive communication with my mentor throughout the project. I will use Zulip and provide short progress updates at least 2–3 times a week.

# Personal statement

I thrive in projects that blend creativity with technical depth, and I see contribution to Ethology as a chance to grow through real-world collaboration. I’m excited to contribute meaningfully while learning from an open-source community pushing the boundaries of science and tech.

# Past experience.

I was introduced to computer vision during my coursework, I’ve developed several minor projects that involved applying computer vision techniques in areas such as object detection, image processing.

# Motivation: why this project?

I find the goals of the Ethology package deeply impactful and am drawn to how it leverages computer vision to facilitate animal behavior research. This project aligns perfectly with my goal of gaining hands-on experience in applied computer vision— learning and contributing to areas such as few-shot object detection, Napari GUI development.

# Match: why you?

I’ve already familiarized myself with the ethology codebase and submitted a PR to implement a new feature, which gave me hands-on insight into its structure and contribution workflow. My background includes coursework and mini-projects in computer vision, where I’ve worked with tools like PyTorch, OpenCV, and NumPy. Driven by intrest and a strong desire to learn, I’m confident in my ability to contribute meaningfully to this project.

# Availability

I have my summer break during the GSoC work period, so I will be fully available without any conflicting commitments.

# GSoC experience

I hope to gain hands-on experience collaborating on a real-world open-source project, deepen my skills, through guidance from experienced mentors.

# Are you also applying to projects with other organisations in GSoC 2025?

No, I’m only applying to Neuroimformatics Unit (Ethology).
