# datashuttle: Allow Google Drive or AWS as remote storage
## Personal Details
- **Full Name:** Angajala Sumana Sree
- **Preferred Name:** Sumana
- **Email:** sumanasree2705@gmail.com
- **Github Username:** sumana-2705
- **Zulip Username:** Sumana Sree
- **Location & time-zone:** Anantapur, India (GMT+5:30)
- **Portfolio Website:** https://sumana-2705.github.io/Sumana-Portfolio/
- **Proposal discussion link:** https://github.com/neuroinformatics-unit/gsoc/pull/5
- **Code contribution:**
<blockquote>
  <table>
    <tr>
      <td rowspan="6"><strong>In Datashuttle</strong></td>
      <td><a href="https://github.com/neuroinformatics-unit/datashuttle/pull/487">#487</a></td>
      <td>Fixed log directory creation issue in _start_log</td>
    </tr>
    <tr>
      <td><a href="https://github.com/neuroinformatics-unit/datashuttle/pull/501">#501</a></td>
      <td>Added support for custom tags in template input with regex conversion</td>
    </tr>
    <tr>
    <tr>
      <td><a href="https://github.com/neuroinformatics-unit/datashuttle/pull/495">#495</a></td>
      <td>Show Warning message for Existing Folder Creation in TUI</td>
    </tr>
    <tr>
      <td><a href="https://github.com/neuroinformatics-unit/datashuttle/pull/489">#489</a></td>
      <td>Added Projects List Button on Project Manager Screen</td>
    </tr>
    <tr>
      <td><a href="https://github.com/neuroinformatics-unit/datashuttle/pull/475">#475</a></td>
      <td>Updated tree view while selecting location of new project</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>PRs related to Python</strong></td>
      <td><a href="https://github.com/aeon-toolkit/aeon/pull/2419">#2419</a></td>
      <td>Add LITETimeClassifier Example to Classification Notebook</td>
    </tr>
    <tr>
      <td><a href="https://github.com/flyteorg/flytesnacks/pull/1739">#1739</a></td>
      <td>Added examples for tensorflow types in Datatypes and IO section</td>
    </tr>
    <tr>
      <td rowspan="3"><strong>PRs related to UI/UX</strong></td>
      <td><a href="https://github.com/ruxailab/RUXAILAB/pull/599">#599</a></td>
      <td>Improve responsiveness of User Test Preview with a cleaner layout</td>
    </tr>
    <tr>
      <td><a href="https://github.com/ruxailab/RUXAILAB/pull/596">#596</a></td>
      <td>Fix layout overflow and incorrect margin</td>
    </tr>
    <tr>
      <td><a href="https://github.com/internetarchive/openlibrary/pull/10208">#10208</a></td>
      <td>Added yearly goal affordances to mobile view in my books page</td>
    </tr>
    <tr>
      <td rowspan="1"><strong>Stopwatch Project</strong></td>
      <td><a href="https://github.com/sumana-2705/Stopwatch">link</a></td>
      <td>A self-made project to learn textual framework</td>
    </tr>
  </table>
</blockquote>

## Project proposal
**Synopsis** <br/>
This project aims to enhance datashuttle, a Python-based tool for standardized data transfer in neuroscience, by adding support for **Google Drive** and **Amazon Web Services**. Currently, datashuttle facilitates data transfer via SSH or mounted drives; this extension will enable cloud storage integration using **RClone**. The project will implement new functionalities in both the Python API and TUI, ensuring efficient remote data access. Additionally, comprehensive testing and documentation will be provided to support users. This upgrade will significantly improve data accessibility and collaboration for researchers handling large-scale neuroscience datasets.
  
**Deliverables** <br/>
- Extend DataShuttle to support transfers between the local filesystem and cloud services like Google Drive and AWS using both the Python API and terminal interface.
- Write tests to the newly added transfer features.
- Provide clear and concise documentation.

**Stretch Goals** <br/>
- Add detailed logs and a progress bar to track file transfers.
- Address open issues in the repository adding new functionalities.

