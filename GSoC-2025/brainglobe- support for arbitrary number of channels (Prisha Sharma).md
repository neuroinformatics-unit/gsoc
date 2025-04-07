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
      <td><b>Week 1-2</b><br>Modify cell candidate detection for Multichannel detection</td>
      <td>
        <ol type="1">
          <li>Modify the cell candidate detection pipeline to handle N channels.</li>
          <li>Feature Extraction for Each Channel</li>
          <li>Normalize feature values across different channels </li>
          <li>Combine extracted features from all channels to create a comprehensive feature representation for each cell candidate</li>
          <li>Validate using real test images with 1, 2, and 3 channels</li>
          <li>Refine based on mentor's feedback</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 3-4</b><br>Modify Neural Network for Multichannel Input </td>
      <td>
        <ol type="1">
          <li>Expand the input layer to accept an arbitrary number of channels.</li>
          <li> Adjust CNN Feature Extractor for Multi-Channel Input.</li>
          <li> Modify fully connected (FC) layers to enable multi-class classification using a softmax output.</li>
          <li>Ensure compatibility of skip connections in Voxception-ResNet with the modified feature maps.</li>
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
          <li>Integrate trained multi-channel classification model into Cellfinder.</li>
          <li>Modify Cellfinder’s data pipeline to process multi-class outputs.</li>
          <li>Ensure detected cell labels are correctly assigned and stored.</li>
          <li>Validate integration with real test images.</li>
          <li>Ensure compatibility with existing Cellfinder visualization and segmentation tools.</li>
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
    <td><b>Stretch  Goal</b><br>•	Extend the model to support multi-channel outputs instead of just binary cell/non-cell classification. (Prototype)</td>
      <td>
        <ol type="1">
          <li>Enable classification of different cell types (e.g., Cell Type A, B, C, or Non-cell)..</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
  </tbody>
</table>

- **Communication plan**

  -	For any immediate doubts, I will prefer using Zulip for quick conversations.
  - For technical discussions and progress tracking, I will primarily use GitHub pull requests and issues.
  -	Additionally, I would appreciate weekly video calls to discuss updates and receive feedback
  -	I will maintain full transparency with my mentor and use these modes of communication wisely to ensure everything runs smoothly and this project turns out be success.

## Personal statement

_Length: max 0.75 page_

- **Past experience**

  -	I have been actively contributing to open-source organizations for a while, including a contribution to SunPy ( #8068, #8038), NumFOCUS (#146) and actively in NIU.

  -	My research paper, "Integration of Modern-Era Retrospective Analysis for Research and Applications, Version 2 (MERRA-2) Data and Lightning Detection Sensor (LDS) Data for Lightning Event Prediction", has been accepted by the Journal of Geomatics (Confirmation).

  -	I have been working in the field of Machine Learning and Deep Learning for the past two years, with experience in both Keras and PyTorch. Additionally, I have interned at the Indian Space Research Organisation (ISRO), where I applied advanced ML techniques for scientific research (Certificate)

  -	I was appointed as an AI and ML Engineer at NOT@MRP Pvt. Ltd., where I developed a personalized recommendation system and an intelligent chatbot for customer support.

Additionally, I was selected as a Grand Finalist in the Bhartiya Antariksh Hackathon organized by NRSC (National Remote Sensing Centre, ISRO centre that manages satellite and aerial data), ranking in the top 10 out of over 34,000 participating teams. I was also among the top 5 finalists in the India Festival Space Hackathon organized by ISRO (Indian Space Research Organisation), competing against more than 4,000 teams from across the country.

- **Motivation: why this project?**

  This project perfectly aligns with my interests in deep learning and scientific data processing. While working on a patient-doctor LLM-based project with the University of Ulster, I found myself deeply inspired by how AI can drive real impact in scientific research. I’ve worked extensively with multi-dimensional scientific datasets during my research on lightning prediction using MERRA-2 and LDS data. My experience lies in handling complex image data, particularly using tools like NumPy and Pandas to process, and extract insights from large-scale arrays and tabular datasets.

  In a previous project, I enhanced low-resolution images from the Moon’s South Pole, gaining hands-on experience with pre-processing raster image data (.tiff files). Currently, I’m applying similar skills in an AI-driven 3D terrain reconstruction system that converts 2D drone imagery into high-resolution DSMs and 3D geospatial meshes using customised Mega NERF model.
  
  What excites me the most about this NIU project is how closely it aligns with my experience and interests. I’m genuinely committed to contributing to the neuroinformatics community, and I see this project as a powerful way to support meaningful scientific discovery.

  I specifically chose the topic “Support for Arbitrary Number of Channels” because neuroscience datasets often include multiple imaging channels, and hardcoding fixed channel numbers limits experimentation and research flexibility. By contributing to this enhancement, I aim to improve usability handling diverse brain imaging data, helping tools better adapt to real-world scientific needs.

  For me, this isn’t just about writing code, it’s about using ML to push the boundaries. It’s a chance to bring together everything I love, research, AI, and open-source, to make a real difference.


- **Match: why you?**

  With a background in complex data set handling and AI, I believe I’m a great fit for this project. I’ve worked with tools like PyTorch, Keras, and Python, and one of my most rewarding projects involved increasing the SNR ratio of lunar South Pole images from -8 dB to 14 dB using advanced enhancement techniques (Github).

  Working with organizations like OpenAstronomy (SunPy) and NumFOCUS taught me how to contribute effectively to open-source, writing clean code and following community best practices. These experiences are especially relevant to a project like Support for Arbitrary Number of Channels, where flexibility and quality code matter.

  Interning at ISRO also shaped my approach—I learned the value of discipline, transparency, and staying committed even when tackling complex, high-stakes problems. I bring that same mindset to every project I 


- **Availability**

  I assure you of my complete availability for GSoC 2025, as I do not have any prior commitments. I will dedicate approximately 30-35 hours per week to ensure steady progress. Additionally, I will have a two-month-long vacation starting after May 28, 2025, which will allow me to fully focus on GSoC.

## GSoC

_Length: max 0.25 page_

- **GSoC experience**

  No, I have not participated in GSoC before.

  Through GSoC, I aim to deepen my open-source collaboration skills, improve my technical implementation abilities, and develop practical, well-documented solutions for the community.

- **Are you also applying to projects with other organisations in GSoC 2025?**

  I am applying exclusively to NIU for GSoC 2025 because this project aligns closely with my interests in image enhancement and machine learning.
