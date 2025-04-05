Movement: Support For Kalman filters (Deepak Goel)
Personal Details
•	Full Name: Deepak Goel
•	Email: deepak.goel.pro@gmail.com
•	GitHub Username: deepakpro190
•	Zulip Username: Deepak Goel
•	Location & Time-zone: Delhi, India (IST, UTC+5:30)
•	Personal Website / Project Portfolio: deepakpro190
•	Proposal Discussion Link: https://github.com/neuroinformatics-unit/gsoc/pull/47/files

Project Proposal

Synopsis

This project aims to enhance the Movement library by integrating an optimized multi-object tracking system that ensures accurate position, velocity, and acceleration smoothing, while effectively handling identity switches in Multi-Animal Tracking.
At its core, the system will utilize an advanced Kalman Filter framework, rigorously benchmarked to select the most efficient configuration for the Movement dataset. To ensure robust and reliable tracking, the implementation will incorporate state-of-the-art identity association techniques, including:
•	Mahalanobis Distance & Hungarian Algorithm for optimal detection-to-track assignment, minimizing incorrect identity associations.
•	Joint Probabilistic Data Association (JPDA) to enhance stability in complex scenarios, where multiple animals interact or occlusions occur.
•	Re-Identification (Re-ID) with Deep Learning to extract deep feature embeddings from animal appearances, ensuring long-term identity tracking.
To further improve decision-making, the tracking pipeline will compute a dynamic confidence score for each frame, integrating:
•	Motion Consistency Score, derived from Kalman Filter-based trajectory predictions.
•	Appearance Similarity Score, leveraging deep CNN feature embeddings for Re-ID.
•	Final Fusion Score, a weighted combination of motion and appearance cues for robust identity resolution.
By the project's completion, the Movement library will feature a highly accurate, AI-powered multi-animal tracking pipeline capable of handling occlusions, identity switches, and non-linear motion. This will provide researchers and developers with a scalable, efficient, and reliable tracking system, tailored for biological movement analysis, behavioral studies, and large-scale multi-animal research. 

Implementation Timeline

Deliverables

•	Integration of a Kalman Filter for position, velocity, and acceleration smoothing.
•	Implementation of identity switch correction using Mahalanobis distance and the Hungarian Algorithm.
•	Incorporation of Joint Probabilistic Data Association (JPDA) to handle identity assignment in complex tracking scenarios, reducing errors in cases of occlusions and overlapping trajectories.
•	Re-Identification (Re-ID) Module utilizing deep learning-based feature extraction, ensuring long-term identity consistency across frames.
•	Benchmarking and testing of smoothing and identity correction algorithms on synthetic and real datasets.
•	Comprehensive documentation, including function docstrings, integration guides, and example use cases for the Movement library.
•	Unit tests to ensure the correctness and stability of implemented features.

Stretch Goal
•	Extending the Kalman Filter to support automatic parameter tuning where applicable (like Expectation-Maximization or Adaptive Noise Expectation).
•	Implementing additional identity correction heuristics if needed.

________________________________________
📅 Weeks & Phase Distribution for 12 Weeks

Pre-GSoC Phase 1 (March 24 – April 8)
•	Finalizing and submitting the GSoC proposal.
•	Exploring the Movement codebase, documentation, and testing framework.
•	Fixing minor bugs and implementing small test cases to understand Movement’s internal workflow.
Pre-GSoC Phase 2 (April 9 – May 8)
•	Conduct a comparative study of Kalman Filter (KF) implementations: PyKalman, NFoursid, Dynamax, MovingPandas.
•	Implement and evaluate basic KF on synthetic noisy data for position tracking.
•	Compare results across different implementations to finalize the best approach.
Community Bonding Period (May 8 – June 1)
•	Discuss the best KF approach with mentors based on experiments.
•	Research identity switch correction and data association techniques (Hungarian Algorithm, Mahalanobis Distance, JPDA).
•	Plan integration of confidence scores for re-identification in Movement.
________________________________________
🔹 Coding Phase 1: Kalman Filtering for Multi-Entity Motion Tracking
Week 1 (June 2 – June 8)
•	Implement basic Kalman Filter for position smoothing.
•	Generate synthetic position data and evaluate filtering accuracy.
•	Fix initial bugs and ensure seamless integration with Movement datasets.
Week 2 (June 9 – June 15)
•	Extend Kalman Filter to smooth velocity and acceleration data.
•	Validate on Movement datasets and optimize performance.
Week 3 (June 16 – June 22)
•	Implement Expectation-Maximization (EM) for parameter tuning, if applicable.
•	Conduct a thorough review and integrate mentor feedback.
•	Develop unit tests for Kalman Filter smoothing.
Week 4 (June 23 – June 29)
•	Write detailed documentation & docstrings for the Kalman Filter module.
•	Create an initial example use case for Movement's gallery.
Week 5 (June 30 – July 6)
•	Final refinements and optimizations to Kalman Filter implementation.
•	Prepare for mid-term evaluations and submit progress reports.
________________________________________
🔹 Coding Phase 2: Identity Association & Re-Identification
Week 6 (July 7 – July 13) — Mid-Term Evaluation
•	Submit mid-term evaluation and review feedback.
•	Conduct final testing & performance evaluation for Kalman Filter.
Week 7 (July 14 – July 20)
•	Research and experiment with Hungarian Algorithm & Mahalanobis Distance for identity tracking.
•	Gather relevant datasets and discuss the re-identification approach with mentors.
Week 8 (July 21 – July 27)
•	Implement identity switch correction using Hungarian Algorithm & Mahalanobis Distance.
•	Utilize Kalman Filter predictions for identity tracking.
•	Validate with test cases and refine based on mentor feedback.
Week 9 (July 28 – August 3)
•	Improve identity tracking for occlusions & path crossings.
•	Introduce confidence scores for re-identification and association.
Week 10 (August 4 – August 10)
•	Develop unit tests for identity switch correction.
•	Integrate the correction module into Movement’s tracking pipeline.
________________________________________
Week 11 (August 11 – August 17)
•	Implement Joint Probabilistic Data Association (JPDA) for complex tracking cases.
•	Create a detailed use case example for identity switch correction and re-identification.
•	Write documentation & integration guide for Movement users.
Final Week (August 18 – September 1)
•	Codebase freeze & final performance evaluation.
•	Conduct extensive testing & mentor reviews.
•	Submit the final GSoC report and complete project handover.

