# BrainGlobe: Updating Atlas API scrpits to Atlas API v2 - Packaging Script Modernization (Muqeet Salam)

# Personal Details

- **Full name:** Mohammed Muqeet Us Salam
- **Email:** muqeetsalam168@gmail.com
- **GitHub username:** Muqeet-Salam
- **Zulip username:** Muqeet Salam (User ID: 893310)
- **Location & time-zone:** India, IST
    

# Project Proposal 

## Synopsis

The MongoDB Atlas API v2 introduces several breaking changes over v1, including endpoint restructuring, updated authentication mechanisms, and enhanced resource representations. Currently, numerous open-source and internal packaging scripts depend on API v1 endpoints, which are now deprecated. This project aims to modernize those scripts by migrating them to API v2, improving reliability, security, and future compatibility.

The work will involve identifying v1 dependencies, replacing deprecated calls with v2 equivalents, adapting authentication to use digest or programmatic API keys, updating payloads, handling paginated responses, and ensuring complete test coverage. By the end of the project, all packaging scripts will be updated, documented, and backward-compatible where necessary.

This work is essential to ensure continued functionality of tools and pipelines built around Atlas API, and will reduce tech debt while encouraging the adoption of best practices across Atlas-integrated projects.
## Minimal Set of Deliverables
    
- Identify and catalog all v1 Atlas API dependencies across packaging scripts.
- Fully migrate all calls and auth methods to v2 equivalents.
- Handle pagination, error codes, rate limits as per v2 specs.
- Add tests (unit + integration) for all updated scripts.
- Write clear documentation and migration notes for users.
- Submit a blog post/tutorial explaining key changes and migration process.


## Weekly Timeline

  | Week                         | Tasks                                                                                                                                             |
  |------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
  | Week 0, (Jun 2 – Jun 6)      | Community bonding, codebase setup, review API docs, identify all v1 dependencies.|
  | Weeks 1-2 (Jun 9 - Jun 20)   | Migrate all basic GET/POST calls to v2. Refactor auth and headers. Add regression tests.      |
  | Weeks 3-4 (Jun 23 - Jul 4)   | Handle complex resources (e.g. clusters, networks). Begin backward compatibility logic.                                                                                        |
  | Week 5 (Jul 7 - Jul 11)      | Midterm submission. Validate all scripts against sandbox org. Start documentation.                            |
  | Week 6 (Jul 14 - Jul 18)     | Add pagination handling, retry logic, and default error messages for v2 flows.                                                                          |
  | Weeks 7-8 (Jul 21 - Aug 1)   | Test edge cases, permissions errors, and auth failures. Finalize compatibility layer.                                                               |
  | Week 9 (Aug 4 - Aug 7)       | Polish CLI UX, write blog/tutorial, mentor review, final submission.                                                      |

Time commitment: 40hr / week, Mon-Fri (except Week 9, which is Mon-Thu).

## Communication Plan

Weekly check-in video calls
Async communication via Zulip, GitHub, and email
Daily status updates (if needed during critical weeks)

# Personal Statement

## Past Experience - Why Me?

I have strong experience in full-stack development, especially with backend tools like FastAPI, Django, and SQLAlchemy. I’ve worked with both SQL and NoSQL databases, including MySQL and MongoDB, and I’ve built APIs and full web applications using React and other modern tools. I’m confident working with large codebases, writing clean and reusable code, and creating useful features that are easy to test and maintain.
What really makes me interested in this project is my personal interest in brain data and MRI scan images. I’ve spent time learning how to work with MRI datasets and thinking about how to analyse and improve brain image processing using AI/ML tools. The BrainGlobe tools are exciting to me because they combine neuroscience with real software problems — and that’s exactly where I want to contribute.
This project is a great match for both my skills and my interests. I’m confident I can help update the code to use Atlas API v2, improve documentation, and make sure everything works smoothly for users. I care about building tools that help researchers, and I’m excited to be part of something that supports open science.

## Motivation: Why This Project?

Atlas is the backbone of many cloud-native database systems, and ensuring tools stay aligned with its latest APIs is crucial. This project has a direct and measurable impact—not only will it ensure smooth functioning of critical pipelines, but it will also serve as a template for similar migrations in the future. I’m excited about working closely with maintainers, learning from real-world DevOps pain points, and contributing to a cleaner, more future-ready codebase.


## Availability

Available full-time (Mon–Fri, 40 hours/week) throughout the summer. I will communicate any planned time off in advance.

## GSoC Experience

GSoC represents a unique opportunity for me to contribute to meaningful backend/tooling infrastructure in open-source. I’m especially interested in the real-world application of DevOps, API design, and system migrations, and this project is a perfect match for my interests and skills.


## Are you also applying to projects with other organisations in GSoC 2025?

No.
