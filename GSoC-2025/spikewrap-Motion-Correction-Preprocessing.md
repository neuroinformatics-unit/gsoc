# spikewrap: Motion Correction Preprocessing (Your-Name)

## Personal details

- **Full name:** Hailey Cheng (Cheng Hei Lam)
- **Email:** heilcheng2-c@my.cityu.edu.hk
- **GitHub username:** heilcheng
- **Zulip username:** Hailey
- **Location & time-zone:** Hong Kong, UTC +08:00
- **Personal website / project portfolio:** https://haileycheng.com/about

## Code contribution

Update feature roadmap with new planned features #227, according to Issue #217 Update roadmap.
https://github.com/neuroinformatics-unit/spikewrap/pull/227


## Project proposal

### Synopsis

This project aims to integrate motion correction preprocessing capabilities into spikewrap, leveraging the functionality available in SpikeInterface. Motion correction is a critical preprocessing step in extracellular electrophysiology, as electrode drift can significantly impact the quality of neural recordings over time. By incorporating motion correction into spikewrap's preprocessing pipeline, we can improve spike sorting accuracy and data reliability without requiring users to implement complex correction algorithms manually.

The primary goals are to:
1. Abstract SpikeInterface's motion correction methods into spikewrap's user-friendly API
2. Implement appropriate parameter validation and error handling
3. Ensure seamless integration with existing preprocessing steps
4. Provide comprehensive documentation and usage examples

The deliverables will include Python modules for motion correction, test coverage for all new functionality, and thorough documentation including practical examples. This addition will significantly enhance spikewrap's utility for neuroscientists working with extracellular recordings, especially during long experimental sessions where electrode drift is common.

### Implementation timeline

**Minimal set of deliverables:**
- Implement motion correction preprocessing functions in spikewrap
- Create unit and integration tests for all new functionality
- Document the new features in the spikewrap documentation
- Develop usage examples demonstrating motion correction workflows

**Stretch goals:**
- Create visualization tools for before/after motion correction comparison
- Implement automated motion detection to suggest when correction might be needed
- Add benchmarking tools to evaluate correction quality

**Detailed weekly timeline (based on 12-week GSoC period):**

| Week | Deliverables | Hours |
|------|--------------|-------|
| Community bonding | Familiarize with spikewrap and SpikeInterface codebases; Set up development environment; Study motion correction algorithms in SpikeInterface | 20 |
| 1 | Investigate SpikeInterface motion correction API; Design integration approach; Create initial PR structure | 30 |
| 2 | Implement core motion correction function wrappers; Begin parameter validation | 30 |
| 3 | Complete parameter validation; Implement error handling; Begin integration with preprocessing pipeline | 30 |
| 4 | Complete integration with preprocessing pipeline; Start writing unit tests | 30 |
| 5 | Complete unit tests; Begin integration tests; Start documentation | 30 |
| 6 | Complete integration tests; Continue documentation; Create initial usage examples | 30 |
| 7 | Review and refine implementation based on mentor feedback; Address any issues | 30 |
| 8 | Implement visualization tools for comparing pre/post motion correction (stretch goal) | 30 |
| 9 | Begin implementing automated motion detection (stretch goal); Continue refining code | 30 |
| 10 | Complete stretch goals implementation; Refine documentation and examples | 30 |
| 11 | Code freeze; Final testing and bug fixes; Complete documentation | 30 |
| 12 | Final polishing; Prepare for submission | 30 |

I plan to dedicate approximately 30 hours per week to this project. This schedule accounts for the complexity of working with electrophysiological data while allowing time for thorough testing and documentation.

### Communication plan

I will maintain regular communication with my mentor through:
- Status updates via Zulip chat
- Code reviews through GitHub pull requests
- Ad-hoc discussions for urgent matters

All code changes will be documented in GitHub pull requests with detailed descriptions. I will maintain a development log to track progress and decisions made during the project.

## Personal statement

### Past experience

I am a sophomore in Mathematics and Computer Science, with a research interest in computational biology. I have a solid foundation in Python, with experience in using scientific libraries such as NumPy, SciPy, and pandas for data analysis, as well as PyTorch for deep learning applications. 

In the realm of neuroscience, I have conducted dry lab research under Prof. Tin Chung in CityUHK, focused on analyzing neural activity data using signal processing and machine learning techniques in Python. My work involved building analysis pipelines for spike detection and classification, and I have hands-on experience working with extracellular electrophysiology data.
### Motivation: why this project?

Motion correction is a critical component of electrophysiology data processing that significantly impacts the quality of neural recordings and subsequent analyses. My interest in this project stems from [your specific interest in computational neuroscience/electrophysiology/signal processing]. I believe improving these preprocessing tools will make high-quality neural data analysis more accessible to researchers who may not have expertise in signal processing.

The implementation of motion correction in spikewrap will help bridge the gap between raw data collection and meaningful scientific insights by ensuring that electrode drift doesn't compromise data integrity. This aligns with my personal goal of [your goals related to neuroscience/open science/tool development].

### Match: why you?

Strong programming background, familiarity with electrophysiology data formats and preprocessing, and prior research experience in computational neuroscience uniquely position me for this project.

I am particularly well-suited for this project because I understand both the technical challenges of implementing robust motion correction algorithms and the domain-specific needs of neuroscience researchers. My commitment to clean code, documentation, and collaboration further ensures I can contribute meaningfully to the project and the broader neuroinformatics community.

### Availability

I will be available to commit approximately 30 hours per week to the project during the GSoC period. I plan to frontload preparatory tasks during the Community Bonding period and remain flexible to work evenings and weekends when necessary to meet milestones.

## GSoC

### GSoC experience

From the GSoC program, I expect to gain valuable experience contributing to an open-source scientific software project while receiving mentorship from experts in the field. I look forward to improving my software engineering skills, deepening my understanding of electrophysiology data processing, and becoming an active member of the neuroinformatics community.

I am also applying to DeepChem and Open2C. My top preference is the spikewrap project as it aligns most closely with my current research interests in neuroinformatics and my long-term goal of building accessible, high-impact computational tools for neuroscience.
