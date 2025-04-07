# BrainGlobe:brainglobe-registration (Saarah Hussain)

# Personal Details

- **Full name:** Saarah Hussain
- **Email:** saarah.815@gmail.com
- **GitHub username:** saarah815
- **Zulip username:** Saarah Hussain (User ID 733864)
- **Location & time-zone:** London, UK. BST.
- **Code contribution:**
    
    https://github.com/brainglobe/brainglobe-atlasapi/pull/358
    https://github.com/brainglobe/brainglobe-registration/pull/52
    https://github.com/brainglobe/brainglobe-registration/pull/49
    
    https://github.com/brainglobe/brainglobe-registration/pull/46
    https://github.com/brainglobe/brainglobe-registration/pull/48

- **Proposal discussion link:**

    https://github.com/neuroinformatics-unit/gsoc/pull/65
    

# Project Proposal 

## Synopsis

This project aims to enhance the brainglobe-registration tool by automating the selection of atlas regions for aligning 2D or 3D brain images to a standard anatomical reference via brainglobe-atlasapi. Currently, this process is manual, time-consuming, and subjective, posing a barrier to reproducibility and efficiency. By introducing a new preprocessing step that automatically identifies the optimal atlas region – using methods such as adaptive grid search, machine learning, or Bayesian optimisation – this project will streamline the workflow and improve accuracy. Deliverables include at least two implemented approaches, benchmarking, comprehensive testing, full documentation, and a blog post to showcase the new functionality.

This automation directly benefits my research on spatiotemporal brain development in paediatric brain tumour radiotherapy, where mapping histology images to an atlas is essential for analysing cellular behaviour across brain regions. By making this process faster and more robust, it not only enhances my own work but also enables broader adoption of BrainGlobe tools by researchers in neuroscience and healthcare, even those without extensive anatomical expertise.

## Minimal Set of Deliverables
    
- Implement a new preprocessing step to automatically select the atlas region.
- Compare at least two region-selection methods (e.g., adaptive grid search vs ML/Bayesian optimisation).
- Add tests to validate the new functionality.
- Document the new pipeline and add usage instructions.
- Write a blog post showcasing the project and results.

## Weekly Timeline

  | Week                         | Tasks                                                                                                                                             |
  |------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
  | Week 0, (Jun 2 – Jun 6)      | Community bonding: explore codebases, review literature, align project scope with mentors. |
  | Weeks 1-2 (Jun 9 - Jun 20)   | Implement and refine baseline region selection method (e.g., grid search). Integrate into pipeline with test coverage. Add toggle for manual/auto mode. Internal review and cleanup.      |
  | Weeks 3-4 (Jun 23 - Jul 4)   | Develop and integrate alternative method (Bayesian/ML). Run early performance checks.                                                                                        |
  | Week 5 (Jul 7 - Jul 11)      | Evaluate both methods on representative datasets (e.g., region similarity, accuracy). Visualise and document results. Submit midterm report. Mentor check-in.                            |
  | Week 6 (Jul 14 - Jul 18)     | Benchmark both methods across atlases. Optimise runtime and default parameters. Code cleanup, API integration.                                                                          |
  | Weeks 7-8 (Jul 21 - Aug 1)   | Add tests for edge cases and improve logging/UI. Optimise default parameters. Start user documentation and usage tutorials.                                                               |
  | Week 9 (Aug 4 - Aug 7)       | Finalise documentation, blog post, and visuals. Submit final report. Gather mentor feedback and prepare follow-up PRs/stretch goals.                                                      |

Time commitment: 40hr / week, Mon-Fri (except Week 9, which is Mon-Thu).

## Communication Plan

Weekly video calls, Zulip catch-ups when required

# Personal Statement

## Past Experience - Why Me?

My ongoing research project at UCL MPBE: “Investigating Radiotherapy Response: A Machine Learning Approach to Cell Classification and Spatial Transcriptomics”. Within this, I have:
  -	Used **Elastix** to align histological images with a 3D brain atlas, applying transformation parameters from Slice2Volume for accurate spatial mapping 
  -	Integrated **Napari** for interactive visualisation of transformed and registered images, overlaying atlas slices onto histological sections with adjustable colormaps
  -	Performed image segmentation and cell detection using Meta’s **deep learning** Segment Anything Model (SAM) to segment cells from histology images
  -	Implemented distributed inference across multiple GPUs using **PyTorch Lightning** to efficiently process whole slide images (WSIs)
  -	Automated background removal and tile sampling from WSIs using custom pipelines (TiffSlide, OpenSlide, TileOps), achieving large-scale tiling for downstream analysis
  -	Processed spatial transcriptomics data to analyse gene expression in tissue context by mapping immunofluorescence data to gene expression profiles from RNA sequencing

Contributed to BrainGlobe during a two-week summer placement at the SWC. A number of my PRs were merged. Please see below for a few examples:
  - **Load atlas with no Internet**: I updated get_all_atlases_lastversions() to support offline use by checking for internet connectivity and GIN availability. If offline, it attempts to load a local last_versions.conf, warning the user that the list may be outdated. If no local file exists, it prompts the user to connect to the internet to fetch the atlas list.
  -	**Filter Images**: Functionality for user to filter fixed and moving image before registration.
  -	**Info message when running BrainGlobe Registration plugin with no atlas installed**: If user has no atlases installed, I created a widget which informs user that they need to install atlas(es) before they are able to use BrainGlobe Registration plugin.
  -	**Communicate napari layer deletions appropriately to the plugin**: Overcame the issue of undefined behaviour and out of bounds errors when user deletes the atlas or moving image. Layer deletions are now communicated appropriately and the plugin can handle restarting the entire workflow without having to restart the plugin.


## Motivation: Why This Project?

I’m deeply invested in the BrainGlobe project because its tools are central to my ongoing research at UCL on spatiotemporal brain development in paediatric brain tumour radiotherapy. Accurately mapping histology images to a standard atlas is essential for analysing cellular behaviour across brain regions, and the automation proposed in this project would directly enhance the efficiency, reproducibility, and scalability of that process. My experience using Elastix, Napari, and spatial transcriptomics pipelines, as well as my prior contributions to BrainGlobe during a summer placement—including offline atlas loading and plugin robustness—have shown me the immense value of this ecosystem. This project is a natural and meaningful extension of my work, both personally and for the wider neuroscience and medical research community.

## Availability

Available full-time after May (Mon-Fri, 40hr / week). Plan to 2 weeks off in August, as reflected in my timeline.

# GSoC

## GSoC Experience

I see the program as a unique opportunity to grow as a contributor to open-source scientific software while developing tools that have real impact in neuroscience research. I hope to deepen my understanding of image registration, atlas-based workflows, and optimisation techniques, while learning how to design software that is robust, well-documented, and accessible to the broader research community. I'm particularly excited about working closely with experienced mentors, gaining insight into collaborative development practices, and contributing to a project that improves research reproducibility and efficiency. While the project aligns closely with my own work, I’m especially looking forward to learning from the community and building tools that can support a wide range of users beyond my own use case.

## Are you also applying to projects with other organisations in GSoC 2025?

No.
