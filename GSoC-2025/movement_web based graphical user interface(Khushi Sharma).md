Project title
movement: web-based graphical user interface(Khushi Sharma)

Personal details

Full name : Khushi Sharma

Email: khsharma2503@gmail.com

GitHub username: khushi-2503

Zulip username: Khushi Sharma

Location & time-zone : India (UTC+5:30)

Personal website / project portfolio (optional): https://khushi-2503.github.io/personal-website/

Code contribution : https://github.com/neuroinformatics-unit/movement/pull/528

Proposal discussion link : https://github.com/neuroinformatics-unit/gsoc/pull/33

Project Proposal

Synopsis

Movement is a powerful tool for analyzing keypoint and trajectory data. While it currently provides a Napari-based GUI, researchers and data scientists often rely on Jupyter Notebooks for their workflows. This project aims to develop a web-based GUI that enables interactive visualization within Jupyter, enhancing usability, accessibility, and collaboration.
Why is it Important?

1. Better accessibility: Researchers who prefer notebooks will have an intuitive interface without switching tools.

2. Improved collaboration: A web-based approach enables easier sharing and cloud-based workflows.

3. Expanded usability: Users can interactively explore, analyze, and visualize movement data in a more flexible environment.

Goals & Deliverables

1.Data Loading: Support for keypoint/bounding box trajectory files.
2. Video Visualization: Overlay trajectories on video and navigate frame-by-frame.
3. Data Exploration: Filtering, sorting, and visualization options.
4. Exporting: Save visualizations as images or videos.
5. Consistent UI: Maintain alignment with the existing Napari-based interface.
6. OpenAPI & REST API for Programmatic Access: Provide a well-documented API that allows external tools and scripts to interact with Movement’s web-based GUI. This will facilitate integration with Jupyter notebooks via a Python SDK and enable broader adoption by the research community.

Open Source Community Benefits

1. Enhances Movement’s usability by making it accessible in Jupyter Notebooks.

2. Encourages wider adoption among researchers in machine learning, neuroscience, and behavior analysis.

3. Provides an extensible foundation for future contributions and integrations.

Implementation timeline
Expected Weekly Commitment: 35-40 hours per week

Community Bonding Period (Before Official Coding Starts)

1. Familiarize with Movement’s codebase and data structures.

2. Engage with the mentor and community to finalize technical choices.

3. Explore visualization libraries (D3.js, Plotly) and integration with Jupyter.

4. Draft initial UI/UX wireframes for the web-based GUI.

Weekly Timeline

Week                            Task

Week 1                         Set up project structure, initialize Flask backend, and define API endpoints for data loading.

Week 2                         Implement trajectory data parsing and visualization using Matplotlib/Plotly in Jupyter.

Week 3                         Develop video overlay functionality to render keypoints over video frames.

Week 4                         Implement interactive filtering and sorting of movement data.

Week 5                         Create export functionality for images/videos of visualized data.

Week 6 (Mid-Term Evaluation)   Refine and test core features; submit for review.

Week 7                         Improve UI/UX for better user experience.

Week 8                         Add advanced visualization options and real-time interaction improvements.

Week 9                         Begin integration testing and bug fixes.

Week 10                        Write documentation and tutorials for users and developers.

Week 11                        Code freeze; finalize testing and optimize performance.

Week 12                        final project submission, gathering feedback, and refinining documentation

Stretch Goals(If Time Allows)

1. Implement real-time visualization updates.

2. Add support for additional file formats.

3. Explore potential cloud deployment options for remote access.

Communication Plan

1. Weekly Meetings: Zoom meetings with the mentor to discuss progress and challenges.

2. Asynchronous Communication: Zulip chat and GitHub discussions for quick updates and feedback.

3. Weekly Reports: Summarizing completed work,roadblocks, and next steps to be taken in project.

4. Mid-Term and Final Evaluations: Formal reviews of progress and refinements based on feedback.

By following this plan, I aim to build a robust,user-friendly, and well-documented web-based GUI along with mentors for Movement that enhances the experience for researchers worldwide!

Personal Statement

Past Experience

I have a strong background in Python, C, and web development, with experience building interactive web applications using Flask, HTML, CSS, and JavaScript. I have worked on several projects, including data visualization dashboards, an AI-powered finance management tool, and a custom email-sending application with dynamic templates. My experience with SQLite and MySQL has helped me efficiently manage and query large datasets.
I have worked on multiple web development projects, including a Smart Grocery List App with Price Comparison, a Personal Finance Management App with AI Budget Recommendations, and a tax assistant web application.These projects have given me experience in building intuitive user interfaces, working with APIs, and implementing real-time data visualization. 

I am also currently working under the supervision of my unversity professor on the project "Dynamic Bandwidth Allocation in Satellite Communication for better QoE". This project focuses on optimizing bandwidth allocation strategies in satellite networks to enhance the Quality of Experience (QoE) for end users. It involves real-time data analysis, machine learning models, and network optimization techniques, further solidifying my expertise in handling large-scale data processing and visualization.

Motivation: Why This Project?

I have a keen interest in Python and have extensively worked with it for data visualization, backend development, and algorithmic problem-solving. The flexibility and power of Python make it my preferred language for building efficient and scalable applications. This project provides an excellent opportunity to apply my Python expertise to enhance Movement’s usability and accessibility.
I am deeply interested in interactive data visualization and tools that enhance scientific research workflows. Many researchers struggle with handling and visualizing movement data effectively. By working on this project, I aim to bridge the gap between scientific computing and user-friendly interfaces, enabling seamless data exploration within Jupyter Notebooks.
This project also aligns with my passion for making advanced tools more accessible. A web-based GUI will democratize access to Movement, benefiting researchers, data scientists, and students who prefer working in Jupyter environments.

Match: Why Me?
My experience in full-stack development, data visualization, and API design makes me a strong fit for this project. I have previously built interactive dashboards, implemented APIs—all of which are essential for this project’s success.Beyond my technical skills, I am highly self-motivated and adaptable. I have consistently worked on complex projects independently and with teams, ensuring timely delivery while maintaining high code quality.

Availability
I am fully committed to GSoC and will dedicate 35-40 hours per week to this project. I have no conflicting schoolwork or job obligations during the coding period, ensuring my full focus on development, testing, and documentation.
By contributing to this project, I aim to enhance Movement’s usability and accessibility, ensuring that researchers worldwide can leverage its capabilities effortlessly.

GSoC

I see GSoC as an opportunity to deepen my involvement in open-source development while contributing to a project that has a meaningful impact. I look forward to collaborating with experienced mentors, improving my software development skills, and learning best practices for scalable and maintainable open-source contributions. Additionally, I hope to strengthen my ability to work in a community-driven environment, receive constructive feedback, and contribute effectively to discussions.
I have also applied to other organizations in GSoC 2025, but my final choice will depend on which project aligns best with my tech stack, skills, and interests. I am particularly drawn to this project because of its emphasis on interactive data visualization, Python development, and enhancing accessibility for researchers.
