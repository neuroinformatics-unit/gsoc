## BrainGlobe:Add to BrainGlobe's data visualization tools (Kirato Yoshihara)

## Personal

- **Full name**: Kirato Yoshihara
- **Email**: kiratoyoshihara@gmail.com
- **GitHub username**: kira1228
- **Zulip username**: kirato yoshihara
- **Location & time-zone**: Osaka, Japan, GMT+9:00
- **Personal website / project portfolio**: <a href="https://github.com/kira1228">https://github.com/kira1228</a>
- **Proposal discussion link**: <a href="https://github.com/neuroinformatics-unit/gsoc/pull/18">https://github.com/neuroinformatics-unit/gsoc/pull/18</a>
- **Code contribution**
<blockquote>
    <table>
        <tr>
            <td rowspan="5"><strong>brainrender-napari PRs</strong></td>
            <td><a href="https://github.com/brainglobe/brainrender-napari/pull/175">#175</a></td>
            <td>Color rows of atlas manager widget</td>
        </tr>
        <tr>
            <td><a href="https://github.com/brainglobe/brainrender-napari/pull/183">#183</a></td>
            <td>Changed color scheme</td>
        </tr>
        <tr>
            <td><a href="https://github.com/brainglobe/brainrender-napari/pull/180">#180</a></td>
            <td>Add some kind of indicator to show that data is being downloaded or updated
</td>
        </tr>
        <tr>
            <td><a href="https://github.com/brainglobe/brainrender-napari/pull/176">#176</a></td>
            <td>Add popup warning for 2D mesh display</td>
        </tr>
        <tr>
            <td><a href="https://github.com/brainglobe/brainrender-napari/pull/192">#192</a></td>
            <td>Simplify multi-threading around progressbar</td>
        </tr>
        <tr>
            <td rowspan="1"><strong>brainglobe-atlasAPI PR</strong></td>
            <td><a href="https://github.com/brainglobe/brainglobe-atlasapi/pull/519">#519</td>
            <td>Add fn_update as an optional argument</td>
        </tr>
    </table>
</blockquote>

## Project proposal

- **Synopsis**

  This project aims to extend the powerful visualization capabilities of brainrender by integrating it with the widely-used napari image viewer. The goal is to make atlas-registered brain data visualization accessible to users without programming expertise. This is important because it democratizes access to advanced neuroimaging tools, fostering broader collaboration and enhancing data reproducibility in the open source community. The deliverables include the napari widget implementation, comprehensive tests for the new functionality, and detailed documentation, all of which will empower researchers and enthusiasts to leverage high-quality brain data more efficiently.

- **Implementation**

  A bullet point list with **minimal set of deliverables**:

  - A Python implementation of a napari widget that allows users to download and visualize atlas-registered data.
  - Tests to cover any added functionality.
  - Documentation for the new functionality.
  - Preparation of mid-term and final reports.

- **Implementation timeline**

