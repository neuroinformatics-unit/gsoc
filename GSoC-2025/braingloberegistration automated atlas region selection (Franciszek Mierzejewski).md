# BrainGlobe-Registration – Google Summer of Code 2025

## Personal Details

Name: Franciszek Mierzejewski

Zulip Name: Franciszek Mierzejewski

Email: [franek.mski@gmail.com](mailto:franek.mski@gmail.com)

GitHub: [FranciszekMierzejewski](https://github.com/FranciszekMierzejewski)

LinkedIn: [LinkedIn Profile](https://www.linkedin.com/in/franciszek-mierzejewski-1914b0350/)

Phone: (+44) 07922 723272

Country: Colchester, United Kingdom

Timezone: GMT+1

Language: English

Code Contribution Link: https://github.com/brainglobe/brainglobe-registration/pull/87
Project Discussion Link: https://github.com/neuroinformatics-unit/gsoc/pull/53

## Project Proposal

### Synopsis

The BrainGlobe-Registration tool currently manually aligns atlas regions for 2D or 3D brain images to brain atlases, this process is time-expensive, prone to errors and inefficient. The aim of this project is to tackle these issues by the means of automating optimal atlas regions identification through methods such as Convolutional Neural Networks (CNNs), Bayesian Optimisation and Adaptive Grid Search. This approach will ensure a higher accuracy and reproducibility of results that is crucial in scientific cross-examination.

### Deliverables

The minimum set of deliverables I aim to achieve are:
- Implement a new preprocessing step to automatically select the optimal atlas region.
- Compare at least two region-selection methods (e.g., CNNs and Adapative Grid Search).
- Perform extensive tests to ensure stability with existing brainglobe-registration workflow.
- Provide clear documentation detailing usage instructions and example cases.
- Write a blog post showcasing the features of the project and its impact

If time allows it, I'll complete the following:
- Implement another method to select optimal atlas region.

### Timeline

The [project description](https://neuroinformatics.dev/get-involved/gsoc/projects_2025/brainglobe.html) details either a medium (~175 hours) or large (~350 hours) duration. Given my experience, I have chosen to apply for medium (~175 hours) duration. The timetable constructed is formed with end of year university exams in mind. These exams run from the 15<sup>th</sup> to the 23<sup>rd</sup> of May.

| Stage | Title | Start Date | End Date | Hours Assigned |
| --- | --- | --- | --- | --- |
| I   | Community Bonding Period (getting familiar with codebase and structure) | 08/05/25 | 14/05/25 | 15  |
| II  | Research Different Methods to Select Region | 24/05/25 | 27/05/25 | 20  |
| III | Write Up Quantitative Comparison of Methods | 28/05/25 | 01/06/25 | 10  |
| IV  | Evaluation I – Choose Method | 02/06/25 | 03/06/25 | 5   |
| V   | Implement Chosen Method | 04/06/25 | 09/07/25 | 40  |
| VI  | Optimise Code | 10/07/25 | 13/07/25 | 10  |
| VII | Evaluation II | 14/07/25 | 17/07/25 | 10  |
| VIII | Conduct Tests (same time as IX) | 18/07/25 | 15/08/25 | 25  |
| IX  | Rectify Errors Found From Tests | 18/07/25 | 15/08/25 | 10  |
| X   | Write Up Blog & Documentation | 16/08/25 | 23/08/25 | 20  |
| XI  | Final Evaluation | 24/08/25 | 31/08/25 | 20  |

I plan to host weekly meetings on Zulip with my mentor discussing current progress and plans. In the case where the timeline is disrupted (e.g. task completion delay), I’ll contact my mentor to discuss the reason behind the delay and the best course of action. It may be in the best interest of NIU to postpone the delayed task to focus on higher priority tasks.

## Personal Statement

### About Me

I’m Franciszek Mierzejewski, a 1<sup>st</sup> year student from the University of Essex studying towards a Bachelor of Science Degree in Computer Science.

### Past Experience

I have worked on an open-source project before – DryPi, a team submission to the 2023 AstroPi competition (hosted by European Space Agency and Raspberry Pi Foundation) that with Artificial Intelligence used images taken from a Rapberry Pi 4 Model 4 to calculate NDVI (Normalised Difference Vegetation Index) values that analysed near-infrared and red light reflectance (a grayscale image) to map to a colourmap to generate into a false-colour image. This false-color image, alongside the International Space Station (ISS) coordinates at the time of the image being taken, was then used to compare with historical open-source data to look at how vegetation density has changed on different continents in the last few decades. It achieved ‘Flight Status’ on the ISS in May 2023. The code for DryPi can be found at: [GitHub - DryPi](https://github.com/FranciszekMierzejewski/AstroPi-Team-DryPi)

I have had experience with coding in Python (3 years) and NumPy, working with and processing image data. Although I have no experience with ITK or Elastix, I would be learning it as part of my research prior to my project implementation. An example of my experience in machine learning can be taken from a [module](https://www1.essex.ac.uk/modules/Default.aspx?coursecode=CE101&level=4&period=FY&campus=CO) at my university where I applied K-Nearest-Neighbour, Support Vector Machine and Extreme Gradient Boosting (amongst other) algorithms to predict heart disease of patients. The documentation of the project progress can be found [here](https://drive.google.com/file/d/1lJsK8pFbCAYZ0sB8rczpWF_0sl9xBfRG/view?usp=sharing)

### Availability

I am available throughout the whole work period, apart from the exam period mentioned earlier which has been taken into account in my timetable.

## GSoC

In recent months I have grown fascinated with neurocomputation and wish to pursue it as a career path. It is my hope that contributing to NIU will be a milestone towards this goal. This is the only project I have applied to in GSoC 2025.

I would be honoured if given the opportunity to undertake this project under the mentorship of Igor Tatarnikov and Alessandro Felder. Regardless of the outcome of this proposal, I will continue to contribute to open-source projects to gain experience and plan to participate in research studies – in the hope that my involvement in the field will make someone’s life better, someday.

Thank you for taking my application into consideration.