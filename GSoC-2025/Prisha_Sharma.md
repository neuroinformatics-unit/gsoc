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
            <td>Inform the user when they supply just the weights in place of the full model (merged)</td>
        </tr>
        <tr>
            <td><strong>Cellfinder</strong></td>
            <td><a href="https://github.com/brainglobe/cellfinder/pull/499">#499</a></td>
            <td>Remove save weights option from training widget (merged)</td>
        </tr>
        <tr>
            <td><strong>Datashuttle</strong></td>
            <td><a href="https://github.com/neuroinformatics-unit/datashuttle/pull/470">#470</a></td>
            <td>Attempting to copy in the terminal user interface crashes on headless HPC (merged)</td>
        </tr>
    </table>
</blockquote>



## Project proposal

_Length: max 1 page_

**Synopsis**

This project aims to enhance CellFinder by adding multi-channel support for brain image classification. The goal is to extend CellFinder’s capabilities to process and classify cells from an arbitrary number of channels, making it more adaptable and improving its usability across different datasets. This enhancement is crucial, as some datasets may contain only a single signal channel, while others may have multiple signal channels carrying valuable information. By improving flexibility and accuracy, this project will make CellFinder a more powerful tool for the open-source neuroscience community.

### Deliverables

- Modify cell candidate detection to support multiple channels.

- Enhance neural network for multi-channel cell classification.

- Ensure comprehensive testing for new functionalities.

- Provide detailed documentation for ease of use.

- Publish a blog post showcasing improvements with 1 & 3-channel images.

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
      <td><b>Community Bonding Period</b><br> Understanding</td>
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
      <td><b>Week 1</b><br>Modify cell candidate detection for Multichannel detection</td>
      <td>
        <ol type="1">
          <li>Modify the cell candidate detection pipeline to handle N channels.</li>
          <li>Feature Extraction for Each Channel</li>
          <li>Normalize feature values across different channels </li>
          <li>Combine extracted features from all channels to create a comprehensive feature representation for each cell candidate</li>
          <li>Refine based on mentor's feedback</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 2</b><br>Refine Multichannel Cell Candidate Detection</td>
      <td>
        <ol type="1">
          <li>Optimize feature selection across channels for better accuracy</li>
          <li>Improve the detection algorithm based on cell shape, intensity, and texture to reduce false positives.</li>
          <li>Validate using real test images with 1, 2, and 3 channels</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 3-4</b><br>Modify Neural Network for Multichannel Input </td>
      <td>
        <ol type="1">
          <li>Expand the input layer to accept an arbitrary number of channels.</li>
          <li> Adjust convolutional layers for better feature extraction.</li>
          <li>Define new loss functions & evaluation metrics for multi-class classification.</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 5-6 </b><br>Train the Modified Neural Network</td>
      <td>
        <ol type="1">
          <li> Prepare training dataset with 1, 2, and 3-channel images..</li>
          <li>Train initial models for classification.</li>
          <li>Debug issues & optimize hyperparameters.</li>
          <li>Fine-tune model performance (reduce false positives/negatives).</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 7</b><br>Integrate Multichannel Classification into Cellfinder</td>
      <td>
        <ol type="1">
          <li>Modify to enable multi-class labeling.</li>
          <li>Ensure compatibility with existing pipeline.</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 8</b><br>Update Napari Visualization for Multichannel</td>
      <td>
        <ol type="1">
          <li>Modify napari viewer to support multi-channel overlays.</li>
        </ol>
      </td>
      <td>30</td>
    </tr>
    <tr>
      <td><b>Week 9-10</b><br>Testing & Documentation</td>
      <td>
        <ol type="1">
          <li>  Implement unit tests for modified functions.</li>
          <li> Compare new implementation with existing single-channel approach.</li>
          <li>Update Cellfinder documentation.</li>
          <li>Create user guide for running Cellfinder with different channel configurations.</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
    <td><b>Week 11-12</b><br>Prepare Blog Post on Multichannel Cellfinder</td>
      <td>
        <ol type="1">
          <li>Write an article on detecting & classifying cells with multichannel images.</li>
          <li>Include example workflows & results.</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
    <td><b>Week 13</b><br>Project Wrap-Up & Submission</td>
      <td>
        <ol type="1">
          <li>Submit final implementation & documentation..</li>
          <li>Publish blog post & showcase results.</li>
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
