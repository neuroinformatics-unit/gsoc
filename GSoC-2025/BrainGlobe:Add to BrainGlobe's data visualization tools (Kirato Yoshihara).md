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

This project integrates brainrender with the napari image viewer to enable atlas-registered brain data visualization for non-programmers. By combining these tools, it democratizes advanced neuroimaging capabilities, fostering collaboration and enhancing reproducibility in open source research.

- **Minimal set of deliverables**

  - A Python implementation of a napari widget that allows users to download and visualize atlas-registered data.
  - Tests and documentation to cover any added functionality.

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
      <td><b>Community Bonding</b><br>Mon 5/8 - Sun 6/1</td>
      <td>
        <ol type="1">
          <li>Discuss project details with mentor and understand codebase</li>
          <li>Study the <a href="https://elifesciences.org/articles/65751" target=_blank>paper</a> and focus on atlas-registered data and visualization methods</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 1</b><br>Mon 6/2 - Sun 6/8<br><i>(Exam)</i></td>
      <td>
        <ol type="1">
          <li>Create technical specifications document for widget</li>
        </ol>
      </td>
      <td>5</td>
    </tr>
    <tr>
      <td><b>Week 2 ~ 5</b><br>Mon 6/9 - Sun 7/6</td>
      <td>
        <ol type="1">
          <li>Define interfaces focusing on streamlines data</li>
          <li>Implement core data fetching for projection streamlines and basic retrieval API</li>
          <li>Develop configuration for projection data sources</li>                    
        </ol>
      </td>
      <td>80</td>
    </tr>
    <tr>
      <td><b>Week 6 ~ 9</b><br>Mon 7/7 - Sun 8/3<br><i>(Exam weeks)</i></td>
      <td>
        <ol type="1">
          <li>Review implementation progress</li>
          <li>Prepare napari widget integration plan</li>
          <li>Create mid-term project report</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
      <td><b>Week 10</b><br>Mon 8/4 - Sun 8/10</td>
      <td>
        <ol type="1">
          <li>Integrate napari widget with brainglobe-data-api</li>
          <li>Create UI for streamlines data selection</li>
        </ol>
      </td>
      <td>20</td>
    </tr>
    <tr>
    <td><b>Week 11 ~ 14</b><br>Mon 8/11 - Sun 9/8<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Develop streamlines data query interface</li>
          <li>Complete streamlines visualization components</li>
          <li>Integrate visualization with napari layers and implement results display for connection data</li>
          <li>Implement single neuron morphology and gene expression visualization</li>             
        </ol>
      </td>
      <td>150</td>
    </tr>
    <tr>
      <td><b>Week 15 ~ 16</b><br>Mon 9/9 - Sun 9/22<br><i>(Summer break)</i></td>
      <td>
        <ol type="1">
          <li>Conduct comprehensive testing</li>
          <li>Complete user documentation and prepare for the final evaluation</li>          
        </ol>
      </td>
      <td>55</td>
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

  I'll communicate with my mentor via Zulip or Slack for general discussions and use GitHub PR for technical questions. I would appreciate having weekly video calls for progress updates and feedback.

## Personal statement

- **Past experience.**

  I am conducting research at Osaka University, focusing on Diffusion Models for visualizing human brain imagery. This work has provided valuable neuroimaging and data visualization experience. I also refined my Python skills at two AI startups, developing image recognition models and building RAG systems, and at Goldman Sachs, where I created an AI model for FX trading. These experiences combine to give me the technical and domain knowledge needed for successfully implementing the brainrender-napari integration.

- **Motivation: why this project?**

  I’m motivated by the opportunity to combine my Diffusion model–based brain imaging research with advanced Python visualization techniques. This open-source tool will lower technical barriers and make neuroimaging more accessible, accelerating neuroscience research by enabling more scientists to visualize and analyze brain data effectively.

- **Match: why you?**

  I bring specialized experience from my feature enhancement PRs to brainrender-napari, demonstrating my ability to implement, test, and document code within this ecosystem. My background in Python-focused internships further honed my real-world development skills. Together, these experiences give me confidence in delivering high-quality results for this project and its community.

- **Availability**

  I am currently working as an RA in a graduate research lab, which requires about 5 hours per week. On days when I have classes, I can dedicate around 20–25 hours per week to this project. However, during midterm and final exam periods, I expect to spend only about 5 hours per week on the project. I plan to make up for this by committing 30–40 hours per week during the summer break.

## GSoC

- **GSoC experience**

  I aim to enhance my image processing experience and programming skills through real-world software development on this project. Additionally, by collaborating with global researchers and engineers, I hope to build the foundation for a successful international career.

- **Are you also applying to projects with other organisations in GSoC 2025?**

  No, I'm submitting my proposal only to this organization.
