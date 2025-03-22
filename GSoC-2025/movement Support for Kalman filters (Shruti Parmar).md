# movement: Support for Kalman filters in movement (Shruti Parmar)

## Personal Details
- **Full Name:** Shruti Parmar 
- **Email:** shrutiparmar01082003@gmail.com 
- **GitHub Username:** shrutiparmar2003 
- **Zulip Username:** Shruti Parmar 
- **Location & Timezone:** Location : Jabalpur, Madhya Pradesh, India. Timezone : Asia/Kolkata  
- **Personal Website / Portfolio (optional):** [Github Profile](https://github.com/shrutiparmar2003) , [Linkedin Profile](https://www.linkedin.com/in/shruti-parmar-0625282a2/)

- **Code contribution**
Here’s a quick breakdown of how my PRs relate to each other :

- [First PR](https://github.com/neuroinformatics-unit/movement/pull/477) ([#477](https://github.com/neuroinformatics-unit/movement/pull/477)) – Initial Kalman filter experiment using simulated motion data, compared with other filtering methods.
- [Second PR](https://github.com/neuroinformatics-unit/movement/pull/484) ([#484](https://github.com/neuroinformatics-unit/movement/pull/484)) – Applied Kalman filtering to real-world data (SLEAP), implemented xarray integration.
- [Third PR](https://github.com/neuroinformatics-unit/movement/pull/496) ([#496](https://github.com/neuroinformatics-unit/movement/pull/496)) – Robust features: adaptive noise rejection, validation checks, basic Napari visualization, optimized filtering.

- **Proposal discussion link**
Please link to the pull request where you discussed your project proposal with the community. 

## Project Proposal

- **Synopsis**

  - **Project Overview:**  
  - To integrate a Python-based Kalman filter into Movement to enhance motion tracking by smoothing position, velocity, and acceleration data and extend functionality to handle identity switches in multi-animal tracking for improved accuracy.
    
  - **Why is it important:**  
  - Reduces noise in motion tracking, leading to more reliable state estimation enhancing accuracy and supports real-world applications crucial for biomechanics and computer vision, where precise tracking is essential.  
  
  - **What has been done?**  
  - I've implemented a functional Kalman filter for motion smoothing, applying it to both simulated and real-world SLEAP data. This includes velocity and acceleration estimation, adaptive noise rejection using Mahalanobis distance, and validation to ensure improved state estimation. I also added a basic Napari visualization to help interpret the filtered motion data.

  - **How would the open source community benefit from this project?** 
  This project helps researchers in neuroscience, robotics, and biomechanics by making motion tracking more accurate and reliable. By integrating it into the Movement package, it becomes easier to use and improve over time.

- **Implementation timeline**
   
- **Deliverables**
   - A Python implementation of a Kalman filter for smoothing position, velocity and acceleration timeseries.
   - Tests to cover any added functionality.
   - Documentation for the new functionality.
   - An example use case in the movement gallery.

- **Stretch goals**
-  A Python implementation of a Kalman filter for fixing identity switches in multi-animal tracking data (stretch goal).

- **Weekly timeline**


| **Phase**                | **Dates**                | **Planned Tasks & Deliverables**                                             |
|--------------------------|--------------------------|-----------------------------------------------------------------------------|
| **Pre-GSoC Phase 1**     | March 24 – April 8       | - Finalizing and submitting the GSoC proposal while continuing discussions with mentors and refining my contributions |
| **Pre-GSoC Phase 2**     | April 9 – May 8          | -  	Finalize approach with mentors, explore improvements (outlier handling, visualization), and select datasets.<br>- Ensure everything is aligned to keep the project on track. |
| **Community Bonding**    | May 8 – June 1           | - Since the groundwork is already in place, I'll refine the existing work and plan the next steps. |
| **Week 1**               | June 2 – June 9          | - Start the coding phase by improving how outliers are handled.<br> - I'll refine the Mahalanobis distance method and experiment with dynamic thresholding for more accurate filtering. Initial testing will be done on available datasets, with plans to expand to additional data if feasible |
| **Week 2**               | June 10 – June 16        | - Building on the filtering improvements, I'll refine the Napari visualization by overlaying raw vs. filtered motion data.<br>- I'll also test the filter on different datasets and fine-tune parameters to ensure it works well across various movement patterns. |
| **Week 3**               | June 17 – June 23        | - Right now, the Kalman filter has fixed parameters for process noise and measurement noise. However, movement patterns can vary significantly across different datasets,so :<br> -Refine the Kalman filter to ensure smooth tracking across different datasets, adjusting noise parameters for stability and better handling of sudden movements. |
| **Week 4**               | June 24 – June 30        | - Create unit tests for Kalman filter accuracy across datasets. Update documentation for better clarity and ease of contribution. |
| **Week 5 (Midterm Prep)**| July 1 – July 7          | -  Wrap up key improvements, check in with mentors, and prepare for midterm evaluation. Start preliminary exploration of identity switch detection if time allows. |
| **Week 6 (Midterm)**     | July 8 – July 14         | - Submit the midterm evaluation and go over feedback with mentors.<br>- After wrapping up the core work, I’ll dive into research papers and resources while also discussing ideas with mentors to get a solid understanding of identity switch detection. I’ll explore existing methods for multi-animal tracking and identity preservation before starting the implementation. |
| **Week 7**               | July 15 – July 21        | - Implement identity switch detection using methods like the Hungarian algorithm. Test with basic scenarios and refine for accuracy, focusing on edge cases for reliable tracking. |
| **Week 8**               | July 22 – July 28        | - Refine the identity switch detection algorithm and test it on more complex multi-animal scenarios, starting simple and gradually increasing the complexity.<br>- Optimize based on the results. |
| **Week 9**               | July 29 – August 4       | - As progress is made, deepen understanding of the algorithm. Test with diverse datasets, optimize performance, and refine accuracy. Prepare for final submission. |
| **Week 10**              | August 5 – August 11     | - Put in the final effort to polish the algorithm, making sure it works smoothly across all scenarios. Focus on fine-tuning performance and fixing any remaining issues.<br> - Wrap up documentation to ensure everything is clear and ready for the final submission. |
| **Week 11**              | August 12 – August 18    | - Finalize the project, complete testing, and make any last improvements. Prepare all deliverables, including code, documentation, and examples, for submission. |
| **Final Week**           | August 19 – September 1  | - Freeze the codebase, making sure everything is in its final, polished form. Submit the project along with all required deliverables.<br>- Review mentor feedback, make any final adjustments, and ensure the project is ready for future contributions. |


- **Communication Plan**

"I will manage my GSoC work alongside my college schedule by dedicating 4-5 hours each day and utilizing weekends (6-8 hours) to ensure consistent progress. I'll stay in regular touch with my mentor, with weekly check-ins via video calls (Zoom/Google Meet) and daily updates on Zulip for any quick feedback or questions."

---

## Personal Statement

- **Past experience.** 

**Academic Background** : 3rd-year Computer Science student specializing in Data Science, with a strong interest in AI/ML and data-driven applications. I am also Google Developer Groups (GDG) On-Campus Co-Lead, with active involvement in open-source and hackathons.  

**Real-World Data Experience**: Worked on real-world data challenges, particularly with noisy and complex datasets. I have developed an Indian Sign Language Translation system **(Patent Granted)** as a part of team to recognize and translate Indian Sign Language gestures into text and vice versa. Additionally, I have developed a Deepfake Detection System (ResNet + LSTM) **(Patent in progress)** processed time-series data and detected face swap deepfakes successfully. I've tackled various projects in data science, AI/ML, and NLP, enhancing my problem-solving and analytical skills.   

**Technical Skills**: Proficient in Python, C, and C++, with expertise in data science, ML (Scikit-learn, TensorFlow, Keras), deep learning (CNNs, ResNet, LSTM), data visualization (Matplotlib, Seaborn, Power BI), and database management (MySQL). Experienced with Git/GitHub, APIs, Streamlit, and GNOME (Linux).
[Open-Source Contributions](https://github.com/gitsofaryan/Hacktoberfest-Projects-2024/tree/main/Hacktobercpp)
Actively contributed to **Girlscript Summer of Code, Hacktoberfest, and Summer of Bitcoin**.  

- **Motivation: why this project?**
- I'm really excited about the potential to improve motion tracking, especially in areas like robotics and biomechanics, where getting precise, real-time data is so important. The Movement package, with its focus on Kalman Filtering to handle noisy data, seems like the perfect place to apply my skills. Having worked on Deepfake Detection (ResNet + LSTM) and Indian Sign Language Translation **(Patent Granted)**, I’ve tackled complex data challenges. This project is a great opportunity to apply my skills while contributing to an impactful open-source tool.

- **Match: why you?**
- I've tackled **Deepfake Detection (ResNet + LSTM) and ISL Translation, competed in **70+ hackathons**, winning multiple, including **2nd place at IIT Madras Guvi’s national hackathon**, **finalist at Eureka (IIT Bombay)**, and **9th in a national Data Engineering Hackathon**. Active in **GSSoC, Hacktoberfest, and Summer of Bitcoin**, I’m passionate about open-source and real-world solutions.


- **Availability**
My final exams are scheduled from May 21 to June 15, during which my availability may be slightly limited. However, I am committed to managing my time efficiently to ensure steady progress on the project. I will plan ahead, utilize my weekends effectively, and make up for any lost time before and after my exams to stay on track with the GSoC timeline.
    

## GSoC

_Extension: max 0.25 page_

- **GSoC experience**

    What do you expect from the program?
  - I see GSoC as a great opportunity to dive deeper into open-source development while sharpening my technical and collaboration skills. I'm excited about working with 
    experienced mentors, learning more about motion tracking and Kalman Filtering, and contributing to something that has real-world impact. More than just writing code, I 
    want to gain hands-on experience in building reliable, scalable solutions and be part of a community that’s passionate about solving challenging problems

- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, I am exclusively applying to NIU for GSoC 2025. I am very excited by the opportunity to work on this project, and I am very interested in learning more about Kalman Filters.
