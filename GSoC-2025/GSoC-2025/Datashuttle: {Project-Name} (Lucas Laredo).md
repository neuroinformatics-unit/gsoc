# datashuttle: Deploy datashuttle as an installable package (Lucas Laredo)  

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

    ---

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

| Week  | Tasks | Hours |
|-----------|----------|-----------------|
| Community Bounding | Project refinement: Discuss the proposal with the menthor and understand/plan the best approach. Further familiarize with the project standard packages and expected results. | 15h/20h |
| Week 1 | Start researching different cross-platform distribution methods. | 25h |
| Week 2 | Evaluate compatibility, compare approaches, and decide on the best approach for PoC. Start the writing the documentation. | 30h |
| Week 3 | Start implementing PoC using the selected method, identify roadblocks. | 25h |
| Week 4 | Conclude PoC implementation and validate it. Test on different OS environments and refine the approach. | 30h |
| Week 5 | Integrate the selected method into Datashuttle, ensure compatibility. | 25h |
| Week 6 | Implement Python API support, and conduct preliminary tests. First mentor review for mid-term point. | 25h |
| Week 7 | Test on different system configurations, and address issues. | 25h |
| Week 8 | Validate/Optimize performance. | 25h |
| Week 9 | Write further unit and integration tests and update documentation | 30h |
| Week 10 | Implement GitHub CI workflows. | 20h/25h |
| Week 11 | Final cross-platform testing, address any remaning bug and engage with the community for feedback. | 30h |
| Week 12 | Final mentor review. Prepare for final submission. | 30h |

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

    I plan to dedicate around 25 hours per week to the GSoC project while balancing my part-time internship. I am confident with my ability to manage both commitments, specially since during the period of the program I will be on vacation from university and which I plan to use it to further focus on the project.

## GSoC

- **GSoC experience**

    I perceive GSoC as a gateway to open-source collaboration. In other words, I expect from this program an opportunity to introduce myself to the open-source community and effectively contribute to it. Regarding specifically to the NIU team, I also believe that this is a great chance to create a lasting professional and collaborative relationship with the crew and to learn more about the Neuroscience field. 
  
- **Are you also applying to projects with other organisations in GSoC 2025?**

    I am not submitting any other proposals. 
