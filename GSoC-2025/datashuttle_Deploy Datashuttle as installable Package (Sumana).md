# datashuttle: Deploy Datashuttle as installable Package
## Personal Details
- **Full Name:** Angajala Sumana Sree
- **Preferred Name:** Sumana
- **Email:** sumanasree2705@gmail.com
- **Github Username:** sumana-2705
- **Zulip Username:** Sumana Sree
- **Location & time-zone:** Anantapur, India (GMT+5:30)
- **Portfolio Website:** https://sumana-2705.github.io/Sumana-Portfolio/
- **Proposal discussion link:** 
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
      <td rowspan="3"><strong>PRs related to Python</strong></td>
      <td><a href="https://github.com/aeon-toolkit/aeon/pull/2419">#2419</a></td>
      <td>Add LITETimeClassifier Example to Classification Notebook</td>
    </tr>
    <tr>
      <td><a href="https://github.com/flyteorg/flytesnacks/pull/1739">#1739</a></td>
      <td>Added examples for tensorflow types in Datatypes and IO section</td>
    </tr>
    <tr>
      <td><a href="https://github.com/wagtail/wagtail/pull/12387">#12387</a></td>
      <td>Updated can_handle method to check for AbstractGroupApprovalTask in mail.py</td>
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
Datashuttle is a tool that helps users easily transfer and organize data between local and remote systems. It supports the open-source community by making data management simpler, improving collaboration, and ensuring research is more reproducible. The goal of this project is to make datashuttle easily installable as a cross-platform executable, removing its dependency on Conda. Currently, users need technical expertise to set it up, limiting accessibility. By packaging tools like PyInstaller, Briefcase, Nuitka, etc., this project will create an easy-to-install executable for Windows, macOS, and Linux while ensuring smooth Textual UI rendering in native terminals. Additionally, the project will automate deployment using GitHub CI/CD and provide documentation. This will enhance usability, increase adoption, and make datashuttle more accessible to non-technical users.
  
**Deliverables** <br/>
- Make datashuttle easy to install without requiring Conda, allowing users to set it up with a graphical installer (alongside a CLI based option).
- Ensure smooth functionality across Windows, macOS, and Linux terminals without display issues.
- Automate updates and improvements using GitHub CI/CD for seamless maintenance.

