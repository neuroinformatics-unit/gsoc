# movement: Support for Kalman filters in movement (Shruti Parmar)

## Personal Details
- **Full Name:** Shruti Parmar 
- **Email:** shrutiparmar01082003@gmail.com 
- **GitHub Username:** shrutiparmar2003 
- **Zulip Username:** Shruti Parmar 
- **Location & Timezone:** Location : Jabalpur, Madhya Pradesh, India. Timezone : Asia/Kolkata  
- **Personal Website / Portfolio (optional):** [Github Profile](https://github.com/shrutiparmar2003) , [Linkedin Profile](https://www.linkedin.com/in/shruti-parmar-0625282a2/)

- **Code contribution** :
   - I've been experimenting with a Kalman filter and learned a lot from my earlier PRs ([#477](https://github.com/neuroinformatics-unit/movement/pull/477) and [#484](https://github.com/neuroinformatics-unit/movement/pull/484) ), which helped shape my work in PR [#496](https://github.com/neuroinformatics-unit/movement/pull/496). While PR [#496](https://github.com/neuroinformatics-unit/movement/pull/496) is still in progress, I aim to refine the filter further by integrating it with Movement's built-in data structures. I initially tested the Kalman filter using the filterpy package, but it turned out to be outdated, so I’m now exploring more up-to-date alternatives for better performance and compatibility.

- **Proposal discussion link** : [Link](https://github.com/neuroinformatics-unit/gsoc/pull/8)


## Project Proposal

- **Synopsis**

To improve motion tracking in Movement by applying Kalman filtering to smooth position, velocity, and acceleration. Extend functionality to handle identity switches. Deliverables include code, tests, documentation, and a Movement gallery example. This improves tracking accuracy and provides an open-source tool researchers can use and build on.

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
| **Pre-GSoC Phase 2**     | April 9 – May 8          | - Explore and compare different Kalman filter implementations for Movement (NumPy-based, PyKalman, Dynamax, MovingPandas, and NFoursid). Test each for RMSE, noise stability, and integration with Movement’s data structure (Already tested filterpy but it's an outdated package.)|
| **Community Bonding**    | May 8 – June 1           | - Finalize the best Kalman filter approach with mentor's feedback. Compare methods based on accuracy, efficiency, and ease of integration. Plan the integration and refine the approach.|
| **Week 1**               | June 2 – June 9          | - Integrate the chosen Kalman filter into Movement, ensuring it processes position data correctly and outputs smoothed position, velocity, and acceleration .<br> Run initial tests to verify library functionality and basic operation within Movement. |
| **Week 2**               | June 10 – June 16        | - Apply the Kalman filter to Movement datasets by extracting, structuring, and filtering position data while preserving dimensions. Convert the output back into xarray DataArray objects and visualize raw vs. filtered data for comparison. |
| **Week 3**               | June 17 – June 23        | - Fine-tune Q & R—boost Q if lagging, adjust R if too jumpy. Test across datasets, using RMSE to balance accuracy and stability. |
| **Week 4**               | June 24 – June 30        | - Test and evaluate the Kalman filter by checking its accuracy on Movement data. Use synthetic data with added noise to see how well it performs, compare its results on both real and synthetic data.<br>- Document its strengths and limitations |
| **Week 5 (Midterm Prep)**| July 1 – July 7          | - Wrap up core implementation, refine filtering, and make sure everything aligns with Movement’s datasets and mentor feedback.<br> - Review and update function docstrings to match Movement’s style (likely NumPy docstring format) |
| **Week 6 (Midterm)**     | July 8 – July 14         | - Submit evaluation, review feedback, research identity switch detection methods with mentor’s guidance and research papers (Stretch goal). |
| **Week 7**               | July 15 – July 21        | - Explore identity switch detection methods, studying similar projects, and test a basic Hungarian algorithm on simple cases(2-animal crossings).<br>Run small-scale experiments to check feasibility and discuss findings with mentors to refine the approach |
| **Week 8 & Week 9**      | July 22 – Aug 04         | - Improve identity switch detection, gradually increasing complexity (e.g., 5 animals). <br> - Conduct benchmarking using RMSE, noise reduction, and filter stability.|
| **Week 10**              | August 5 – August 11     | - Finalize algorithms, ensure smooth execution, refine documentation  and prepare an example use case for the movement gallery |
| **Week 11**              | August 12 – August 18    | - Address final improvements, validate results, and package deliverables for submission. |
| **Final Week**           | August 19 – September 1  | - Freeze codebase, submit project, finalize documentation, mentor review |


- **Project Length**
  Medium-sized (175-hour) project
  
- **Communication Plan**

I'll dedicate 4-5 hours/day on weekdays and 6 hours on weekends. Regular check-ins with mentors via weekly video calls (Zoom/Google Meet) and daily Zulip updates for feedback

---

## Personal Statement

- **Past experience.** 

**Academic Background** : 3rd-year Computer Science student specializing in Data Science, with a strong interest in AI/ML and data-driven applications. I am also Google Developer Groups (GDG) On-Campus Co-Lead, with active involvement in open-source and hackathons.  
**Real-World Data Experience**: Worked on real-world data challenges, particularly with noisy and complex datasets. I have developed an Indian Sign Language Translation system **(Patent Granted)** as a part of team to recognize and translate Indian Sign Language gestures into text and vice versa. Additionally, I have developed a Deepfake Detection System (ResNet + LSTM) **(Patent in progress)** processed time-series data and detected face swap deepfakes successfully. I've tackled various projects in data science, AI/ML, and NLP, enhancing my problem-solving and analytical skills.   
**Technical Skills**: Proficient in Python, C, and C++, with expertise in data science, ML (Scikit-learn, TensorFlow, Keras), deep learning (CNNs, ResNet, LSTM), data visualization (Matplotlib, Seaborn, Power BI), and database management (MySQL). Experienced with Git/GitHub, APIs, Streamlit, and GNOME (Linux).
[Open-Source Contributions](https://github.com/gitsofaryan/Hacktoberfest-Projects-2024/tree/main/Hacktobercpp)
Actively contributed to **Girlscript Summer of Code, Hacktoberfest, and Summer of Bitcoin**.  

- **Motivation: why this project?**
- Working on ISL translation and Deepfake detection taught me the importance of accurate tracking. This project lets me apply those skills to improve motion tracking in Movement, making it more reliable for researchers.

- **Match: why you?**
- I’ve worked on AI/ML projects and competed in 70+ hackathons, winning 2nd at IIT Madras Guvi, finalist at IIT Bombay’s Eureka, and 9th in a national Data Engineering Hackathon. I’ve also contributed to open-source (GSSoC, Hacktoberfest, Summer of Bitcoin) and built real-world projects like Deepfake Detection and ISL Translation. These experiences make me well-prepared for this project.


- **Availability**
- My final university exams run from May 21 – June 15, during which my availability may be slightly limited. However, I will plan ahead, use weekends efficiently, and compensate before and after exams to stay on track.
    

## GSoC

- **GSoC experience**

    What do you expect from the program?
  - I see GSoC as a way to improve my open-source skills and work on a meaningful project. Learning more about Kalman filtering and motion tracking excites me, and I look forward to working with experienced mentors.

- **Are you also applying to projects with other organisations in GSoC 2025?**

    No, I am exclusively applying to NIU for GSoC 2025. I am very excited by the opportunity to work on this project, and I am very interested in learning more about Kalman Filters.
