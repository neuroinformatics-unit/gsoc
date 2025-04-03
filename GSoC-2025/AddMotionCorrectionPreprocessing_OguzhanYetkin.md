Add motion correction preprocessing (Oguzhan Yetkin)
Personal Details

    Full Name: Oguzhan Yetkin

    Email: oguzhan.yetkin123@gmail.com

    GitHub Username: OguzhanTheCoder

    Zulip Username: Oguzhan Yetkin

    Location & Time Zone:  Germany (CET)


    Code Contribution:
    I have not yet contributed to open source projects, and my GitHub profile is currently empty. However, I am fully committed to starting my open source journey. I plan to create my first meaningful pull request for spikewrap—integrating motion correction preprocessing—during the community bonding period.

    Proposal Discussion Link:
    I will initiate a discussion on the NIU GitHub channel as soon as my initial PR is ready.

Project Proposal
Synopsis

Extracellular electrophysiology allows the recording of thousands of neurons simultaneously to study brain activity via spike sorting. spikewrap, built on top of SpikeInterface, streamlines electrophysiological preprocessing and spike sorting. This project will add motion correction preprocessing to spikewrap, addressing mechanical drift in recordings and improving the accuracy of spike sorting. Deliverables include the integration of SpikeInterface’s motion correction functionality, comprehensive unit tests, and updated user documentation with clear usage examples. This enhancement will significantly benefit the open-source neuroscience community by providing more reliable preprocessing tools.
Implementation Timeline

Minimal Deliverables:

    Integration:

        Add SpikeInterface’s motion correction functionality to the spikewrap codebase.

    Testing:

        Develop comprehensive unit tests for the motion correction functions.

    Documentation:

        Update spikewrap documentation with detailed usage examples and guidelines.

Weekly Timeline (Approximately 30 hours/week, 12 weeks total – ~350 hours):

    Community Bonding (Pre-GSoC / Week 0):

        Set up the development environment (spikewrap, SpikeInterface).

        Review the existing spikewrap codebase and relevant motion correction modules.

    Week 1:

        Develop an initial prototype integrating basic motion correction functionality into spikewrap.

    Week 2:

        Refine the prototype to ensure proper data ingestion and preprocessing.

        Begin preliminary testing on sample electrophysiological datasets.

    Week 3:

        Expand integration to support various motion correction presets; document parameter effects.

    Week 4:

        Develop unit tests for the motion correction module (target: ~50% coverage).

    Week 5:

        Increase test coverage to approximately 75% by incorporating edge cases and diverse datasets.

    Week 6 (Mid-term Checkpoint):

        Deliver a functional prototype with near-complete unit test coverage and an initial draft of user documentation.

    Week 7:

        Optimize the motion correction pipeline for speed and accuracy; incorporate mentor feedback.

    Week 8:

        Implement performance benchmarks comparing different motion correction presets.

    Week 9:

        Draft detailed user documentation with step-by-step examples and troubleshooting guidelines.

    Week 10:

        Finalize documentation and polish the integration; prepare a demo script showcasing improvements.

    Week 11:

        Code freeze; perform intensive debugging and finalize tests across multiple datasets.

    Week 12:

        Complete final documentation, produce a demo video, and prepare the final submission.

Communication Plan

    Weekly Meetings:

        Regular video calls (via Zoom or Google Meet) with my mentor (@JoeZiminski) and the team to review progress and gather feedback.

    Daily Updates:

        Brief status updates via Zulip chat and GitHub pull requests.

    Review Process:

        Regular code reviews and discussions on pull requests to ensure smooth integration and clear documentation.

Personal Statement
Past Experience

I hold a B.Sc. in Psychology and am currently completing my M.Sc. in Artificial Intelligence at Vrije Universiteit Amsterdam, with a focus on machine learning, signal processing, and robotics. I have professional experience as a software developer at Construktiv GmbH, where I developed solutions using Python and C++. My project experience includes electrophysiological data analysis (e.g., EEG), deep learning using PyTorch and TensorFlow, robotics (using ROS and Gazebo), and reinforcement learning algorithms.
Motivation: Why This Project?

Accurate preprocessing of extracellular electrophysiological data is critical for reliable spike sorting and neural analysis. Adding motion correction to spikewrap will mitigate mechanical drift, thereby significantly enhancing data quality. I am passionate about the intersection of neuroscience and AI, and this project directly supports my long-term goal of pursuing a PhD in Brain–Computer Interface research. Improved preprocessing tools will have a meaningful impact on neural data analysis and ultimately on neuroprosthetics and brain–computer interfaces, laying the groundwork for advanced research in this field.
Match: Why Me?

My interdisciplinary background in psychology, neuroscience, and AI, combined with strong programming skills in Python and C++, makes me well-suited for this project. Although I have not yet contributed to open source, my experience in developing complex personal projects and my hands-on expertise in signal processing and data analysis ensure that I can successfully integrate motion correction functionality into spikewrap. My commitment to advancing neurotechnology is underscored by my plans to pursue a PhD in Brain–Computer Interface research, and this project is a natural step toward achieving that goal.
Availability

I am fully available throughout the GSoC period with no conflicting commitments, allowing me to dedicate my complete focus to this project.