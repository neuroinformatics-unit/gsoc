# BrainGlobe:  brainglobe-registration tool  (Richard Dushime Mudahera)

## Personal Details
- **Full name:** Richard Dushime Mudahera
- **Email:** mudaherarich@gmail.com
- **GitHub username:** richarddushime
- **Zulip username:** Richard Dushime
- **Location & time-zone:** Italy, GMT+1
- **Personal website / project portfolio:** [Personal Website]()
- **Code contribution:** 
  - [Automate collection of papers citing BrainGlobe tools #295](https://github.com/brainglobe/brainglobe.github.io/pull/295)  
- **Proposal discussion link**:  
  - [PR #: Proposal discussion for GSoC 2025]()  

## Project Proposal

### Synopsis
Image registration to standardized atlases is foundational for reproducible neuroscience, enabling cross-study comparisons of brain structure and activity. However, the manual selection of atlas subregions in brainglobe-registration introduces bottlenecks, inconsistencies, and scalability limits. This project will eliminate this critical barrier by developing automated, data-driven methods to identify optimal registration targets, accelerating workflows while enhancing accuracy and reproducibility.

### Problem: The Cost of Manual Selection

- Time Burden: Researchers spend hours adjusting 2D/3D atlas boundaries for each dataset.
- Human Bias: Inter-user variability compromises cross-lab reproducibility.
- Scalability Limits: Manual workflows are impractical for large-scale studies (e.g., whole-brain mapping or multi-experiment analyses).

### Solution: Intelligent, Adaptive Target Selection
I propose three complementary approaches to automate atlas region selection:
- Adaptive Grid Search: Systematically evaluate atlas subregions at multiple scales to identify the best match to the input data.

- Bayesian Optimization: Leverage probabilistic surrogate models to efficiently explore the parameter space, minimizing computational overhead.

- ML-Based Selection (Stretch Goal): Train lightweight models on atlas features (e.g., anatomical landmarks) to predict optimal regions.

### Impact

- Faster Analysis: Reduce registration setup from hours to seconds, enabling high-throughput pipelines.

- Improved Consistency: Eliminate human bias, ensuring uniform processing across datasets and labs.

- Democratization: Lower the expertise barrier, empowering non-specialists to perform atlas alignment.

### Deliverables

- Integrated Module: A Python API in brainglobe-registration for automated region selection, compatible with 2D/3D data.

- Benchmarking Suite: Quantitative evaluation of methods using:
  - Accuracy: Dice coefficient, landmark RMSE.
  - Efficiency: Runtime and memory usage.
  - Testing: Unit/integration tests on diverse neuroimaging datasets.

- User-Centric Resources:
  - Documentation: Tutorials, API references, and troubleshooting guides.
  - Blog Post: Interactive case study comparing automated vs. manual workflows, including time/accuracy metrics.

### Open-Source Value
Integrating into the widely adopted BrainGlobe ecosystem, this project will directly benefit neuroscientists analyzing data from platforms like light-sheet microscopes or volumetric imaging. Automation aligns with the community’s push toward standardized, scalable tools, fostering collaboration and accelerating discovery in fields like connectomics and neurodevelopment.

### Implementation Timeline

**Minimal Deliverables**:  
- Adaptive grid search implementation
- Bayesian optimization pipeline
- Benchmark framework with spatial overlap/RMSE metrics

**Stretch Goal**:  
- ML-based selector using pre-trained feature extractors

Below is the detailed 12-week timeline (30 hours per week) that includes investigation, coding, and documentation. The community bonding period is also included for preparatory work.

<table style="width:100%; border-collapse: collapse; font-family: Arial, sans-serif;">
  <thead>
    <tr style="background-color:rgb(18, 6, 50);">
      <th style="border: 1px solid #ccc; padding: 8px;">Week</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Tasks</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Deliverables</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Hours</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">Community Bonding</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Deep dive into the Atlas API, study brainglobe-registration code, and establish test datasets with mentors</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Pre-GSoC phase</td>
      <td style="border: 1px solid #ccc; padding: 8px;">20 hrs</td>
    </tr>
    <!--Week 1-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">1</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Problem Analysis <br>	- Audit manual selection patterns.<br>- Define search space parameters (bounds, resolution). </td>
      <td style="border: 1px solid #ccc; padding: 8px;">Design document outlining parameters.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">30 hrs</td>
    </tr>
    <!--Week 2-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">2</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Grid Search Implementation	<br>- Code adaptive grid search.
- Test on sample 2D/3D data.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Functional grid search prototype.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">35 hrs</td>
    </tr>
    <!--Week 3-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">3</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Bayesian Optimization	<br>- Research libraries (e.g., Optuna).<br>- Build pipeline with parallelization.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">BO prototype with convergence plots.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">35 hrs</td>
    </tr>
    <!--Week 4-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">4</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Benchmarking Setup<br>- Design evaluation framework.<br>- Implement DICE/RMSE metrics.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Benchmarking scripts.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">30 hrs</td>
    </tr>
    <!--Week 5-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">5</td>
      <td style="border: 1px solid #ccc; padding: 8px;">- Compare grid vs. BO performance.<br>- Draft API for the module.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Benchmark report, API draft.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">35 hrs</td>
    </tr>
    <!--Week 6-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">6</td>
      <td style="border: 1px solid #ccc; padding: 8px;"><strong>Mid-term Review</strong>: - Add error handling(partial FOV).<br>- Write integration tests.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Peer review and mentor feedback</td>
      <td style="border: 1px solid #ccc; padding: 8px;">30 hrs</td>
    </tr>
    <!--Week 7-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">7</td>
      <td style="border: 1px solid #ccc; padding: 8px;">	Documentation	<br>- Write user guides.<br>- Create Jupyter tutorials.</td>
      <td style="border: 1px solid #ccc; padding: 8px;"> Published tutorials</td>
      <td style="border: 1px solid #ccc; padding: 8px;">30 hrs</td>
    </tr>
    <!--Week 8-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">8</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Final Benchmarks	- Test across MRI/light-sheet datasets.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Cross-modality performance report.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">35 hrs</td>
    </tr>
    <!--Week 9-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">9</td>
      <td style="border: 1px solid #ccc; padding: 8px;">CI/CD Integration	- Set up GitHub Actions.<br>- Stress-test code.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Automated testing pipeline.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">30 hrs</td>
    </tr>
    <!--Week 10-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">10</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Conduct final performance comparisons across imaging modalities</td>
      <td style="border: 1px solid #ccc; padding: 8px;">35 hrs</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Ensure broad applicability</td>
    </tr>
    <!--Week 11-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">11</td>
      <td style="border: 1px solid #ccc; padding: 8px;">-Finalize code/docs. <br>- Address feedback.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Focus on stability and Polish codebase.</td>
      <td style="border: 1px solid #ccc; padding: 8px;">35 hrs</td>
    </tr>
    <!--Week 12-->
    <tr>
      <td style="border: 1px solid #ccc; padding: 8px;">12</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Finalize code and documentation; write a blog post showcasing case studies</td>
      <td style="border: 1px solid #ccc; padding: 8px;">35 hrs</td>
      <td style="border: 1px solid #ccc; padding: 8px;">Prepare for final project presentation</td>
    </tr>
    <!-- Week 13 -->
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">13</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
         - Stay active as a community contributor by addressing bugs, offering support, and enhancing features as needed.<br> - Provide assistance through forums, Zulip, and GitHub for users adopting the tool.<br> - Monitor feedback and plan follow-up in agreement with mentors.<br> - Act as a resource for new contributors and maintain a connection with mentors.
      </td>
      <td style="border: 1px solid #ccc; padding: 8px;">Continued Community Engagement</td>
      <td style="border: 1px solid #ddd; padding: 8px;">30</td>
    </tr>
  </tbody>
</table>

## Communication Plan

- **Mentor Meetings:** Hold weekly video or voice calls to discuss progress, challenges, and next steps.
- **Daily/Weekly Updates:** Share progress, Quick updates and blocker discussions via Zulip.
- **Documentation & Issue Tracking:** Use GitHub Issues and project boards(if preferred) to track tasks and milestones.
- **Code Reviews:** Submit regular or weekly pull requests to ensure the project stays on track and meets community standards.


## Personal Statement
### Past Experience
I have a strong background in Python, computer vision, and working with open-source projects. I started during my Bachelor’s in Information Systems by building a facial recognition system for taking class attendance. This project improved my skills in Python, image processing, and solving problems. Now, as a Master’s student in Data Science at the University of Messina, I focus on machine learning and research software engineering. I have also contributed to several open-source projects, including a Flask web app for WEHI’s Research Software Engineer Internship program. In addition, I have taken part in initiatives like FORRT (Framework for Open and Reproducible Research Training), The Turing Way, and Open Life Science. Attending events like the Collaborations Workshop 2024 and serving as Secretary for RSE Asia & Australia have strengthened my commitment to creating sustainable, community-driven software.

### Why This Project?
The manual selection of registration targets in brainglobe-registration is both time-consuming and prone to error, creating a bottleneck in neuroscientific analyses. I am passionate about developing tools that streamline research workflows and promote reproducibility. Automating the selection of atlas regions using methods such as adaptive grid search, machine learning techniques, or Bayesian optimization, this project promises to significantly enhance the efficiency and accuracy of image registration. I am excited about the opportunity to contribute to a solution that not only saves time but also makes advanced neuroinformatics techniques accessible to researchers.

### Why Me?
My skills in Python, numerical computing (NumPy), and foundational machine learning provides a solid base for developing and comparing automated region selection methods. I have experience in both research-level and production-quality code, and I am dedicated to producing clear, user-friendly software. I am eager to expand my skill set further—exploring frameworks and integrating modern optimization techniques—making me well-prepared to deliver a high-quality solution for this project.

### Availability
I am available full-time and can commit approximately 30 hours per week in line with GSoC guidelines, with additional buffer hours on weekends to address any unexpected challenges. This commitment ensures focused and consistent progress throughout the project.

### GSoC Experience
GSoC represents an exceptional opportunity to enhance my technical skills while contributing to a project that bridges innovative research and practical application. I look forward to collaborating with experienced mentors and the open source community, gaining valuable insights, and developing a tool that advances neuroinformatics by automating the registration process.

### Applying to Other Projects
I am applying exclusively within this community, with a strong interest in two projects:

- Brainglobe-registration: Automating atlas region selection to improve efficiency and reproducibility in neuroscientific analyses.

- Ethology (any-point tracking integration):

Both projects align with my skills, interests, and passion for creating accessible, advanced analysis tools for researchers.
