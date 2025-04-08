# movement - Web-based graphical user interface for movement (Swayam Jaiswal)

## Personal Details

- **Full Name**: Swayam Jaiswal  
- **Email**: swayamjai0444@gmail.com  
- **GitHub Username**: Swayamjexe  
- **Zulip Username**: Swayam Jaiswal  
- **Location & Timezone**: Pune, India (GMT+5:30 IST)  
- **Personal Website**: N/A  

---

## Code Contribution

- [**Draft PR for the Jupyter-based prototype GUI**](https://github.com/neuroinformatics-unit/movement/pull/542)

---

## Proposal Discussion Link

- [**GitHub Discussion Thread**](https://github.com/neuroinformatics-unit/gsoc/pull/57)

---

## Project Proposal

### **Synopsis**

This project focuses on building a lightweight, accessible, web-based graphical user interface (GUI) for the **movement** library, a tool used for analyzing and visualizing pose estimation data in neuroscience and behavior research. The existing GUI is built with **napari**, which can be hard to use in cloud-based and notebook environments like Jupyter and Google Colab.

The proposed web-based GUI will mimic the functionality of the napari GUI while being easier to deploy and interact with in both notebook and online workflows. It will include tools for loading videos and pose data, filtering and overlaying keypoints per body part and `animal_id`, navigating through frames, and exporting annotated data. The open-source community will benefit from broader accessibility and improved usability across platforms.

Over the past few days, I have developed a working Jupyter prototype using **matplotlib**, **ipywidgets**, and **VideoReader** to replicate some core features. However, the playback is choppy due to the limitations of matplotlib, which is optimized for static visualizations. I am now actively researching alternatives like **Plotly**, **Bokeh**, and **Dash** to build a more scalable and interactive interface. These frameworks better support dynamic rendering and align well with the project's long-term goals. You can see the working of the prototype [here](https://drive.google.com/file/d/1kguSF_7yjORYI3rSWTqtK_OW_VO4Ikde/view?usp=sharing).

---

## Implementation Timeline

### **Minimal Set of Deliverables**

**A web-based GUI prototype for movement, supporting video and pose data loading (SLEAP, DeepLabCut, LightningPose), with features like keypoint overlays (e.g., snout, tail), animal ID filtering, and basic playback controls** 

### **Stretch Goals**

**Enable export of annotated frames/videos, add trajectory visualization tools, and support deployment in notebook environments like Binder or Hugging Face Spaces.**

### **Weekly Timeline**

| **Phase**                         | **Weeks**              | **Deliverables**                                                                                                              | **Estimated Hours** |
|----------------------------------|------------------------|------------------------------------------------------------------------------------------------------------------------------|---------------------|
| **Planning & Setup**             | Community Bonding + Week 1 | - Finalize feature list with mentors  <br> - Evaluate visualization frameworks  <br> - Set up project structure  <br> - Initialize Dash/Plotly-based GUI scaffold | 25–28 hrs           |
| **Data Integration**             | Weeks 2–3              | - Implement video and pose data loading (SLEAP, DLC, LightningPose)  <br> - Add keypoint overlay logic  <br> - Build filtering UI for body parts                  | 36–41 hrs           |
| **Interactivity & Filtering**    | Weeks 4–5              | - Implement frame navigation and playback controls  <br> - Add animal_id-based filtering  <br> - Polish UI and integrate components for testing                   | 27–32 hrs           |
| **Advanced Visualization**       | Weeks 6–7              | - Implement trajectory visualization  <br> - Refine interactive controls  <br> - Add export functionality for annotated frames/videos                             | 38–42 hrs           |
| **Optimization & Compatibility** | Weeks 8–9              | - Optimize performance  <br> - Finalize filtering interactions  <br> - Test in Colab, Binder, and other notebook environments                                    | 28–32 hrs           |
| **Finalization & Submission**    | Weeks 10–12            | - Final UI polish and bug fixes  <br> - Write documentation and user guide  <br> - Record walkthrough video  <br> - Final submission prep                         | 23–29 hrs           |

---

## Communication Plan

- **Meeting Frequency**: Weekly check-ins with the mentor, with additional meetings if needed.  
- **Daily Updates**: Regular progress updates via Zulip chat for quick feedback.  
- **Communication Channels**: Zulip chat for discussions, GitHub issues for tracking progress, and occasional video calls for in-depth reviews.  
- **Progress Reports**: Weekly reports maintained in a log style for summarizing development milestones, challenges, and next steps, shared via GitHub or a Zulip.  

---

## Personal Statement

### **Past Experience**

I am a final-year Computer Engineering undergrad with a strong background in Python, data visualization, and machine learning. I’ve worked on ML-powered safety systems (**CogniSafe**), built interactive dashboards using **PowerBI**, and developed cross-platform GUI tools using **Tkinter** and **ipywidgets**. My interest in human-computer interaction and visual design has led me to build user-friendly interfaces tailored for data exploration.

### **Motivation: Why this project?**

This project combines my passion for building usable tools and my interest in open science and research tooling. I am also intrigued by the field of AI especially the computer vision domain. I was drawn to the idea of making complex pose estimation data more accessible to researchers without a strong programming background and keeping it intuitive. The Jupyter-based prototype I’ve already built was a deep learning experience in understanding how different visualization libraries work and how state management affects interactivity. I want to turn these insights into a robust, long-term contribution to the **movement** project.

### **Match: Why you?**

I’ve already invested time researching and building an initial prototype. My understanding of the project’s technical challenges—such as state management in dynamic UIs, integration of multiple pose estimation formats, and filtering by animal/keypoints—puts me in a great position to take this project forward. My frontend and visualization background, combined with ML familiarity, makes me a unique fit for this hybrid technical project.

---

## Availability

I will not have any conflicting commitments during the summer. No internships, courses, or vacations are planned. I’ll be available for GSoC full-time throughout the program.

---

## GSoC

### **GSoC Experience**

This is my first time applying to GSoC or contributing to an open-source program and I’m excited to work under experienced mentors and learn more about open-source development, team workflows, and sustainable code practices. I want to contribute something meaningful and long-lasting.

### **Other Applications**

This is the only project I am applying to for GSoC 2025. This project aligns best with my skill set and interests, and I want to give it my full focus and energy.
