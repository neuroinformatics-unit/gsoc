# ethology: Low-shot detection for semi-automatic labelling (Rajat Kriplani)

## Personal Details

*   **Full name:** Rajat Kriplani
*   **Email:** krips.new@gmail.com
*   **GitHub username:** rajatkriplani
*   **Zulip username:** RajatKriplani
*   **Location & time-zone:** Asia/Kolkata (UTC+5:30)
*   **Personal website / project portfolio:** Project FLARE (Work in Progress) - [link](https://rajatkriplani.github.io/FLAREmob/)
*   **Code Contribution:**
    *   ethology: PR #74: Docs: Add guide for labelling with VIA tool ([Link to PR #74](https://github.com/neuroinformatics-unit/ethology/pull/74))
    *   ethology: PR #77: Feat: Add auto-detection for annotation file format (closes #43) ([Link to PR #77](https://github.com/neuroinformatics-unit/ethology/pull/77))
    *   ethology: PR #79: Docs: Add initial glossary (closes #25) ([Link to PR #79](https://github.com/neuroinformatics-unit/ethology/pull/79))

    *(I confirm these contributions represent my own work, incorporating valuable feedback and guidance received from the community.)*
*   **Proposal Discussion Link:**
    *   [Link to the PR discussing this proposal](https://github.com/neuroinformatics-unit/gsoc/pull/60)

---

## Project Proposal
### Synopsis
This project aims to integrate low-shot object detection into the ethology Python package to support semi-automatic labelling of bounding boxes for animal behaviour research. Manually annotating video data is often tedious and time-consuming, especially in settings with static cameras and uniform backgrounds. Low-shot detection models like GeCo and CountGD can detect objects from just a few labelled examples, making them well-suited for this task. The project will deliver a backend API for running inference and exporting annotations, along with a user-friendly Napari widget. The widget will allow users to load video frames, draw a few example annotations, run model inference on the rest of the data, and review or correct the results. This workflow will significantly reduce the effort required to create high-quality annotated datasets, accelerating research within the ethology ecosystem.

### Implementation Timeline

*   **Total Duration:** 12 Weeks (Standard GSoC)
*   **Estimated Weekly Hours:** Approx. 29-30 hours/week (to meet the ~350-hour project size)

**Minimal Deliverables:**

*   Backend functionality in `ethology` to run inference using at least one pre-trained low-shot detection model (e.g., GeCo), taking user-provided examples (prompts) as input and outputting an `ethology` annotation DataFrame.
*   Backend API designed to potentially support multiple similar models (e.g., CountGD).
*   A functional Napari widget that allows users to:
    *   Load image frames.
    *   Draw/select bounding boxes as examples ("prompts").
    *   Trigger backend inference using the chosen model.
    *   Display model-generated bounding boxes on the Napari canvas.
    *   Facilitate review and correction by leveraging Napari's built-in shape layer tools (e.g., for selecting, deleting, and modifying boxes) and allowing users to add new manual boxes where needed.
    *   Export the final set of annotations (manual + reviewed/corrected) in a format compatible with `ethology` (e.g., save to COCO JSON or directly as a DataFrame).
*   Unit tests covering the core backend functionality and essential widget interactions/workflow steps.
*   User documentation a step-by-step Guide and Example pages within the main ethology documentation detailing the workflow, usage of the Napari widget, and any model-specific considerations.

**Detailed Weekly Timeline:**

| Week | Dates (Approx. GSoC 2025) | Planned Tasks                                                                                                                                                              |
| :--- | :------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **CB** | (Community Bonding)       | Deep dive into GeCo & CountGD papers/code. Set up dev environment thoroughly. Experiment with Napari widget basics. Draft detailed API & preliminary widget UI mockups. Discuss designs with mentors. |
| 1    | Late May                  | Finalize API design for backend inference. Set up backend module structure in `ethology`. Implement basic image/annotation loading for backend function. Start Napari widget boilerplate (loading images). Write initial backend tests. |
| 2    | Late May/Early June       | Implement core inference logic for the first model (e.g., GeCo) in the backend, focusing on processing prompts and running model. Refine backend tests. Draft basic backend API usage docs (internal).                               |
| 3    | Early June                | Refine backend inference output to standardized DataFrame format. Add backend unit tests. Implement basic bounding box drawing/selection tool in Napari widget for creating prompts.        |
| 4    | Mid June                  | Integrate backend inference call into Napari widget. Display model output boxes on Napari canvas. Write initial integration tests & draft widget usage section for Guide.                                                                        |
| 5    | Mid/Late June             |Implement review/correction workflow using Napari's shape layer tools: enabling selection and deletion of model-generated boxes. Refine tests & Guide section for review features.                                                                               |
| 6    | Late June/Early July      | Enhance review workflow: leverage Napari tools for adjusting existing boxes, allow adding new manual boxes to correct misses. Ensure smooth interaction between layers. **(Midterm: Core workflow demonstrable)**                         |
| 7    | Early July                | Implement saving/exporting functionality for the final annotations from Napari. Refactor backend API for potential second model integration (if applicable). Write tests & docs for export.                             |
| 8    | Mid July                  | *If pursuing stretch goal:* Integrate second model (e.g., CountGD) OR *If sticking to minimal:* Add more robust testing for backend and frontend interactions.           |
| 9    | Mid/Late July             | Develop the Example demonstrating the full workflow. Refine and polish the Guide documentation.                                                                                                                 |
| 10   | Late July/Early August    | Thorough end-to-end testing. Bug fixing. Address identified edge cases (e.g., no detections, poor prompts, varying image conditions, performance with many frames/boxes, errors during model loading/inference).                                             |
| 11   | Early August              | Finalize all tests and documentation (Guide, and Example taking reference from 'movement').                          |
| 12   | Mid August                | Final code review buffer, final submission preparation, potentially create a short demo/screencast.                                                                                     |


## Communication Plan

I plan to communicate actively and transparently throughout the project. I am flexible and happy to adapt to the mentors' preferred schedule and methods.

---

## Personal Statement

### Past Experience

My programming foundation is in Python, with machine learning experience gained via a Coursera ML certification using TensorFlow (covering pipelines, evaluation, preprocessing). I am actively transitioning to PyTorch, focusing on research-relevant skills like `nn.Module`, dynamic graphs, `torchvision`, and `Datasets`/`DataLoaders`.

My open-source journey started with Hacktoberfest (Python contributions, testing), leading to active involvement in the Liquid Galaxy community. While the core [Liquid Galaxy repository](https://github.com/LiquidGalaxyLAB/liquid-galaxy) shows limited recent activity (the last PR was merged five years ago), the ecosystem thrives through community projects; I am an active contributor within this broader ecosystem, currently developing Project FLARE which focuses on leveraging platform capabilities. Recently, I've contributed documentation and features to `ethology` (PRs #74, #77, #79), gaining familiarity with its codebase, workflow, and Git/GitHub best practices.

While new to Napari plugin development, I am enthusiastic about learning it; my work on the UI/UX-focused Project FLARE provides transferable skills. My computer vision knowledge is foundational, built during ML studies, and I am actively learning more about object detection and transformers relevant to this project's low-shot context.

### Motivation: Why this project?

This project uniquely aligns my Psychology background with my technical interests in ML. Addressing the annotation bottleneck in ethology using low-shot detection resonates strongly with my understanding of behavioral research challenges. I am motivated by the technical CV problem itself, the chance to contribute to impactful open-source neuroscience tools, the opportunity to learn Napari plugin development, and the end-to-end nature of building both backend logic and a user-facing interface.

This work directly supports my goal of pursuing interdisciplinary projects where ML aids scientific discovery, particularly in behavioral sciences. Gaining practical experience in low-shot learning, applied CV, and scientific tool-building is key to my intended career path.

### Match: Why you?

My blend of technical skills, relevant academic context, and strong motivation makes me a good fit. Proven Python ability, foundational ML knowledge (TensorFlow, learning PyTorch), and practical open-source experience (`ethology`, Liquid Galaxy, Hacktoberfest) demonstrate my capacity to execute the project's technical aspects. My current PyTorch focus directly targets required skills (`nn.Module`, `torchvision`).

My Psychology studies offer crucial user empathy, enabling me to contribute to an intuitive Napari widget design that serves researchers effectively. This unique perspective, combined with an interest in full-stack development (backend models, frontend UI) and my passion for accessible science, positions me well to deliver a valuable tool for the `ethology` community while advancing my own interdisciplinary skills.

### Availability

I confirm I have no other significant commitments (coursework, jobs, internships, vacations) during the GSoC 2025 coding period (approx. May-August). I am prepared to fully dedicate the required time (approx. 30 hours/week) to this project.

---

## GSoC

### GSoC Experience

My primary expectations from the GSoC program are to gain invaluable real-world software development experience under the guidance of experienced mentors. I look forward to contributing code to a meaningful open-source project that has a direct impact on scientific research. I also expect to significantly improve my technical skills, particularly in PyTorch, computer vision, Napari development, and collaborative software engineering practices. Furthermore, I am excited by the prospect of helping to make advanced technology more accessible to researchers from diverse backgrounds.

### Other Applications

Yes, I am also applying to a project with the Liquid Galaxy organization for GSoC 2025.

Given my recent contributions to `ethology` and my strong interest in bridging my psychology background with computational neuroscience and computer vision, **my preference would be to work on this `ethology` project** if I were fortunate enough to receive offers from both organizations. While I value my involvement with the Liquid Galaxy community, this specific `ethology` project aligns more directly with my current learning objectives and long-term interdisciplinary goals.
