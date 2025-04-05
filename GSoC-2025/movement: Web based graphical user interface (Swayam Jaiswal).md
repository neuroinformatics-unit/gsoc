## Project title movement: Web-based graphical user interface for movement (Swayam Jaiswal)


## Personal details
- **Full name**: Swayam Jaiswal
- **Email**: swayamjai0444@gmail.com
- **GitHub username**: Swayamjexe
- **Zulip username**: Swayam Jaiswal
- **Location & time-zone**: India, Indian Standard Time (GMT+5:30)
- **Code contribution**

    I have submitted a draft pull request for the prototype version of the Jupyter-based GUI for movement. This prototype introduces video playback with overlaid pose tracks, enabling researchers to interactively explore pose estimation data within notebook environments.
  [Link to Pull Request] (https://github.com/neuroinformatics-unit/movement/pull/542)

- **Proposal discussion link**

    [Proposal Discussion](https://github.com/neuroinformatics-unit/gsoc/pull/57)

## Project proposal 
- **Synopsis**
  
    Pose estimation is widely used in biomechanics, neuroscience, and human-computer interaction for analyzing movement data. The movement library provides powerful data visualization tools for pose estimation research, but its current functionality is limited to static visualizations in Jupyter Notebooks and a napari-based GUI that must be run through a terminal on a local machine.
    
    Many researchers prefer web-based or Jupyter-integrated environments for tasks like data visualization and motion quantification, as these offer greater accessibility and flexibility. This project aims to enhance movement's usability by developing a web-based GUI, allowing users to interactively explore, analyze, and export pose estimation data. The GUI will be compatible with Jupyter, Google Colab, and standalone web environments, making pose analysis more intuitive and scalable.

    Key Features
    
    •	Load and overlay pose estimation data on video frames.
    
    •	Interactive tools for filtering and analyzing keypoints/trajectories.
    
    •	Playback functionality for dynamic visualization of pose data.
    
    •	Export capabilities for saving visualizations as images or videos.




- **Implementation timeline**

    **Minimal Deliverables**
      
    •	Develop a notebook-integrated GUI for interactive pose estimation and visualization.
    
    •	Ensure compatibility with Jupyter environments like Google Colab.
    
    •	Maintain consistency with the existing napari implementation, ensuring a similar workflow and using key libraries such as VideoReader for frame handling.
    
    •	Implement core GUI functionalities, including 	Loading pose estimation data  &	Interactive playback of pose tracks
    
    **Stretch Goals** (if time allows)
  
    •	Cloud deployment for broader accessibility.
    
    •	Additional visualization widgets to integrate more movement functions beyond basic playback.


    **Weekly Timeline**:
      | **Week & Dates** | **Tasks & Deliverables** |
    |------------------|-------------------------|
    | **Week 1** | Initial setup, community bonding, and understanding the codebase. Engage with mentors and explore project requirements. **(12-15 hrs)** |
    | **Week 2** | Implement initial features, set up the development environment, and explore **fastplotlib** and **Plotly Dash** for visualization. **(15-18 hrs)** |
    | **Week 3** | Develop core functionalities: loading pose estimation data, integrating **VideoReader** for frame handling, and beginning basic UI prototyping. **(18-20 hrs)** |
    | **Week 4** | Continue feature development, implement **interactive playback functionality**, and start integrating widgets for visualization. **(18-22 hrs)** |
    | **Week 5 (Midterm Review)** | Complete major features, refine interactivity, and collect feedback from mentors/community. **(20-22 hrs)** |
    | **Week 6** | Optimize code, improve **UI/UX**, and implement additional functionalities like **filtering keypoints/trajectories**. **(20-22 hrs)** |
    | **Week 7** | Address mentor feedback, enhance **visualization features**, improve **state management**, and refine documentation. **(18-20 hrs)** |
    | **Week 8** | Bug fixes, stress testing GUI performance, and optimizing data handling in **Jupyter/Colab environments**. **(18-22 hrs)** |
    | **Week 9** | Finalizing features, ensuring stability, and preparing for usability testing. **(18-20 hrs)** |
    | **Week 10** | **Code Freeze:** Refine tests and documentation, ensure feature completeness. **(15-18 hrs)** |
    | **Week 11** | Final testing, resolving edge cases, preparing for submission. **(12-15 hrs)** |
    | **Week 12  (Final Submission)** | Submit the final project, mentor reviews, and complete wrap-up tasks. **(10-12 hrs)** |


    **Planned Work Hours per Week**: 15-22 hours/week
  
    (Adjustable based on project needs and feedback.)


- **Communication plan**
  
    •	Meeting Frequency: Weekly check-ins with the mentor, with additional meetings if needed.
      
    •	Daily Updates: Regular progress updates via Zulip chat for quick feedback.
    
    •	Communication Channels: Zulip chat for discussions, GitHub issues for tracking progress, and occasional video calls for in-depth reviews.
    
    •	Progress Reports: Weekly reports maintained in a log style for summarizing development milestones, challenges, and next steps, shared via GitHub or a Zulip.



## Personal statement


- **Past experience.** 

    I have three years of coding experience in Python, specializing in AI, Machine Learning, and Deep Learning. My expertise includes computer vision, motion tracking, and real-time video analysis, with hands-on experience in PyTorch, scikit-learn, OpenCV, VideoReader, and Plotly Dash.
      
    I have developed several projects, including CogniSafe, a real-time threat detection system using an ensemble of ResNet50 and a custom model, and a GenAI-powered resume analysis tool that matched job descriptions with user resumes. I also worked on multimodal plant species classification using Sentinel-2, Landsat, and Chelsa data with a Siamese network and ResNet18.
    
    While I am new to open-source contributions, I actively use GitHub for version control and have experience maintaining projects collaboratively. As a Computer Engineering student, coursework in Data Structures, Data Science, and Software Engineering has strengthened my ability to build scalable solutions.

- **Motivation: why this project?**

    I enjoy building solutions that make life easier, and this project directly contributes to that by enhancing researchers' ability to interact with pose estimation data in familiar environments like Jupyter and Colab. Improving interactivity and usability for movement aligns perfectly with my passion for developing tools that simplify complex workflows.
      
    Technically, this project allows me to showcase and deepen my Python expertise by working with advanced libraries like Plotly Dash, VideoReader, and fastplotlib while reinforcing best practices in scalability, maintainability, and testing. It also gives me exposure to real-world open-source development, an area I want to explore further.
    
    The impact of this project extends beyond individual users—researchers in neuroscience, biomechanics, conservation, and ethology rely on pose estimation tools like DeepLab and SLEAP for tracking movements without physical markers. By providing an intuitive, web-based visualization interface, movement along with my work will help standardize and simplify this process, ensuring more efficient analysis within commonly used research environments.

- **Match: why you?**

    My strong Python background, experience with data visualization (Matplotlib, Plotly, OpenCV), and GUI development (Tkinter) make me a strong fit for this project. I have built numerous projects in python in various domains wih different tech stacks which demonstrates my ability to integrate multiple technologies into intuitive applications. With my expertise in Python, visualization, and AI, I am confident in delivering a scalable, interactive web-based GUI to enhance movement’s usability for researchers.

- **Availability**

    I will be fully available during the GSoC work period, while I am attending my course, I do not have any other commitments towards any other internship or research work and can fully dedicate my time towards this project with a planned schedule. I am flexible to adjust under any other time zones, especially for meetings whenever needed.   

    

## GSoC

- **GSoC experience**

    This is my first time applying to GSoC or contributing to an open-source program, and I’m excited about the opportunity to work on movement. Through this project, I aim to enhance my skills, gain hands-on experience, and learn from experienced mentors and industry experts while making meaningful contributions to the community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, this is my only proposal and I want to solely focus on this project.