**Implementation Timeline** <br/>
- I have structured the project timeline based on a dedicated 30-hour workweek, allotting required time to the all the phase
<br/>
<table>
  <thead>
    <tr>
      <th>Timeline</th>
      <th>Deliverables</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Community Bonding Period</b><br>Mon 5/8 - Sun 6/1</td>
      <td>
        <ol type="1">
          <li>Familiarizing more with the community and clearing my doubts regarding the project, discussing expectations.</li>
          <li>Connecting with other contributors working with Neuroinformatics Unit.</li>
          <li>Review the existing codebase to gain a comprehensive understanding of the API-TUI interaction.</li>
          <li>Explore the process of integrating new functionalities into the Textual API and Terminal User Interface (TUI).</li>
          <li>Research and understand RClone’s architecture, supported cloud storage services, and file transfer mechanisms to aid in seamless integration.</li>
          <li>Analyze previously implemented data transfer methods, including SSH and mounted drives.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 1</b><br>Mon 6/2 - Sat 6/7</td>
      <td>
        <ol type="1">
          <li>Define the integration strategy for Google Drive support via <b>RClone</b>.</li>
          <li>Identify necessary modifications to both the Python API and the TUI for seamless integration.</li>
          <li>Create a design document outlining the approach, expected challenges, and success criteria.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 2</b><br>Mon 6/9 - Sat 6/14</td>
      <td>
        <ol type="1">
          <li>Begin coding the core functionality for data transfer between the local filesystem and Google Drive.</li>
          <li>Conduct basic functionality tests to ensure the integration is correctly functioning in both Python API and TUI.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 3</b><br>Mon 6/16 - Sat 6/21</td>
      <td>
        <ol type="1">
          <li>Develop comprehensive test cases covering various scenarios for Google Drive transfers.</li>
          <li>Execute tests and document any issues or failures.</li>
          <li>Start debugging and refining the code based on test outcomes.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 4</b><br>Mon 6/23 - Sat 6/28</td>
      <td>
        <ol type="1">
          <li>Write detailed documentation for the Google Drive integration, including setup instructions, API usage, and TUI operations.</li>
          <li>Ensure that the documentation covers both common use cases and edge scenarios.</li>
          <li>Feedback on the documentation from mentors ensure clarity.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 5</b><br>Mon 6/30 - Sat 7/5</td>
      <td>
        <ol type="1">
          <li>Enhance the user experience by refining the workflow and interactions within the TUI for Google Drive support.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 6</b><br>Mon 7/7 - Sat 7/12</td>
      <td>
        <ol type="1">
          <li>Address any leftover issues or bugs discovered during testing and user experience enhancements.</li>
          <li>Finalize and polish all deliverables in preparation for the midterm evaluation.</li>
          <li>Write a blog post summarizing the progress made so far</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 7</b><br>Mon 7/14 - Sat 7/19</td>
      <td>
        <ol type="1">
          <li>Define the integration strategy for AWS S3 bucket support using RClone.</li>
          <li>Identify necessary modifications in both the Python API and the TUI to accommodate AWS transfers.</li>
          <li>Create a design document outlining the implementation approach, expected challenges, and success criteria.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 8</b><br>Mon 7/21 - Sat 7/26</td>
      <td>
        <ol type="1">
          <li>Implement the core functionality for data transfer between the local filesystem and AWS S3 buckets.</li>
          <li>Conduct initial manual tests to verify basic file transfer operations.</li>
          <li>Ensure that AWS-specific configurations (e.g., authentication, bucket selection) are correctly handled in both API and TUI.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 9</b><br>Mon 7/28 - Sat 8/2</td>
      <td>
        <ol type="1">
          <li>Develop comprehensive test cases to validate AWS integration under different scenarios.</li>
          <li>Debug and refine the implementation based on test results.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 10</b><br>Mon 8/4 - Sat 8/9</td>
      <td>
        <ol type="1">
          <li>Write detailed documentation explaining the AWS integration, including API usage and TUI operations. Ensuring that documentation provides clear instructions on setting up AWS credentials and configuring RClone for seamless transfers.</li>
          <li>Include examples of common use cases and troubleshooting guidelines.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 11</b><br>Mon 8/11 - Sat 8/16</td>
      <td>
        <ol type="1">
          <li>Improve the user interface (UI) within the TUI to enhance usability and visual clarity for both functionalities.</li>
          <li>Optimize menu structures, error messages, and progress indicators for better user experience.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 12</b><br>Mon 8/18 - Sat 8/23</td>
      <td>
        <ol type="1">
          <li>Address any remaining issues or bugs discovered in the AWS integration.</li>
          <li>Conduct final integration tests for both Google Drive and AWS functionalities to ensure stability and reliability.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><b>Week 13</b><br>Mon 8/25 - Mon 9/1<br>(Final eval due 9/1)</td>
      <td>
        <ol type="1">
          <li>Discuss the final evaluation with the project mentor.</li>
          <li>Prepare a project report that shows the work done till week 12.</li>
          <li>Document all the progress made in my GSoC blog about GSoC’25 journey.</li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>

