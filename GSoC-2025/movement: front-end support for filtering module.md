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
  3. [Added a Widget for drawing region of interest in napari (feature discussed in #378).](https://github.com/neuroinformatics-unit/movement/pull/489)
  4. [Fix Runtime Warning raised by ROI plot test](https://github.com/neuroinformatics-unit/movement/pull/534)
- **Proposal discussion link**:   

---

## Project Proposal  
**Synopsis**  
This project aims to develop an intuitive napari plugin for Movement’s filtering module, enabling non-programmers to clean and analyze motion-tracking data (e.g., from pose estimation tools like DeepLabCut) through a graphical interface instead of Python scripting.  

**Why It Matters**  
- **Accessibility Gap**: Most biologists/neuroscientists lack coding skills but rely on pose-tracking data.  
- **Time Efficiency**: Manual data cleaning consumes research time; real-time filtering previews streamline workflows.  
- **Reproducibility**: GUI-driven workflows ensure standardized filtering across labs.  
- **Open Science**: Democratizes advanced tools for underrepresented institutions with limited computational resources.  

---

## Implementation Timeline  
### 1. **Core Deliverables**  
- **Napari Widget Suite**:  
  - Dropdown menus for confidence filters (threshold-based outlier removal).  
  - Sliders/inputs for Median filter (window size) and SavGol filter (window size, polynomial order).  
  - Real-time overlay of raw vs. filtered data.  
- **Testing Framework**:  
  - Unit tests for filter logic and UI components.  
  - Performance benchmarks (latency <500ms for 10k data points).  
- **Documentation**:  
  - Jupyter notebook tutorials with sample datasets.  
  - Contributor guidelines for extending the widget.  
- **Video Tutorial**: 5-minute demo for all the filters, covering how and when to use each.  

### 2. **Extended Deliverables (Aspirational)**  
- **Filter Chaining**: Sequential application of filters (e.g., confidence → median → SavGol).  
- **Export Workflows**: Save/load filter in netCDF file format (or any other decided after discussion with the mentor).  
- **Community Presets**: Curated settings for common use cases (e.g., fruit fly locomotion).  
- **Hardware Acceleration**: GPU-backed filtering.  

---

## GSoC 2025 Timeline  
### **Community Bonding Period** *(May 8 – June 1)*  
| Week | Tasks | Hours | Output |  
|------|-------|-------|--------|  
| CB1  | Study napari plugin architecture; draft wireframes with mentors | 7 | Environment setup guide |  
| CB2  | Profile filter performance; create UML diagrams; setup Sphinx docs | 8 | Technical design doc |  
| CB3  | Finalize widget CSS theme; draft Jupyter notebook | 5 | PR for docs infrastructure |  

### **Coding Period** *(June 2 – August 24)*  
| Week | Focus Area | Critical Deliverables | Hours |  
|------|------------|------------------------|-------|  
| 1    | Widget Framework | Base widget class; confidence threshold UI | 15 |  
| 2    | Median Filter | Rolling window logic; unit tests | 14 |  
| 3    | SavGol Filter | Polynomial order control; benchmarks | 16 |  
| 4    | Preview System | Live parameter tuning; visualization | 14 |  
| 5    | Error Handling | Tooltip explanations; logging | 13 |  
| 6    | **Midterm** | Cross-platform tests; user docs v1 | 14 |  
| 7    | Advanced Features | Filter chaining; undo/redo stack | 12 |  
| 8    | Testing | Codecov integration; release pipeline | 15 |  
| 9    | Documentation | Video tutorial; accessibility audit | 14 |  
| 10   | Optimization | Memory leak fixes; batch processing | 12 |  
| 11   | Polish | Keyboard shortcuts; contributor guide | 13 |  
| 12   | Validation | Final benchmarks; release checklist | 12 |  

---

## Communication Plan  
| Channel | Purpose | Frequency |  
|---------|---------|-----------|  
| Zulip   | Daily updates; progress tracking | Daily (Mon–Fri) |  
| Zoom    | Weekly sync meetings; demos | Weekly (Thursdays) |  
| GitHub  | PR reviews; issue tracking | Per milestone |  

---

## Personal Statement  
**Past Experience**  
My technical experience aligns with this project’s goals through Python programming, signal processing, and open-source contributions. During my Machine Learning Internship, I developed segmentation models (U-Net, ResNet-34) using PyTorch and NumPy. At Goa Shipyard Limited, I designed a SCADA-based monitoring system with real-time alarms, emphasizing intuitive GUI design. My web projects (e.g., a WebRTC video app and WebSocket-based IDE) required real-time interactivity, similar to the widget’s preview functionality. Academically, my B.E. coursework in *Digital Signal Processing* covered FIR/IIR filters and Fourier transforms, providing foundational knowledge for SavGol/median filters. I’ve also contributed to Movement’s frontend codebase via PRs like [#489](https://github.com/neuroinformatics-unit/movement/pull/489).  

**Motivation: Why This Project?**  
I’m excited to work on this project because it offers the opportunity to combine my Python skills with real-time UI development to solve practical challenges in movement analysis. Developing an intuitive filtering widget for napari excites me because it will simplify complex workflows and make pose-tracking data processing more efficient for researchers.

The chance to contribute to open-source tools that accelerate scientific research, while deepening my skills in real-time UI development, makes this project uniquely impactful.This project bridges the gap between advanced algorithms and user accessibility, directly supporting open science and reproducibility. 

**Match: Why Me?**  

You should choose me for my blend of Python expertise, signal processing knowledge, and GUI development experience. I’ve built ML models using Python/NumPy nad pandas, studied DSP (SavGol/median filters), and designed intuitive GUIs like a SCADA system for non-technical users at Goa Shipyard. My contributions to Movement demonstrate codebase familiarity and collaboration skills. My goal is to empower researchers by automating tedious tasks, letting them focus on discovery. 

**Availability**  
My end-semester exams conclude in early May, freeing me to commit fully to GSoC.  

---

## GSoC   

- **GSoC experience** <br>
I expect GSoC to deepen my open-source collaboration skills, refine my technical expertise (e.g., napari plugin development), and connect me with mentors to build impactful tools. The program offers a structured environment to contribute meaningfully to Movement while learning industry-standard practices in testing, documentation, and community-driven development. Ultimately, I aim to grow as a developer and deliver a feature that simplifies research workflows for scientists globally. 

- **Other Applications**  
No—I’m exclusively applying to the neuroinformatics-unit.  