Communication Plan with Mentors
•	Weekly Meetings: Scheduled weekly sync-up meetings with mentors to discuss progress and resolve issues.
•	GitHub Discussions: Use GitHub issues and discussions for technical queries and code reviews.
•	Google Docs: For collaborative documentation and mentor feedback.

Personal Information

Past Experience

Vehicle & License Plate Recognition (YOLO & OCR)
•	Developed a real-time vehicle tracking system using YOLOv8-L, achieving 99.47% mAP@50.
•	Integrated OCR for license plate text extraction in images and videos.
•	Relevance: Experience with tracking, identity re-identification (Re-ID), Hungarian algorithm-based assignment, and Kalman filters.
Sentiment Analyzer
•	Fine-tuned RoBERTa (94.04% accuracy) and optimized LSTM for sentiment classification.
•	Relevance: Hands-on sequence modeling and state estimation, useful for Kalman filtering and tracking optimizations.
RAG-based Financial Chatbot
•	Built a multi-agent system for query routing, improving efficiency by 50%.
•	Relevance: Experience with multi-agent coordination, useful for identity tracking and confidence-based Re-ID.
Internship at NSUT (BiasFinder Project)
•	Worked with large datasets (IMDb: 50K, Twitter: 1.6M), gaining expertise in data processing and model evaluation.
•	Relevance: Handling noisy real-world data, essential for identity tracking challenges.
Relevant Coursework
•	Design & Analysis of Algorithms, Optimization Techniques, Machine Learning, Computer Vision – Strengthens expertise in tracking, filtering, and optimization for the project.


Motivation
•	Fascinated by the challenges of multi-object tracking and improving motion estimation in real-world scenarios.
•	Interested in applying probabilistic filtering techniques to enhance tracking accuracy and stability.
•	Drawn to open-source collaboration, seeing it as an opportunity to contribute meaningfully while learning from experienced mentors.
•	Excited to work on a project that blends algorithmic efficiency with practical impact, particularly in identity assignment and re-identification.
Why Me?
•	Background in data-driven model optimization, including experience with filtering methods and structured tracking pipelines.
•	Comfortable with experimenting and iterating on tracking solutions, balancing theory with practical implementation.
•	Experience working on projects involving object recognition and feature matching, which align with identity tracking challenges.
•	Detail-oriented in testing and documentation, ensuring clarity and usability in implementations.
•	Committed to open-source development, eager to engage with the community and refine solutions through collaboration.
Availability
•	I commit to dedicating 200+ hours to this project and do not have any planned vacations or 
travel during the program. 
•	 My working hours are as follows (UTC +5:30): 

Weekday Availability (5-6️ hours/day) 
• 11:00-18:00 IST 
Weekend Availability (4-5 hours/day) 
• 11:00-16:00 IST 

•	I am flexible and willing to adjust and re-plan my schedule based on project requirements 
and mentor feedback..

GSoC
GSoC Experience
•	This is my first time applying for GSoC, and I am enthusiastic about the chance to contribute to a meaningful open-source initiative. I have actively explored past GSoC projects, studied relevant discussions, and engaged with the community to gain insights into the development process and best practices.
•	 I look forward to collaborating with experienced mentors and making a substantial impact on the project.I have been following previous GSoC contributions and community discussions to understand the workflow.
Applying to Other Orgs?
•	No, this is my sole application. My full attention and dedication are directed toward this project, and I am committed to ensuring its successful execution.