**Communication Plan** <br/>
I will communicate with my mentor through Zulip chat whenever needed. However, I feel that having a weekly stand-up meeting via video call would be beneficial for discussing the detailed plan for the week and identifying areas for further improvement. That said, I am completely open to any mode of communication based on my mentor’s availability and preference.
  
## Personal statement
- **Past experience** <br/>
  I have 3 years experience in Python language. I have been actively contributing to open-source projects from last 7 months, collaborating with organizations like Microsoft Recommenders, Aeon, Open Library, Flyte, Wagtail, Open Climate Fix, and more. One of my most memorable moments was receiving appreciation from the Microsoft Recommenders maintainer after my first PR was merged ([link](https://x.com/miguelgfierro/status/1808596073847357646)). So far, I have successfully merged more than [15 PRs](https://github.com/pulls?q=is%3Apr+author%3Asumana-2705+archived%3Afalse+is%3Aclosed) in these organisations and completed [Hacktoberfest 2024](https://holopin.io/@sumana2705). Additionally, I have completed the [Machine Learning Specialization](https://www.coursera.org/account/accomplishments/specialization/FRH15SYH6GVW) by Stanford University (Coursera), covering Supervised Learning, Advanced Learning Algorithms, and Unsupervised Learning.
  
- **Motivation: why this project?** <br/>
Ever since the GSoC organizations were announced, I had been searching for an organisation whose aim resonates with my thinking and experience. I found NIU's initiative to develop open-source software for neuroscience and machine learning truly unique, which motivated me to choose this project. As a Python programmer with a bit of frontend development knowledge, I never expected to find a project that combines both. But when I saw the Datashuttle TUI, I was amazed, this was the first time I had explored an application developed entirely for the terminal. While contributing, I faced some challenges as a beginner, but the project maintainers were incredibly helpful. Their support kept me engaged, and I became even more eager to learn about this technology.

- **Match: why you?** <br/>
I’ve contributed to various open-source projects purely out of curiosity and a passion for learning. One of my biggest strengths is discipline and taking ownership of the project. I would like to treat the project as my own, taking care of its execution, submission and future maintenance. My contributions reflect my dedication, curiosity to learn and compassion for my fellow contributors.To make more meaningful contributions, I have learnt basics of the Textual framework and developed an introductory [project using textual](https://github.com/sumana-2705/Stopwatch). It has helped me understand the codebase deeply and contribute more effectively. I love learning from experienced people and constantly pushing myself to grow which makes me unique from others for this project. This same mindset of discipline, ownership, and continuous learning has been a defining factor in my academic journey as well. I have prepared for and cleared JEE Advanced, one of the world's toughest exams with an acceptance rate of just **1% in 1.2 million students**, through self-study during the COVID lockdown. This achievement earned me a seat at IIT (BHU), one of India’s top-10 engineering institutions. It was a challenging journey, but my dedication and consistency over two years helped me succeed. I bring that same commitment, sincerity, and hard work to everything I do.

- **Availability** <br/>
  I do not have any other commitments during the program, I did not accept any Internship or other offers for the summer. I would be available for the whole program period. My University’s End Semester exams are scheduled from 25th April to 10th May, So I will be available for the whole program period. After this I will be having my Mid Semester Exams scheduled in September, that will also not take too much of my time due to less syllabus in Mid Sems. On an average, I will be available for 30 hours a week for the entire period (considering as a 175 hour project). I am ready to extend this whenever needed.

## GSoC
- **GSoC experience** <br/>
  I hope to gain hands-on experience in building Terminal User Interfaces and further improve my proficiency in Python programming. Additionally, I am eager to explore NIU's other projects beyond Datashuttle and learn more about innovative ideas like it. I also look forward to building a collaborative and professional relationship with the people at NIU and continuing my contributions even after the program ends.
  
- **Are you also applying to projects with other organisations in GSoC 2025?** <br/>
  No, I am not submitting proposal anywhere else other than datashuttle.