<table>
  <thead>
    <tr>
      <th>Timeline</th>
      <th>Deliverables</th>
      <th>Hours</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Community Bonding Period</b><br>Mon 5/8 - Sun 6/1</td>
      <td>
        <ol type="1">
          <li>Discuss project details with mentor and understand the codebase</li>
          <li>Study the <a href="https://elifesciences.org/articles/65751" target=_blank>paper</a> on atlas-registered data and visualization methods</li>
          <li>Set up the development environment and resolve dependencies</li>
          <li>Initial exploration of brainglobe-data-api requirements (ref: <a href="https://github.com/brainglobe/BrainGlobe/issues/77">brainglobe/BrainGlobe#77</a>)</li>
          <li>Familiarize with existing data resources (BrainTrawler, etc.)</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 1</b><br>Mon 6/2 - Sun 6/8<br><i>(Exam period)</i></td>
      <td>
        <ol type="1">
          <li>Create technical specifications document for the widget</li>
        </ol>
      </td>
      <td>5</td>
    </tr>
    <tr>
      <td><b>Week 2</b><br>Mon 6/9 - Sun 6/15</td>
      <td>
        <ol type="1">
          <li>Design and initial planning for brainglobe-data-api architecture</li>
          <li>Define data sources and API interfaces</li>
          <li>Create project structure for brainglobe-data-api</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 3</b><br>Mon 6/16 - Sun 6/22</td>
      <td>
        <ol type="1">
          <li>Implement core data fetching components for brainglobe-data-api</li>
          <li>Develop data structure definitions</li>
          <li>Implement API endpoints for basic data retrieval</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 4</b><br>Mon 6/23 - Sun 6/29</td>
      <td>
        <ol type="1">
          <li>Implement caching system for brainglobe-data-api</li>
          <li>Develop configuration management for data sources</li>
          <li>Add error handling and logging</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 5</b><br>Mon 6/30 - Sun 7/6</td>
      <td>
        <ol type="1">
          <li>Integrate brainglobe-data-api with atlasapi</li>
          <li>Implement data validation and preprocessing</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 6</b><br>Mon 7/7 - Sun 7/13<br><i>(Exam Prep Period)</i></td>
      <td>
        <ol type="1">
          <li>Review implementation progress</li>
          <li>Documentation planning for brainglobe-data-api</li>
        </ol>
      </td>
      <td>5</td>
    </tr>
    <tr>
      <td><b>Week 7</b><br>Mon 7/14 - Sun 7/20<br><i>(Exam Prep Period)</i></td>
      <td>
        <ol type="1">
          <li>Bug fixes and minor improvements</li>
          <li>Prepare integration plan for napari widget</li>
        </ol>
      </td>
      <td>5</td>
    </tr>
    <tr>
      <td><b>Week 8</b><br>Mon 7/21 - Sun 7/27<br><i>(Exam Prep Period)</i></td>
      <td>
        <ol type="1">
          <li>Create mid-term project report</li>
        </ol>
      </td>
      <td>5</td>
    </tr>
    <tr>
      <td><b>Week 9</b><br>Mon 7/28 - Sun 8/3<br><i>(Exam Period)</i></td>
      <td>
        <ol type="1">
          <li>Fix identified issues</li>
          <li>Prepare for post-exam implementation phase</li>
        </ol>
      </td>
      <td>5</td>
    </tr>
    <tr>
      <td><b>Week 10</b><br>Mon 8/4 - Sun 8/10<br><i>(Post-Exam)</i></td>
      <td>
        <ol type="1">
          <li>Begin napari widget implementation</li>
          <li>Integrate widget with brainglobe-data-api</li>
          <li>Implement basic widget functionality</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 11</b><br>Mon 8/11 - Sun 8/17<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Continue basic widget functionality implementation</li>
          <li>Design detailed widget UI components</li>
          <li>Implement data source selection interface</li>
        </ol>
      </td>
      <td>40</td>
    </tr>
    <tr>
      <td><b>Week 12</b><br>Mon 8/18 - Sun 8/24<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Complete widget UI implementation</li>
          <li>Implement query interface for different data types</li>
          <li>Add data visualization components
          </li>
        </ol>
      </td>
      <td>40</td>
    </tr>
    <tr>
      <td><b>Week 13</b><br>Mon 8/25 - Sun 9/1<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Add data visualization components</li>
          <li>Implement results display interface</li>
          <li>Integrate visualization with napari layers</li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 14</b><br>Mon 9/2 - Sun 9/8<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Complete implementation of remaining planned features</li>
          <li><b>CODE FREEZE at end of week</b></li>
        </ol>
      </td>
      <td>35</td>
    </tr>
    <tr>
      <td><b>Week 15</b><br>Mon 9/9 - Sun 9/15<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Conduct comprehensive testing</li>
          <li>Implement integration tests</li>
          <li>Fix identified issues</li>
          <li>Begin user documentation</li>
        </ol>
      </td>
      <td>30</td>
    </tr>
    <tr>
      <td><b>Week 16 (Last Week)</b><br>Mon 9/16 - Sun 9/22<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Complete user documentation</li>
          <li>Prepare final demonstration</li>
          <li>Discuss the final evaluation with my mentor</li>
          <li>Reflect on and summarize the tasks I have completed so far</li>
        </ol>
      </td>
      <td>25</td>
    </tr>
    <tr>
      <td><b>Stretch Goals (If time allows)</b></td>
      <td>
        <ol type="1">
          <li>Advanced Visualization Options: Settings for custom camera positions, background colors, etc.</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
  </tbody>
</table>

- **Communication plan**

  For general discussions with my mentor, I'm planning to communicate via applications like Zulip or Slack, and for technical questions, through GitHub pull requests. Additionally, it would be helpful to have weekly video calls to report on progress and receive feedback for improvements.

## Personal statement

- **Past experience.**

  I am currently conducting research at the Graduate School of Medicine at Osaka University, where my work focuses on using Diffusion Models to visualize human brain imagery. This research has given me valuable experience in neuroimaging techniques and data visualization. In addition, I have honed my Python skills in real-world settings through positions at two AI startups, where I developed image recognition models and built RAG systems. My technical expertise extends to finance, demonstrated during my summer internship at Goldman Sachs where I developed an AI model for FX trading. Throughout these experiences, I've continuously refined my skills in Python programming, data visualization, and machine learning - a combination particularly relevant to creating effective neuroimaging visualization tools. These diverse yet complementary experiences have equipped me with the technical capabilities and domain knowledge needed to successfully implement the brainrender-napari integration.

- **Motivation: why this project?**

  My research on visualizing human brain imagery through Diffusion models is deeply intertwined with neuroscience, requiring advanced visualization techniques in Python. This project represents a perfect alignment with both my technical skills and research interests. The potential impact of this open-source tool particularly motivates me - by making atlas visualization more accessible to researchers without extensive programming expertise, we can democratize access to sophisticated neuroimaging tools. This accessibility will accelerate neuroscience research by lowering technical barriers and enabling more scientists to effectively visualize and analyze brain data.

- **Match: why you?**

  I am uniquely qualified for this project as evidenced by my multiple contributions to brainrender-napari, where I've successfully submitted several feature enhancement PRs. This demonstrates my ability to properly implement, test, and document code within this specific ecosystem. My experience with the project also ensures I can effectively communicate with mentors and understand the development workflow. Additionally, my background includes Python-focused internships where I gained valuable experience working on real-world projects with practical constraints and timelines. This combination of project-specific contributions and broader development experience gives me strong confidence in my ability to successfully complete this project and deliver high-quality results that benefit the community.

- **Availability**

  I am currently working as an RA in a graduate research lab, which requires about 5 hours per week. On days when I have classes, I can dedicate around 20–25 hours per week to this project. However, during midterm and final exam periods, I expect to spend only about 5 hours per week on the project. I plan to make up for this by committing 30–40 hours per week during the summer break.

## GSoC

- **GSoC experience**

  I aim to enhance my image processing experience and programming skills through real-world software development on this project. Additionally, by collaborating with global researchers and engineers, I hope to build the foundation for a successful international career.

- **Are you also applying to projects with other organisations in GSoC 2025?**

  No, I'm submitting my proposal only to this organization.