**Stretch Goals** <br/>
- Build a web-based interface using [Textual-web](https://github.com/Textualize/textual-web) to run datashuttle in a browser.
- Test the web interface to ensure it integrates well with datashuttle's core features.

**Implementation Timeline** <br/>
<table>
  <thead>
    <tr>
      <th>Timeline</th>
      <th>Deliverables</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Community Bonding Period</strong><br>Mon 5/8 - Sun 6/1</td>
      <td>
        <ul>
          <li>Familiarizing more with the community and clearing my doubts regarding the project.</li>
          <li>Research packaging tools: PyInstaller, Briefcase, Nuitka, etc.</li>
          <li>Set up basic cross-platform environment on local and cloud and discuss CI/CD strategies.</li>
          <li>Document tool compatibility (macOS notarization, Windows signing, Linux dependencies).</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Week (1 &amp; 2)</strong><br>Mon 6/2 - Sat 6/14</td>
      <td>
        <ul>
          <li>Finalize packaging tool(s) for each platform based on tests.</li>
          <li>Test local builds for Windows, macOS, and Linux using shortlisted tools.</li>
          <li>Create platform-specific configuration files and test minimal reproducible builds.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Week (3 &amp; 4)</strong><br>Mon 6/16 - Sat 6/28</td>
      <td>
        <ul>
          <li>Set up GitHub Actions workflow to build binaries on push and tags.</li>
          <li>Use Windows, macOS, and Linux runners for platform-specific builds.</li>
          <li>Automate artifact upload for each build (to GitHub Releases or artifacts tab).</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Week (5 &amp; 6)</strong><br>Mon 6/30 - Sat 7/12</td>
      <td>
        <ul>
          <li>Package standalone installers.</li>
          <li>Begin testing installer usability and OS integration.</li>
          <li>Begin user-friendly documentation (installation instructions).</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Week (7 &amp; 8)</strong><br>Mon 7/14 - Sat 7/26</td>
      <td>
        <ul>
          <li>Optimize bundled builds by removing unnecessary files from builds.</li>
          <li>Ensure fonts/assets used by TUI are bundled correctly.</li>
          <li>Explore optional compression (UPX, etc.) to reduce binary size.</li>
          <li>Improve error reporting/logging when users run the packaged app.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Week (9 &amp; 10)</strong><br>Mon 7/28 - Sat 8/9</td>
      <td>
        <ul>
          <li>Run testing on target OS versions (Windows 10+, Ubuntu LTS, macOS).</li>
          <li>Fix platform-specific issues (e.g., terminal size bugs, color rendering, fonts).</li>
          <li>Integrate basic crash/error feedback mechanism (e.g., logs or messages).</li>
          <li>Add versioning and changelogs in builds.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><strong>Week (11 &amp; 12)</strong><br>Mon 8/11 - Sat 8/23</td>
      <td>
        <ul>
          <li>Finalize all documentation including local build instructions, CI/CD process, installation and usage instructions.</li>
          <li>Develop a graphical installer (alongside a CLI based option) to help users locate and install the packaged files across platforms</li>
          <li>Prepare and publish a final GitHub Release.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Communication Plan** <br/>
I will communicate with my mentor through Zulip chat whenever needed. However, I feel that having a weekly stand-up meeting via video call would be beneficial for discussing the detailed plan for the week and identifying areas for further improvement. That said, I am completely open to any mode of communication based on my mentor’s availability and preference.
  
## Personal statement
- **Past experience** <br/>
  I have 3 years experience in Python language. Currently I am a research student in [Sculpt lab](https://www.sculptlab.in/team),  with a team we are analyzing crime patterns at a micro level in Hyderabad (a metropolitan city) by studying the built environment and telecom data using Machine learning techniques. I have been actively contributing to open-source projects for the last 7 months, collaborating with organizations like Microsoft Recommenders, Aeon, Open Library, Flyte, Wagtail, Open Climate Fix, and more. So far, I have successfully merged more than [15 PRs](https://github.com/pulls?q=is%3Apr+author%3Asumana-2705+archived%3Afalse+is%3Aclosed) in these organisations and completed [Hacktoberfest 2024](https://holopin.io/@sumana2705). Additionally, I have completed the [Machine Learning Specialization](https://www.coursera.org/account/accomplishments/specialization/FRH15SYH6GVW) by Stanford University (Coursera), covering Supervised Learning, Advanced Learning Algorithms, and Unsupervised Learning.
  
- **Motivation: why this project?** <br/>
Ever since the GSoC organizations were announced, I had been searching for an organisation whose aim resonates with my thinking and experience. I found NIU's initiative to develop open-source software for neuroscience and machine learning truly unique, which motivated me to choose this project. As a Python programmer with a bit of frontend development knowledge, I never expected to find a project that combines both. But when I saw the Datashuttle TUI, I was amazed, this was the first time I had explored an application developed entirely for the terminal. While contributing, I faced some challenges as a beginner, but the project maintainers were incredibly helpful. Their support kept me engaged, and I became even more eager to learn about this technology and strongly want to work with the Datashuttle community.

- **Match: why you?** <br/>
I’ve contributed to various open-source projects purely out of curiosity and a passion for learning. One of my biggest strengths is discipline and taking ownership of the project. I would like to treat the project as my own, taking care of its execution, submission and future maintenance. My contributions reflect my dedication, curiosity to learn and compassion for my fellow contributors.To make more meaningful contributions, I have learnt basics of the Textual framework and developed an introductory [project using textual](https://github.com/sumana-2705/Stopwatch). It has helped me understand the codebase deeply and contribute more effectively. I love learning from experienced people and constantly pushing myself to grow which makes me unique from others for this project. This same mindset of discipline, ownership, and continuous learning has been a defining factor in my academic journey as well. I have prepared for and cleared JEE Advanced, one of the world's toughest exams with an acceptance rate of just **1% among 1.2 million students**, through self-study during the COVID lockdown. This achievement earned me a seat at IIT (BHU), one of India’s top-10 engineering institutions. It was a challenging journey, but my dedication and consistency over two years helped me succeed. I bring that same commitment, sincerity, and hard work to everything I do.

- **Availability** <br/>
  I do not have any other commitments during the program. My University’s End Semester exams are scheduled from 25th April to 10th May, So I will be available for the whole program period. After this I will be having my Mid Semester Exams scheduled in September (dates not yet announced), that will also not take too much of my time due to less syllabus in Mid Sems. On an average, I will be available for **40 hours a week** considering as a Large project(350 hours) for the entire period. I am ready to extend this whenever needed.
  
## GSoC
- **GSoC experience** <br/>
  I hope to gain hands-on experience in packaging Terminal User Interfaces and further improve my proficiency in Python programming. Additionally, I am eager to explore NIU's other projects beyond Datashuttle and learn more about innovative ideas like it. I also look forward to building a collaborative and professional relationship with the people at NIU and continuing my contributions even after the program ends.
  
- **Are you also applying to projects with other organisations in GSoC 2025?** <br/>
  No, I am not submitting proposals anywhere else other than datashuttle.
