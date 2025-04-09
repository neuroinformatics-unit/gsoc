# Datashuttle: Deploy Datashuttle as an installable package (Lucas Laredo)  

## Personal details
- **Full name** Lucas Rocha Laredo
- **Email** devlucaslaredo@gmail.com
- **GitHub username** [laredoo](https://github.com/laredoo/)
- **Zulip username** [Lucas Laredo](https://neuroinformatics.zulipchat.com/#user/890277)
- **Location & time-zone** Belo Horizonte, Brazil & GMT-3 (BRT)
- **Personal website / project portfolio** [GitHub Portfolio](https://github.com/laredoo/)
- **Code contribution**

    [feat: Ignore files from transfer](https://github.com/neuroinformatics-unit/datashuttle/pull/504) that addresses [#350](https://github.com/neuroinformatics-unit/datashuttle/issues/350)

    [feat: Allow Google Drive as remove storage](https://github.com/neuroinformatics-unit/datashuttle/pull/502) an early implementation of [#407](https://github.com/neuroinformatics-unit/datashuttle/issues/407)


- **Proposal discussion link**

    [#46](https://github.com/neuroinformatics-unit/gsoc/pull/46)

## Project proposal 

- **Synopsis**

    Datashuttle currently relies on dependency and environment managers (i.e. Conda, uv, Poetry) to use. In order to ensure more accessibility for those without coding skills, this proposal aims to implement an executable version to all available platforms. 
  
  **Deliverables:**

1. Research approaches for cross-platform distribution of Datashuttle
2. A proof of concept (PoC) implementing the researched packages/approaches for cross-platform distributions
4. A retrocompatible version of Datashuttle implementing a version using the best cross-platform executable package.
5. Updated documentation and tests (unit/integration) implementation in the project's GitHub CI

   **Stretch Goals:**
   
1. A Datashuttle web application version. This means implementing an early Datashuttle REST API and a front-end web interface.
2. Containerize (using Docker) both the REST API and web interface to facilitate deployment.

- **Implementation timeline**

| Week  | Tasks | Expected Outcome | Notes | Hours |
|----|--------------------| --------------------- | --------------------- | ----|
| Community Bounding | Project refinement: Discuss the proposal with the mentor and understand/plan the best approach. Further familiarize with the project standards and expected results. | Refined implementation timeline and project objectives. Alignment with mentor’s expectations. | Review existing documentation, previous discussions, and best practices of the project. Engage more with the community through Zulip and mailing lists. | 15h/20h |
| Week 1 | Start researching different cross-platform distribution methods. | Summary of researched methods with evaluated community adoption and best practices. | This is a less coding and more researching stage. The goal is to compare consolidated packages, (i.e. PyInstaller, Briefcase and Nuitka) and evaluate them in terms of compatibility, performance, and ease of use. Summarize findings in a document. | 20h |
| Week 2 | Compatibility tests across different OS environments comparing the approaches. | Final selection of the distribution method and initial documentation draft. | This week leads the decision on the Proof of Concept approach, and possibly the final solution. Differently from previous week, more coding and testing is involved. These are crucial weeks and needs attention. As mentioned, it will lead to the final solution, thus the research stage must be taken carefully. | 20h |
| Week 3 | Final decision on the best approach for the PoC. Start effectively writing documentation. | It's expected a concrete decision on PoC approach with a well-defined documentation structure explaining the chosen solution and its rationale.| After two weeks of research and testing, a final solution should be selected. The main risk is reaching this stage without a clear decision. If that happens, there’s still time to reassess feasibility, adjust the timeline, or pivot to an alternative approach. | 20h |
| Week 4 | Start implementing PoC based on selected method, identify roadblocks. | Initially working PoC and a list of encountered development challenges. | By this point, feasiability has already been validated. Week 4 marks the start of actual coding, as all in-depth research and solution selection are complete. Expected challenges will likely be technical (coding barriers), rather than functional (project scope is already set).| 20h |
| Week 5 | Start testing on-going PoC implementation on cross-platforms. Test it on Windows, macOS, Linux, and refine as needed. | Partially functional PoC with OS test results. | By this stage, it’s crucial to have a first working cross-platform version. The PoC doesn't need to be fully functional yet, but it should demonstrate compatibility and be moving in the right direction. Refinements will be iterative. | 20h |
| Week 6 | 	Finalize PoC implementation. | Functional PoC with OS test results. | By this stage, the PoC should be stable and validated across all targeted platforms. Any remaining blockers should be documented with a plan for resolution. This Proof of Concept will be presented as definitive to the mentor as one of the partial deliveries, so it is meaningful that it is representative and working. | 20h |
| Week 7 | Begin integrating the selected method into Datashuttle, ensuring it works smoothly within the existing architecture. |  Initial integration of the PoC, focusing on key components (TUI, validation module, transfer module). Performance impact assessment and early-stage compatibility testing. | This phase marks the transition from a standalone PoC to a fully integrated feature in Datashuttle. The TUI (built with Textual) should be tested to ensure it functions correctly without relying on package managers like Conda. | 20h |
| Week 8 | Conduct extensive testing on different system configurations (Windows, macOS, Linux). Address compatibility issues and refine integration. | Verified cross-platform compatibility with performance benchmarks. Identified and resolved major integration issues. | This stage ensures that Datashuttle, with the new distribution method, runs smoothly across various operating systems and hardware configurations. Tests should cover both TUI functionality and core modules (validation, transfer, etc.), ensuring usability for neuroscientists without requiring manual setup. | 20h |
| Week 9 | Validate/Optimize performance. | Performance benchmarks showing minimal overhead. Optimized execution time and resource usage. | Since it’s crucial that the solution does not impact other functionalities, this week focuses on the final exhaustive performance testing. The three-week testing schedule ensures that every aspect—TUI, validation, and transfer modules—is assessed. | 20h |
| Week 10 | Document all integration. Start writing unit and integration tests. | Comprehensive documentation covering project decisions and implementation details. Initial test suite targeting core functionalities. | After several weeks of intensive testing and implementation, this week provides a structured break by shifting the focus to documentation and test writing. | 20h |
| Week 11 | Conduct final cross-platform testing, address major bugs, engage with the community for feedback. | Issue tracking report with categorized bugs and fixes. Community feedback summary with actionable insights. | This phase ensures that Datashuttle is stable across all target platforms. Engaging with the neuroscience community provides valuable insights for refining the user experience, especially for non-technical users. | 20h |
| Week 12 | Set up and refine CI/CD pipeline to run automated tests | Working GitHub Actions pipeline that executes cross-platform testing. | The goal is to have a fully automated process that runs on every commit, ensuring stability. | 20h |
| Week 13 | Extend CI pipeline to build executables for Windows, macOS, and Linux. | Automated builds generating standalone executables on every commit. | Ensures that the app is always buildable and allows testing real binaries before release. | 20h |
| Week 14 | Set up GitHub Actions to publish a new release only when a new tag is pushed. | Fully automated release pipeline that generates binaries & changelog. | Ensures releases are controlled and only triggered when explicitly tagged. | 20h |
| Week 15 | Round of mentor review. Address initial concerns. | Feedback report with identified issues and areas for improvement. | This is the first full review to ensure the project aligns with expectations. | 20h |
| Week 16 | Iterative improvements, final bug fixes. | Final tests, refined functionality and  optimized performance. Project should be fully functional and stable across all platforms. | Focus on edge cases, error handling, and final performance improvements. | 20h |
| Week 17 | Update documentation, prepare final presentation. | Finalized documentation and a structured project presentation. | Ensure all implementation details, decisions, and tests are well-documented. | 20h |
| Week 18 | Submit the final project and obtain mentor approval. | Project officially approved and submitted. | Complete project submission, mentor sign-off. | 20h |


- **Communication plan**

    I plan to use Zulip as the closest communication method with my mentor alongside drafting pull requests regularly to allow continuous feedback. I also suggest weekly meetings, following the suggested implementation timeline, to serve as checkpoints tracking the progress.

## Personal statement

- **Past experience.** 

    My coding experience range from academic to business software development. As a part-time Cloud Software Engineer Intern at a multinational company for a year and a half, I have contributed to the development of three different major cloud-based Python projects: a Massive Data Processing tool (and its API), a Model Execution Interface to integrate Operational Research/Machine Learning models with backend scalability and, finally, a platform to calculate the probability of OCTG pipe collapse, based on a Monte Carlo algorithm. However, research collaboration has also significantly contributed to the development of my coding skills. During the two first years of my BSc I secured an undergraduate research scholarship in Bioinformatics which allowed me to collaborate with the developement of a Laboratory Information Management System (LIMS) in Python. During this time, I developed my interest for the intersection between Biological and Computational concepts. Although I was not able to publish, I collaborated with other researchers in the lab to submitt a [paper for review](https://drive.google.com/file/d/1zBtBH4bM4327fffN0j4pky9UCv62hWTv/view?usp=sharing) to the Qualis A2 journal, *Knowledge and Information Systems*. Even though open-source projects are part of my developer routine, I haven't yet collaborated to any projects, and I believe GSoC is a great opportunity to actively engage with the open-source community.
    
- **Motivation: why this project?**

    After a frustrated application to the Gatsby Bridging Programme, I believe the NIU program is an amazing opportunity to introduce myself to Neuroinformatics research and its community by starting effectively contributing to it. In special, my experience working with cloud applications and data management are some aspects that intersect with Datashuttle and motivated me to work on it. Additionally, this project also aligns with my further ambition to apply for a MSc program in the field of Neuroinformatics, preferably in London. It is clear to me that the project can have a significantly positive contribution to the open source community by abstracting, in a very intuitive way, difficult tasks, such as data transfer and validation. This perception comes from my previous experience as an undergraduate researcher in the Bioinformatics field, which showed to me how challenging computational concepts might be for researchers with no computational background, and Datashuttle assesses these problems. Also, coming from a developing country, I understand how research in our reality relies on open software code, and I believe Datashuttle can be a very useful tool to the entire community world wide.

- **Match: why you?**

    Having research experience in the Bioinformatics field, handling laboratory data through the development of a Laboratory Information Management System, is perhaps the most significant past experience that particularly suits me for this project. Coming from a computational background I find fundamental to understand not only the tool, but its entire community and users. In this sense, a previous introduction to the biological research community is a unique skill that brings me closer to Datashuttle. However, my experience as an intern at a multinational company has also equipped me with well-suited skills. As an addition to my Python coding proficiency, since a very fundamental requirement is communication, as part of a global team I am used to collaborate in international projects, which is also formally ensured by an IELTS Academic C1 (8.0) certification. Finally, i also emphasize my technical expertise in production-level Python development and cloud applications, highlighted by my experience in data-driven projects are further evidences on how I can be effectively collaborative for this project and its team.

- **Availability**

    I plan to dedicate around 20 hours per week to the GSoC project while balancing my part-time internship (also 20 hours per week). In order to manage both commitments and compensate for the shorther weekly allocation, I have proposed a 18-week project timeline - slightly longer than the usual 12-week schedule. I am confident with my ability to manage both commitments, especially since during the period of the program I will be on vacation from university (Universidade Federal de Minas Gerais), time I plan to use it to focus primarily on the project.

## GSoC

- **GSoC experience**

    I perceive GSoC as a gateway to open-source collaboration. In other words, I expect from this program an opportunity to introduce myself to the open-source community and effectively contribute to it. Regarding specifically to the NIU team, I also believe that this is a great chance to create a lasting professional and collaborative relationship with the crew and to learn more about the Neuroscience field. 
  
- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am not submitting any other proposals. 
