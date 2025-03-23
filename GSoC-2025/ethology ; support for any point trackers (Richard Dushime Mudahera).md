# ethology: Support for Any-Point Tracking (Richard Dushime Mudahera)

## Personal Details
- **Full name:** Richard Dushime Mudahera
- **Email:** mudaherarich@gmail.com
- **GitHub username:** richarddushime
- **Zulip username:** Richard Dushime
- **Location & time-zone:** Italy, GMT+1
- **Personal website / project portfolio:** [Personal Website]()
- **Code contribution:** 
    - [Add basic setup for documentation #56](https://github.com/neuroinformatics-unit/ethology/pull/56)
    - [Set up dependabot to check for updates in GH actions PR #64](https://github.com/neuroinformatics-unit/ethology/pull/64)
    - [supporting image registration with Elastix #66 --In progress](https://github.com/neuroinformatics-unit/ethology/pull/66)

- **Proposal discussion link:** [Discussion PR # ]()

## Project Proposal

### Synopsis
Animal behavior research increasingly relies on computer vision, yet advanced tools like any-point tracking—which tracks arbitrary points in videos—remain underutilized due to accessibility gaps. While pose estimation focuses on predefined anatomical keypoints, any-point tracking offers dynamic, flexible analysis, enabling researchers to study novel behaviors, environmental interactions, or ad-hoc body parts. 

### What is the project about?
This project integrates any-point tracking—a computer vision (CV) technique that tracks arbitrary points in videos—into Ethology, an open-source framework for analyzing animal behavior. Unlike traditional pose estimation (which tracks fixed anatomical keypoints), any-point tracking allows researchers to dynamically select points (e.g., limbs, environmental objects) and trace their motion across video frames.

### Why is it important?

- Flexibility: Enables tracking of novel behaviors (e.g., tool use, social interactions) not limited to predefined body parts.
- Accessibility: Democratizes advanced CV tools for biologists/ecologists without coding expertise.
- Efficiency: Reduces manual annotation effort, accelerating data analysis for large datasets (e.g., long-term behavioral studies).

### Goals

- Provide a user-friendly interface (via Napari) to run any-point tracking on animal videos.
- Generate and visualize trajectories for quantitative analysis (e.g., movement patterns, kinematics).
- Strengthen Ethology’s ecosystem as a unified hub for diverse CV-driven behavioral analysis.

### Deliverables

- A Napari widget for point selection, model inference (TAPIR/CoTracker), and trajectory visualization.
- Back-end integration to process videos and convert outputs into Ethology-compatible datasets.
- Tools to analyze/export trajectories (CSV, HDF5) and documentation for end-users.

### Open-Source Benefits

- Interoperability: Ethology’s modular design will allow integration with existing CV tools (e.g., DeepLabCut, SLEAP).
- Collaboration: Lowers barriers for biologists to contribute to leverage cutting-edge CV advancements.
- Innovation: Encourages community-driven extensions (e.g., multi-animal tracking, 3D motion analysis).

## Implementation Timeline

##### Minimal Deliverables

- Core Napari Widget:
  - Load videos (MP4, AVI).
  - Select query points via GUI.
- Backend Integration:
  - Connect widget to pre-trained models (TAPIR/CoTracker).
  - Extract trajectories into Ethology-compatible datasets.
- Trajectory Visualization:
  - Overlay paths on video with customizable styles.

##### Stretch Goals

- In-Widget Inference: Run tracking directly in Napari.
- Trajectory Correction Tools: Manual editing of paths post-tracking.
- Multi-Model Support.
- Batch Processing: Track points across multiple videos.
- Benchmarking Suite: Compare model accuracy on animal datasets.

<table style="width:100%; border-collapse: collapse; font-family: Arial, sans-serif;">
  <thead>
    <tr style="background-color:rgb(5, 3, 26);">
      <th style="border: 1px solid #ddd; padding: 8px;">Week</th>
      <th style="border: 1px solid #ddd; padding: 8px;">Task Description</th>
      <th style="border: 1px solid #ddd; padding: 8px;">Deliverables</th>
      <th style="border: 1px solid #ddd; padding: 8px;">Hours/Week</th>
    </tr>
  </thead>
  <tbody>
    <!-- Community Bonding Period (Pre-GSoC) -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Community Bonding</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        Engage in discussions on Zulip and GitHub, contribute minor bug fixes, and review napari plugins and documentations (including cotracker3 and TAPIR).
      </td>
      <td style="border: 1px solid #ddd; padding: 8px;"></td>
      <td style="border: 1px solid #ddd; padding: 8px;"></td>
    </tr>
    <!-- Week 1 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">1</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Widget Foundation</strong> - Create basic Napari widget skeleton.<br>- Implement video loading and frame navigation.
      </td>
      <td style="border: 1px solid #ddd; padding: 8px;">Functional widget loads videos.</td>
      <th style="border: 1px solid #ddd; padding: 8px;">20</th>
    </tr>
    <!-- Week 2 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">2</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Point Selection & Backend:</strong> - Add point selection UI.<br>- Store query points as metadata.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Users can select/delete points.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 3 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">3</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Model Integration:</strong>- Integrate TAPIR/CoTracker inference pipeline.<br>- Handle GPU/CPU compatibility.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Points passed to model, raw trajectories generated.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 4 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">4</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Trajectory Extraction:</strong>- Convert model outputs to Pandas DataFrames.<br>- Add timestamps and point IDs.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Trajectories saved in Ethology format.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 5 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">5</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Visualization Layer:</strong>- Overlay trajectories on video.<br>- Add color-coding and path smoothing.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Interactive playback with paths.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 6 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">6</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Mid-Term Review:</strong> - Optimize performance (e.g., frame caching).<br>- Write unit tests for core features.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">50% of code tested, demo video.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 7 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">7</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Export & Analysis:</strong> - Add CSV/HDF5 export.<br>- Integrate with Ethology’s stats modules.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Trajectories usable for velocity/heatmap analysis.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 8 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">8</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Documentation & CI/CD:</strong>- Write user guides.<br>- Set up GitHub Actions for testing.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Docs draft, automated tests pass.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 9 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">9</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Stretch: In-Widget Inference:</strong>- Add model selection dropdown.<br>- Enable progress bars for tracking.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Users run models without CLI.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 10 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">10</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Stretch: Trajectory Correction:</strong>- Add GUI tools to edit paths.<br>- Implement undo/redo functionality.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Manual corrections saved.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 11 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">11</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Code Freeze & Testing:</strong>- Fix edge cases (e.g., occlusions).<br>- Stress-test on large videos.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Beta version released.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 12 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">12</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <strong>Finalization:</strong>- Polish UI/UX.<br>- Finalize tutorials and API docs.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Code merged, presentation ready.</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
    <!-- Week 13 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">13</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
         - Stay active as a community contributor by addressing bugs, offering support, and enhancing features as needed.<br> - Provide assistance through forums, Zulip, and GitHub for users adopting the tool.<br> - Monitor feedback and plan follow-up in agreement with mentors.<br> - Act as a resource for new contributors and maintain a connection with mentors.
      </td>
      <th style="border: 1px solid #ddd; padding: 8px;">Continued Community Engagement</th>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
  </tbody>
</table>

### Key Milestones

- Week 3: First end-to-end tracking prototype.
- Week 6: Mid-term review with core features functional.
- Week 9: Stretch goals implementation begins.
- Week 12: Project submission with full test coverage.

### Communication Plan
- **Mentor Meetings:** Hold weekly video or voice calls to discuss progress, challenges, and next steps.
- **Daily/Weekly Updates:** Share progress and ask quick questions on Zulip.
- **Documentation & Issue Tracking:** Use GitHub Issues and project boards to track tasks and milestones.
- **Code Reviews:** Submit regular or weekly pull requests to ensure the project stays on track and meets community standards.

## Personal Statement

### Past Experience
I have built a good foundation in Python and computer vision by working on several open source projects. My contributions to NIU repositories show that I can work well with open source communities. While I am still learning machine learning and using PyTorch, I am eager to learn more. I have worked on projects that required both research-level and production-quality code. I have also collaborated with Research Software Engineers and participated in events like the Collaborations Workshop 2024, which has deepened my interest in software sustainability and research projects and tools.

### Motivation: Why This Project?
Animal behavior research faces challenges because many tools are too strict and do not work well with non-model organisms or new types of behaviors. Any-point tracking is a new approach that can help researchers study animals more easily by tracking any point on the animal in a video, not just fixed body parts. Ethology’s goal of unifying different computer vision tasks under one easy-to-use interface matches my belief that accessible tools can boost scientific discovery. I am excited about this project because it can help researchers ask new questions and gain better insights into animal behavior.

### Match: Why Me?
I have solid skills in Python, and I am learning more about machine learning and data visualization. My experience in writing clear and useful code, both for research and for production, makes me a good fit for this project. I am eager to learn more and learn about the napari ecosystem and to use my skills to build high-quality software that meets the needs of animal behavior research. I believe my background and passion for open-source development will help me make a positive contribution to this project.

### Availability
- Full-time Commitment: 30+ hrs/week, with no vacations/conflicts.
- Contingency Plan: Buffer hours into weekends to accommodate unexpected delays.

## GSoC

### GSoC Experience
I view GSoC as a unique opportunity to enhance my skills and contribute to a project that bridges cutting-edge research with practical applications. I am eager to collaborate with  mentors and the open source community, learn from their experience, and contribute to a tool that can make a real difference in the field of animal behavior research.

### Applying to Other Projects
I am applying to two projects under the Neuroinformatics Unit:

- Ethology (any-point tracking integration).

- Brainglobe-registration.

Due to their direct alignments with my skills and interests and passion for making advanced analysis tools accessible to researchers.
