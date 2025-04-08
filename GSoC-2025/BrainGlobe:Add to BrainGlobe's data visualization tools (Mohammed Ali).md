## BrainGlobe Atlas API - OpenMINDS SANDS Compatibility (Mohammed Ali Al Sakkaf)

## Personal details

- **Full name:** Mohammed Ali Al Sakkaf
    
- **Email:** [mohammed.binbasri@gmail.com](mailto:mohammed.binbasri@gmail.com)
    
- **GitHub username:** Binbasri-in
    
- **Zulip username:** mohammed.binbasri@gmail.com
    
- **Location & time-zone:** Yemen, IST (GMT+3:00)
    
- **Personal website / project portfolio:** [https://github.com/Binbasri-in](https://github.com/Binbasri-in)
    
- **Code contribution:** New Contributer looking to learn
    
- **Proposal discussion link:** New Contributer looking to learn
    

## Project proposal

- **Synopsis**
    
    This project aims to add support for the OpenMINDS SANDS standard to the BrainGlobe Atlas API, a Python tool used in neuroscience for accessing anatomical atlases. OpenMINDS SANDS is a semantically rich, JSON-LD-based format developed by the INCF to improve interoperability and metadata representation in neuroanatomy. The goal is to extend BrainGlobe's atlas packaging scripts to optionally output SANDS-compliant data, adapt at least one existing atlas workflow (e.g. Allen Mouse Brain Atlas), and update tests and documentation. This work will increase the utility of BrainGlobe tools and promote open, standards-driven neuroscience research.
    
    **Deliverables:**
    
    - Extension of the core Python packaging scripts in BrainGlobe to support optional OpenMINDS SANDS format output.
        
    - Mapping of existing BrainGlobe internal schema to OpenMINDS SANDS structure.
        
    - Packaging workflow adapted for at least one existing public atlas (e.g., Allen Mouse Brain Atlas).
        
    - JSON-LD files produced in compliance with the OpenMINDS SANDS schema, validated with community tools.
        
    - Extensive test coverage for schema validation, file creation, and consistency checks.
        
    - Contributor and user documentation including setup, packaging instructions, and OpenMINDS guidance.
        
    - A blog post or tutorial summarizing the project implementation, learnings, and how others can adopt the new functionality.
        
- **Implementation timeline**
    
    **Minimal set of deliverables:**
    
    - OpenMINDS SANDS format export integrated into packaging tools
        
    - One fully adapted atlas with compliant metadata outputs
        
    - Functional unit and integration tests
        
    - Validated JSON-LD output using external schema tools
        
    - Full contributor documentation
        
    - Public blog post/tutorial
        
    
    **Stretch goals:**
    
    - CLI flag or config toggle to switch between BrainGlobe and OpenMINDS modes
        
    - Multi-atlas packaging script structure to streamline standard adoption
        
    - Auto-validation utility integrated into the test suite
        
    
    **Weekly Timeline (estimated 18–22 hours/week):**
    
    |Week|Dates|Task|
    |---|---|---|
    |Community Bonding|Apr 8 – May 19|Study BrainGlobe API architecture, OpenMINDS SANDS spec; set up environment; select target atlas with mentors|
    |Week 1|May 20 – May 26|Implement export scaffolding for OpenMINDS SANDS with mock data|
    |Week 2|May 27 – Jun 2|Extend core packaging logic to optionally write OpenMINDS-compliant output|
    |Week 3|Jun 3 – Jun 9|Begin refactoring Allen Mouse Brain Atlas script to map its data to OpenMINDS SANDS schema|
    |Week 4|Jun 10 – Jun 16|Validate generated JSON-LD with schema checkers; resolve any structure mismatches|
    |Week 5|Jun 17 – Jun 23|Create automated tests: structural validation, field consistency, file I/O tests|
    |Week 6|Jun 24 – Jun 30|Finalize test coverage; prepare codebase for midterm check|
    |Week 7|Jul 1 – Jul 7|Midterm evaluation submission with working OpenMINDS atlas output|
    |Week 8|Jul 8 – Jul 14|Write usage documentation and contributor setup guide|
    |Week 9|Jul 15 – Jul 21|Refactor documentation; implement feedback from early testers and mentors|
    |Week 10|Jul 22 – Jul 28|Integrate functionality into CI pipeline for automated format validation|
    |Week 11|Jul 29 – Aug 4|Prepare final blog/tutorial; freeze functionality|
    |Week 12|Aug 5 – Aug 11|Conduct final QA and feedback cycle with mentors|
    |Final Week|Aug 12 – Aug 25|Submit PR to BrainGlobe, publish blog/tutorial, and finalize wrap-up|
    
- **Communication plan**
    
    I plan to communicate with my mentors weekly through scheduled video calls, and daily (or as needed) via Zulip chat. I will maintain a running log of progress and blockers and welcome async feedback on GitHub pull requests.
    

## Personal statement

- **Past experience**
    
    I am a Computer Science undergraduate at BMS Institute of Technology and Management, with strong interests in bioinformatics and open data standards. I've contributed to several open-source machine learning and backend projects on GitHub, including tools that interface with structured data formats like JSON and YAML. Previously, I worked on a DNA profiling project using labeled biological images, where I gained hands-on experience with image data processing.
    
- **Motivation: why this project?**
    
    I’m passionate about making neuroscience data more accessible and interoperable. BrainGlobe’s commitment to open standards aligns well with my interests, and OpenMINDS SANDS presents an exciting opportunity to make brain atlas data more structured and reusable across platforms. This project directly supports that mission.
    
- **Match: why you?**
    
    I bring a combination of Python expertise, familiarity with semantic data structures like JSON-LD, and a strong desire to contribute to bioinformatics and neuroscience tooling. My collaborative spirit and open-source experience make me a good fit for this project and community.
    
- **Availability**
    
    Other than minor coursework, I am fully available throughout the GSoC program. I have no vacations planned and can commit 18–22 hours weekly to the project.
    

## GSoC

- **GSoC experience**
    
    I hope to improve my technical, research, and collaboration skills while contributing meaningful code to the neuroscience open-source ecosystem. I look forward to mentorship and community feedback to help me grow as a contributor.
    
- **Are you also applying to projects with other organisations in GSoC 2025?**
    
    No, I am only applying to this project through BrainGlobe.
