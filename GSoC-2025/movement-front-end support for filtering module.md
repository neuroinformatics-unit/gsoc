## movement: front-end support for filtering module in movement (Harsh Bhanushali)
## Personal Details  
- **Full name**: Harsh Rakesh Bhanushali  
- **Email**: bhanushali.harsh203@gmail.com  
- **GitHub username**: harsh-bhanushali-05  
- **Zulip username**: harsh bhanushali  
- **Location & time-zone**: Panjim, Indian Standard Time (GMT+5:30)  
- **Code contributions**:  
  1. [Made `report_nan_stats` and `calculate_nan_stats` more permissive about dimensions.](https://github.com/neuroinformatics-unit/movement/pull/481)  
  2. [Added support for exporting bboxes in VIA-tracks.](https://github.com/neuroinformatics-unit/movement/pull/497)  
  3. [Extended interpolate_over_time to bfill, ffill, nearest and constant functionality](https://github.com/neuroinformatics-unit/movement/pull/537)
  4. [Added a Widget for drawing region of interest in napari (feature discussed in #378).](https://github.com/neuroinformatics-unit/movement/pull/489) 
  5. [Fix Runtime Warning raised by ROI plot test](https://github.com/neuroinformatics-unit/movement/pull/534)
- **Proposal discussion link**:   [link](https://github.com/neuroinformatics-unit/gsoc/pull/41)
---

## Project Proposal  
**Synopsis**  
This project aims to develop an intuitive napari plugin for Movement’s filtering module, enabling non-programmers to clean and analyze motion-tracking data (e.g., from pose estimation tools like DeepLabCut) through a graphical interface instead of Python scripting.  

**Why It Matters**  
- **Accessibility Gap**: Most biologists/neuroscientists lack coding skills but rely on pose-tracking data.  
- **Time Efficiency**: Manual data cleaning consumes research time; real-time filtering previews streamline workflows.  
- **Open Science**: Democratizes advanced tools for underrepresented institutions with limited computational resources.  

---

## Implementation Timeline  
### 1. **Core Deliverables**  
- **Napari Widget Suite**:  
  - Dropdown menus for confidence filters (threshold-based outlier removal).  
  - Sliders/inputs for Median filter (window size) and SavGol filter (window size, polynomial order).  
  - Show overlay of filtered vs the original data
- **Testing Framework**:  
  - Pytests for filter logic and UI components.  
  - Performance benchmarks.  
- **Documentation**:  
  - Tutorials on how to use the new widget on sample datasets.  
  - Contributor guidelines for extending the widget.  
- **Export Workflows**: Save/load filter configurations as YAML.  
- **Blog posts with video Tutorial**: Will write a [blog](https://movement.neuroinformatics.dev/blog/index.html) about the introduction of the new widget with a small video tutorial embeded in the blog. 

### 2. **Extended Deliverables (Aspirational)**  
- **Filter Chaining**: Sequential application of filters (e.g., confidence → median → SavGol).  
- **Community Presets**: Curated settings for common use cases (e.g., fruit fly locomotion).  
- **Acceleration**: Integrate parallel processing with [dask](https://www.dask.org/?utm_source=xarray-docs) where ever possible.  
- **Napari Widget addtion** Real-time preview of filtered data. 

---

## GSoC 2025 Timeline  
### **Community Bonding Period** *(May 8 – June 1)*  
| Week | Tasks | Hours | Output |  
|------|-------|-------|--------|  
| CB1  | Study napari plugin architecture; draft wireframes with mentors | 7 | Environment setup guide |  
| CB2  | Study about various file formats and continue with wireframes with mentors | 8 |Increase techenical understanding |  
| CB3  |   Profile filter performance; create UML diagrams; setup Sphinx docs | 8 | Technical design doc |  
### **Coding Period** *(June 2 – August 24)*  

| Week | Focus Area | Critical Deliverables | Hours (estimated)|  
|------|------------|------------------------|-------|  
| 1    | Widget Framework | Base widget class; confidence threshold UI | 15 |  
| 2    | Median Filter | Rolling window logic with "median", "mean", "min", and "max" being various options.| 14 |  
| 3    | SavGol Filter | Polynomial order control; benchmarks | 16 |  
| 4    | Preview System | Live parameter tuning; visualization | 14 |  
| 5    | Error Handling | Tooltip explanations; logging , Filter chaining (extended deliverable) | 18 |  
| 6    | **Midterm** | Cross-platform tests; user docs v1 | 14 |  
| 7    | Advanced Features | Filter chaining <br> YAML schema design for workflows(chains).| 16 |  
| 8    | Export Implementation | UI elements for exporting (buttons, file dialogs)<br>Save/load workflows to YAML<br>Export filtered data to netCDF<br>Validation tests | 18 |  
| 9    |  Documentation |  Write Blog post<br> Video tutorial (export demo) | 15 |  
| 10   | Optimization | Memory leak fixes;<br>Batch processing for large exports <br> parallel processing with  [dask](https://www.dask.org/?utm_source=xarray-docs)| 12 |  
| 11   | Polish | Keyboard shortcuts;<br>Contributor guide for export features | 13 |  
| 12   | Validation | Final benchmarks;<br>Release checklist | 12 |  

---

## Communication Plan  
| Channel | Purpose | Frequency |  
|---------|---------|-----------|  
| Zulip   | Daily updates; progress tracking | Daily (Mon–Fri) |  
| Zoom    | Weekly sync meetings; demos | Weekly (Friday) |  
| GitHub  | PR reviews; issue tracking | Per milestone |  

---

## Personal Statement  
**Past Experience**  
My technical experience aligns with this project’s goals through Python programming, signal processing, and open-source contributions. During my Machine Learning Internship, I developed segmentation models (U-Net, ResNet-34) using PyTorch and NumPy. At Goa Shipyard Limited, I designed a SCADA-based monitoring system with real-time alarms, emphasizing intuitive GUI design. My web projects (e.g., a WebRTC video app and WebSocket-based IDE) required real-time interactivity, similar to the widget’s preview functionality. Academically, my B.E. coursework in *Digital Signal Processing* covered FIR/IIR filters and Fourier transforms, providing foundational knowledge for SavGol/median filters. I’ve also contributed to Movement’s frontend codebase via PRs like [#489](https://github.com/neuroinformatics-unit/movement/pull/489).  

**Motivation: Why This Project?**  
I’m excited to work on this project because it offers the opportunity to combine my Python skills with real-time UI development to solve practical challenges in movement analysis. Developing an intuitive filtering widget for napari excites me because it will simplify complex workflows and make pose-tracking data processing more efficient for researchers.

The chance to contribute to open-source tools that accelerate scientific research, while deepening my skills in real-time UI development, makes this project uniquely impactful.This project bridges the gap between advanced algorithms and user accessibility, directly supporting open science and reproducibility. 

**Match: Why Me?**  

I should be chosen because I have a combination of signal processing understanding, GUI programming skills, and Python expertise. I've studied DSP (SavGol/median filters), created ML models with Python/NumPy and pandas, and created user-friendly GUIs for non-technical users at Goa Shipyard, such as a SCADA system. My contributions to Movement show my familiarity with the codebase and my ability to work with others. By automating time-consuming activities, I hope to empower researchers so they can concentrate on making discoveries. 

**Availability**  
My end-semester exams conclude in early May, freeing me to commit fully to GSoC.  

---

## GSoC   

- **GSoC experience** <br>
I expect GSoC to deepen my open-source collaboration skills, refine my technical expertise (e.g., napari plugin development), and connect me with mentors to build impactful tools. The program offers a structured environment to contribute meaningfully to Movement while learning industry-standard practices in testing, documentation, and community-driven development. Ultimately, I aim to grow as a developer and deliver a feature that simplifies research workflows for scientists globally. 

- **Other Applications**  
No—I’m exclusively applying to the neuroinformatics-unit.  
