# Spikewrap:Add motion correction processing (Hargun Kaur)

## Personal details

- **Full name:** Hargun Kaur  
- **Email:** hargunkaur286@gmail.com  
- **GitHub username:** hargunkaur286  
- **Zulip username:** Hargun Kaur 
- **Location & Time-zone:** Delhi, India (IST, UTC+5:30)  
- **Personal website:** [hargunkaur.vercel.app](https://hargunkaur.vercel.app)  

### Code contributions:
- [neuroinformatics-unit/spikewrap#232](https://github.com/neuroinformatics-unit/spikewrap/pull/232) - Automatically save plot_probe
- [neuroinformatics-unit/spikewrap#231](https://github.com/neuroinformatics-unit/spikewrap/pull/231) - Update the feature roadmap
- [neuroinformatics-unit/ethology#78](https://github.com/neuroinformatics-unit/ethology/pull/78) - Added YOLO for detecting bounding boxes per frame on an input video

### Proposal discussion link:
- [neuroinformatics-unit/gsoc#69](https://github.com/neuroinformatics-unit/gsoc/pull/69)

## Project proposal  

### Synopsis

This project aims to integrate motion correction functionality into the `spikewrap` Python package by leveraging SpikeInterface's drift correction capabilities. During extracellular neural recordings, mechanical drift can misalign spike waveforms over time, significantly impacting the reliability of spike sorting and subsequent neuron tracking (see e.g. Steinmetz et al. (2019), Nature for multi-region recordings with notable probe drift). Currently, drift correction is only internally available in select sorters such as Kilosort2.5. This project generalizes drift correction by implementing it as a standardized preprocessing step within `spikewrap`.

We will use SpikeInterface’s high-level API ([`spikeinterface.preprocessing.correct_motion()`](https://spikeinterface.readthedocs.io/)), which localizes spikes, estimates probe movement, and realigns the signal. By building a user-friendly wrapper around these capabilities, `spikewrap` will allow researchers to apply drift correction prior to spike sorting, thus improving data quality and reproducibility.

The main goals of this project are to:
- Integrate motion correction into `spikewrap`'s preprocessing workflow, with intuitive configuration and CLI support.
- Develop robust unit and integration tests to ensure correctness and reliability.
- Update documentation and tutorials, demonstrating how to use the new motion correction feature.

By project completion, users will easily enable drift correction, significantly enhancing the reliability and reproducibility of spike sorting results. The neuroscience open-source community will greatly benefit from streamlined access to state-of-the-art motion correction, ultimately improving data quality and utility in research labs worldwide.

### Implementation timeline  

#### Minimal deliverables:
- Integration of SpikeInterface’s motion correction into Spikewrap preprocessing
- Command-line interface support  
- Comprehensive unit and integration tests  
- Updated documentation and tutorial notebook  

#### Stretch goals (if time permits):
- Multiple motion correction algorithm support. (eg: Kilosort2.5-based, DREDge, etc.) 
- Advanced CLI options for fine-tuning  
- Benchmarking impact on spike sorting quality and runtime  

#### Weekly schedule (12 weeks total, ~30 hours/week):

| Week | Tasks |
|------|-------|
| Community Bonding (Pre-week 1, ~10-20 hrs/week) | Study [SpikeInterface APIs and internals](https://spikeinterface.readthedocs.io/), prepare test data (e.g. Neuropixels sample with induced drift),plan integration strategy, and discuss the approach with mentor. |
| 1    | Implement core `MotionCorrection` wrapper in spikewrap that call SpikeInterfaces's `correct_motion` on a recording anf then integrate this into the Session.preprocess pipeline. Then, test on a small recording to verify that motion-corrected output is produced. |
| 2    | Finish integration details and add configuration options to toggle motion correction. Write first tests using synthtic data for validating the expected data transformations(e.g., no shape change, drift metrics reduced.) |
| 3    | Develop CLI support to enable motion correction and verify end-to-end pipeline functionality by testing on example data(including combining with an actual spike sorter). Address any integration bugs |
| 4    | Expand testing suite by adding edge cases(no motion correction vs. motion correction, different recording lengths, multi-shank recordings). Verify effectiveness on drift dataset(e.g. Steinmetz’s imposed motion data), measure performance and begin documentating the changes. |
| 5    | Write a dedicated tutorial or section in spikewrap docs on using motion correction (e.g. “How to use motion correction in spikewrap”), including code examples.  |
| 6 (Mid-term evaluation) | Finalize minimal deliverables(feature is implemented, tested and documented) and conduct mid-term review. If ahead of schedule, start exploring stretch goals (e.g. listing available motion correction methods from SpikeInterface). |
| 7 | Implement support for selecting different motion correction methods or presets provided by [SpikeInterface](https://spikeinterface.readthedocs.io/) (e.g., Kilosort-style vs. DREDge method) |
| 8    | Allow fine-tuning motion correction parameters (for advanced users). Eg: allow setting arguments like spatial bin size or smoothing if supported by SpikeInterface. Validate the parameters and update the documentation. |
| 9    |  Design a small benchmarking experiment to evaluate the effect of motion correction (eg: run spike sorting on a dataset with and without motion correction and compare metrics). Document the findings. |
| 10   | Refine implementation, optimize performance based on community feedback. |
| 11   | Finalize the code by writing any remaining tests and improving coverage. Perform integration testing of the entire spikewrap pipeline including motion correction on various data to ensure stability. |
| 12   | Complete the tutorial and documentation updates with polished examples and clear instructions. Double-check that documentation matches the final code behavior, prepare submission materials, share results with the community. |

### Communication Plan

- **Daily Updates:** Quick daily posts on NIU Zulip.
- **Weekly Meetings:** End of the week video calls for detailed updates.
- **Progress Logs:** Regular updates via GitHub drafts or devlogs.
- **Flexible Style:** Open to asynchronous video or text updates.
- **Community Updates:** Frequent progress sharing with NIU community.

## Personal statement

### Past experience  
I am a final-year B.Tech student in Artificial Intelligence and Machine Learning. I interned at Layer5, contributing to open-source Meshery and merging over 25 PRs. At Pacecourt, I led frontend development and improved performance significantly. Proficient in Python and ML pipelines (ZenML, MLflow), I actively participate in hackathons, winning over 4 national and international events. My previous contributions to NIU’s Spikewrap and Ethology repositories familiarized me with neuroinformatics tools and workflows.

I am also a co-author of a research publication titled **“Deep Learning Techniques for Skin Lesion Identification and Categorization”**, leading implementation, evaluation, and reproducibility tasks with deep learning models on the HAM10000 dataset, aligning closely with technical demands of this project.

### Motivation: Why this project?  
I’m drawn to this project because it’s a perfect intersection of my academic focus and long-term interest. I want to work on brain–behavior research tools, and preprocessing raw electrophysiological signals is a crucial piece. This project will let me build something impactful for labs working with neural recordings, and I hope to continue as a long-term contributor to NIU.

### Match: Why me?  
My solid Python skills, hands-on experience with ML pipelines, and familiarity with best software practices uniquely position me for this project. Having already contributed to `spikewrap` and `ethology`, I understand NIU’s coding style and workflow. I'm comfortable writing clean, testable code and enthusiastic about deepening my understanding of motion correction methods and neuroscience tooling. My proven adaptability, reliability, and strong communication skills ensure effective collaboration with my mentors and the NIU community.

### Availability  
I confirm that I can devote ample time to GSoC. I will dedicate ~30-35 hours weekly. Also, my academic semester concludes before the coding period begins.

## GSoC  

### GSoC experience  
I’m excited about GSoC as a platform to apply my open-source skills to healthcare and neuroinformatics—domains I deeply care about. Although my AIML coursework hasn’t offered direct neuroscience internship opportunities, I’ve contributed through hackathons, open-source, and research. I’ve learned the power of community, mentorship, and reproducibility through my work and contributions at Layer5.

I’m eager to continue growing as a researcher and developer, and GSoC will help me sharpen technical and collaborative skills while building something meaningful. More importantly, I want to remain active in the NIU community beyond GSoC, especially as I graduate and look to stay connected with mission-driven research teams.

### Are you also applying to projects with other organisations in GSoC 2025?  
I am considering submitting proposals to PyDataStructs and NIU’s Ethology project as well(if we're allowed to submit for two projects under NIU). In case of a tie, I would prioritize working on a NIU project. I am committed to focusing my efforts on this project throughout GSoC and beyond, and I look forward to deepening my contributions to the NIU community.