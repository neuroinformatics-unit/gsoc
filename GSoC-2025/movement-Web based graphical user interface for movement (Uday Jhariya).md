# movement: Web-based Graphical User Interface for Movement (Uday Jhariya)

## Personal Details
- **Full Name**: Uday Jhariya
- **Email**: jhariyauday60@gmail.com
- **GitHub**: [Udayscode](https://github.com/Udayscode)
- **Zulip**: Uday Jhariya
- **Location**: Jabalpur, India | **Time Zone**:  Asia/Kolkata UTC+5:30
- **Portfolio**: [https://github.com/Udayscode](https://github.com/Udayscode)

## Code Contribution
  1.[Rename source format](https://github.com/neuroinformatics-unit/movement/pull/525)
  2.[LinAlgError: SVD did not converge in tests on main branch](https://github.com/neuroinformatics-unit/movement/issues/532)
  3.[Ensure Windows CI uses D: drive](https://github.com/neuroinformatics-unit/movement/pull/518)

## Proposal Discussion Link
- **PR Discussion**: [Link to Proposal Discussion Thread](https://github.com/neuroinformatics-unit/gsoc/pull/your-discussion-pr-number)

## Project Proposal

### Synopsis
What if researchers could explore animal behavior data effortlessly, regardless of their coding expertise? This project brings that vision to life by building a web-based GUI for Movement, using Fastplotlib and Dash to seamlessly integrate with Jupyter Notebooks. The goals are clear and impactful:

1. **Cloud-based collaboration** for multi-institution research teams
2. **Interactive data exploration** without local installation barriers
3. **Real-time visualization** of complex trajectory datasets

**Core Deliverables**:
- **HDF5/CSV Data Loader**:    
  - Efficiently load large datasets using chunking or lazy loading techniques.
  - Implement progress indicators with Dash callbacks to enhance user experience.

- **Frame-Synced Video+Trajectory WebGL Visualization**:    
  - Use WebGL for smooth rendering of trajectories over video frames.
  - Optimize performance for real-time visualization of large datasets.

- **Dynamic Filtering**:    
  - Allow users to filter data by animal ID, keypoints, or time ranges dynamically.
  - Ensure filters update visualizations seamlessly using Dash callbacks.

- **MP4/PNG Export**: 
  - Enable users to export visualizations as MP4 videos or PNG images, preserving relevant metadata.

**Stretch Goals**:
- **Collaborative Annotation System**: Allow multiple users to annotate data collaboratively.
- **SLEAP/DeepLabCut Direct Import**: Integrate direct import capabilities for data from popular pose estimation frameworks.

### Implementation Timeline

| Week | Key Tasks | Hours |
|------|-----------|-------|
| **Pre-GSoC** | Study Movement architecture; Prototype basic Dash components to understand the UI framework and start building a minimal viable product (MVP). This includes setting up the development environment and familiarizing yourself with Fastplotlib and Dash. | 20 |
| **1-2** | Implement HDF5 parser with xarray integration. This involves designing a data loading module that can efficiently handle HDF5 files, leveraging xarray for data manipulation and analysis. Ensure that the module includes progress indicators to enhance user experience. | 35 |
| **3-4** | Develop WebGL video overlay using Fastplotlib. Focus on creating an interactive visualization system that overlays trajectories on videos, ensuring seamless frame synchronization. This will involve optimizing WebGL rendering for performance. | 35 |
| **5-6** | Build interactive filters and timeline controls. Implement dynamic filtering capabilities to allow users to focus on specific animals, keypoints, or time ranges. Ensure that filters are intuitive and provide clear visual feedback. | 35 |
| **7-8** | Create an export system with FFmpeg.js integration. Develop functionality to export visualizations as MP4 videos or PNG images, preserving relevant metadata. This will involve integrating FFmpeg.js for video encoding and ensuring metadata preservation. | 35 |
| **9-10** | Perform performance optimization and stress testing. Focus on optimizing the application for large datasets, ensuring that it can handle various input sizes without significant performance degradation. Conduct thorough stress testing to identify and fix any bottlenecks. | 25 |
| **11-12** | Finalize documentation and create Jupyter notebook tutorials. Develop comprehensive documentation for users and contributors, including step-by-step guides on how to use the web GUI. Create interactive Jupyter notebook tutorials to help users get started with the tool. | 25 |
| **Total**: 210 hours (~18 hrs/week)

### Communication Plan
- **Daily**: Zulip updates & PR reviews
- **Bi-weekly**: Video demos with mentors
- **Milestone Reviews**: Week 3, 6, 9
- **Emergency Protocol**: Discord voice channel

## Personal Statement

### Past Experience
One of my most rewarding experiences was during the Kharagpur Data Science Hackathon 2025 (Jan 2025), where I worked on a project called *Automated Research Paper Assessment and Conference Recommendation*. The goal was to help researchers by building an NLP-based system that classified research papers as "Publishable" or "Non-Publishable" by analyzing their methodology, coherence, and validation. I also designed a framework to recommend prestigious conferences like CVPR and NeurIPS for publishable papers, using Pathway Vectorstore for real-time data processing. To make the recommendations more actionable, I integrated a rationale generation feature that provided a comparative analysis with reference papers, ensuring relevance and alignment. This project taught me how to handle complex datasets, work with Python for data processing, and create tools that directly address user needs-skills I'm eager to apply to Movement's web-based GUI. I led a team of six as the team leader in the Smart India Hackathon (SIH) 2024, India's largest hackathon, where we secured top 5 rank among 1000s of teams nationwide. We developed an innovative solution to a real-world problem statement, collaborating under tight deadlines and leveraging Python, data visualization, and user-centric design. This experience enhanced my leadership, teamwork, and ability to deliver intuitive tools under pressure- that skills I'll apply to ensure Movement's GUI meets researcher's needs effectively.

### Motivation
I've always been fascinated by how technology can help solve real-world problems, especially in science. When I first came across pose estimation tools like SLEAP and DeepLabCut, I was amazed by their potential-but I also saw how tricky they can be for someone who isn't a coding expert. I want to change that. This project is personal to me because I believe researchers shouldn't have to struggle with technical barriers to do their best work. By building a web-based GUI for Movement, I want to create a tool that feels intuitive and empowering, so that anyone-whether they're a seasoned scientist or a curious student-can dive into animal behavior analysis with ease.

### Why Me?
I might not be the most experienced developer out there, but I bring a mix of passion and practical skills to this project. I've been coding in Python for over two years now, and I've spent a lot of that time working on data visualization projects that needed to be both functional and easy to use. I understand the pain points of working with tools like SLEAP and DeepLabCut because I've been there myself, trying to make sense of messy datasets late at night. Plus, I've been part of the NIU community past weeks, and I've loved every minute of learning and contributing here. I'm not just here to code-I'm here to build something that makes a real difference for the community I care about.

### Availability
I have no major commitments during the GSoC period and can dedicate 25-30 hours per week to this project-my focus will be entirely on delivering the best results for Movement and the NIU community.

## GSoC

### Expectations
## GSoC Expectations
For me, GSoC is more than just a coding program-it's a chance to challenge myself, learn from the best, and contribute to something truly impactful. As a first-time participant, I'm thrilled at the thought of working closely with the NIU mentors, picking up new skills in scientific web app development, and growing as a developer. Beyond the technical side, this journey is an opportunity to sharpen my problem-solving skills, collaborate in a real-world open-source environment, and make a meaningful difference in animal behavior research through Movement. Most of all, I'm excited to learn from this incredible community, give back by building a tool that researchers can rely on, and be part of a journey that I know will shape my future in amazing ways!

### Other Applications
I have not applied to any other organisations for GSoC, as I am fully dedicated to contributing to Movement and the NIU community. This project is my top priority, and I'm committed to giving it my all!