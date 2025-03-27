## Personal details

Please include the following information:

- **Full name**: Prisha Sharma
- **Email**: prishasharma4553@gmail.com
- **GitHub username**: parharti
- **Zulip username**: Prisha Sharma
- **Location & time-zone**: India, Indian Standard Time (GMT+5:30)
- **Personal website / project portfolio**: https://github.com/parharti
- **Code contribution**
<blockquote>
    <table>
        <tr>
            <td rowspan="5"><strong>PR</strong></td>
            <td><strong>Cellfinder</strong></td>
            <td><a href="https://github.com/brainglobe/cellfinder/pull/490">#490</a></td>
            <td>Inform the user when they supply just the weights in place of the full model</td>
        </tr>
        <tr>
            <td><strong>Cellfinder</strong></td>
            <td><a href="https://github.com/brainglobe/cellfinder/pull/499">#499</a></td>
            <td>Remove save weights option from training widget</td>
        </tr>
        <tr>
            <td><strong>Datashuttle</strong></td>
            <td><a href="https://github.com/neuroinformatics-unit/datashuttle/pull/470">#470</a></td>
            <td>Attempting to copy in the terminal user interface crashes on headless HPC</td>
        </tr>
    </table>
</blockquote>



## Project proposal

_Length: max 1 page_

**Synopsis**

This project aims to enhance CellFinder by adding multi-channel support for brain image classification. The goal is to extend CellFinder’s capabilities to process and classify cells from an arbitrary number of channels, making it more adaptable and improving its usability across different datasets. This enhancement is crucial, as some datasets may contain only a single signal channel, while others may have multiple signal channels carrying valuable information. By improving flexibility and accuracy, this project will make CellFinder a more powerful tool for the open-source neuroscience community.

### Deliverables

- Modify blob detection to support multiple channels.

- Enhance neural network for multi-channel cell classification.

- Ensure comprehensive testing for new functionalities.

- Provide detailed documentation for ease of use.

- Publish a blog post showcasing improvements with 1 & 3-channel images.

-  Bonus (if time allows): Implement a visualization tool to display detected cells across different channels, aiding interpretation.

**Implementation timeline**

<table>
  <thead>
    <tr>
      <th>Timeline</th>
      <th>Deliverables</th>
      <th>Hours/Week</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Community Bonding Period</b><br>Focus: Understanding</td>
      <td>
        <ol type="1">
          <li>Discuss project details with mentor and understand the codebase</li>
          <li>Explore existing multi-channel imaging datasets.</li>
          <li>Set up the development environment and resolve dependencies</li>
        </ol>
      </td>
      <td>15</td>
    </tr>
    <tr>
      <td><b>Week 1-2</b><br>Focus: Integrating attention into blob detection</td>
      <td>
        <ol type="1">
          <li>Modify the blob detection pipeline to process arbitrary channels through attention.</li>
          <li>Conduct multi-channel blob detection tests</li>
          <li>Refine based on mentor's feedback</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 3-4</b><br>Focus: Neural network integration</td>
      <td>
        <ol type="1">
          <li>Integrate attention modules into the neural network classifier to classify cell candidates from brain images with an arbitrary number of channels  .</li>
          <li>Start small-scale training experiments on multi-channel brain datasets.</li>
          <li>Refine based on mentor's feedback</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 5-6</b><br>Focus: Testing </td>
      <td>
        <ol type="1">
          <li>Write and finalize test cases (unit + integration tests).</li>
          <li>Refine based on mentor's feedback</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 7-8 </b><br>Focus: Benchmarking and Documentation</td>
      <td>
        <ol type="1">
          <li>Conduct large benchmark experiments on different brain image datasets.</li>
          <li>Write detailed usage documentation for multi-channel mode.</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 9-10</b><br>Focus: Final Documentation and Blog Draft</td>
      <td>
        <ol type="1">
          <li>Start preparing blog draft (problem, approach, results, visualizations).</li>
          <li>Final documentation polish.</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 11-12</b><br>Focus: Refinement and Finalization</td>
      <td>
        <ol type="1">
          <li>Submit final blog draft to mentors for review</li>
          <li>Address feedback and finalize all tests and documentation.</li>
        </ol>
      </td>
      <td>30</td>
    </tr>
    <tr>
      <td><b>Week 13</b><br>Focus: Add Final Submission and Wrap-up</td>
      <td>
        <ol type="1">
          <li> Submit final report.</li>
          <li>Make final PR to the main repository.</li>
          <li>Deliver blog post showcasing results on single-channel and multi-channel data</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
  </tbody>
</table>

- **Communication plan**

  For general discussions with my mentor, I plan to use Zulip or Slack for quick communication. For technical discussions and progress tracking, I will primarily use GitHub pull requests and issues. Additionally, I would appreciate weekly video calls to discuss updates, receive feedback, and ensure smooth progress.

## Personal statement

_Length: max 0.75 page_

- **Past experience**

  I have been actively contributing to open-source organizations for a while, including a contribution to SunPy (PR #8068), NumFOCUS.

  My research paper, "Integration of Modern-Era Retrospective Analysis for Research and Applications, Version 2 (MERRA-2) Data and Lightning Detection Sensor (LDS) Data for Lightning Event Prediction", has been accepted by the Journal of Geomatics.

  I have been working in the field of Machine Learning and Deep Learning for the past two years, with experience in both Keras and PyTorch. Additionally, I have interned at the Indian Space Research Organisation (ISRO), where I applied advanced ML techniques for scientific research.

- **Motivation: why this project?**

  This project perfectly aligns with my interests in image enhancement and deep learning. While working on a patient-doctor chatbot project with the University of Ulster, I developed a deep interest in AI's role in scientific research. Neuroscience, in particular, is a field that excites me deeply. Contributing to a project that supports scientific discovery through advanced ML methods is a wonderful opportunity to combine my technical skills with meaningful impact.

- **Match: why you?**

  With my experience in image enhancement and deep learning, I believe I am an excellent candidate for this project. I have hands-on experience with Keras, PyTorch, and Python. One of my notable projects is the enhancement of lunar south pole images, where I successfully increased the signal-to-noise ratio (SNR) from -8 dB to 14 dB using image enhancement techniques.

- **Availability**

  I assure you of my complete availability for GSoC 2025, as I do not have any prior commitments. I will dedicate approximately 30-35 hours per week to ensure steady progress. Additionally, I will have a two-month-long vacation starting after May 28, 2025, which will allow me to fully focus on GSoC.

## GSoC

_Length: max 0.25 page_

- **GSoC experience**

  No, I have not participated in GSoC before.

Through GSoC, I aim to deepen my open-source collaboration skills, improve my technical implementation abilities, and develop practical, well-documented solutions for the community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

  I am applying exclusively to NIU for GSoC 2025 because this project aligns closely with my interests in image enhancement and machine learning.
