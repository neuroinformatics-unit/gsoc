Project title
niuvlsi-Neuromorphic VLSI Design for Edge AI ()
Personal details
•	Full name: Prashanth Basutkar
•	Email: buv.prashanth@gmail.com
•	GitHub username: reva2498
•	Zulip username: https://reva2498.zulipchat.com/
•	Location & time-zone: Bengaluru, India, & Kolkata
•	Personal website / project portfolio: (optional)
•	Code contribution: 
•	Proposal discussion link: 
Project proposal
•	Synopsis
Neuromorphic computing emulates the neural architecture of the human brain to enable low-power, event-driven computation. This project focuses on the design and development of a neuromorphic VLSI system optimized for Edge AI applications. It will implement a simple spiking neural network (SNN) architecture using CMOS-compatible analog/digital circuitry to process real-time data with ultra-low power consumption. The aim is to deliver a functional prototype (e.g., on FPGA or simulated ASIC) for applications such as gesture recognition, environmental monitoring, or low-power IoT devices. The open-source community will benefit from accessible hardware designs and SNN models deployable in constrained edge environments.
•	Implementation timeline
Minimal Deliverables
•	SNN model selection and simulation in software
•	VLSI architecture for neuron and synapse circuits
•	RTL/analog design and simulation (Verilog/SystemVerilog + Cadence tools)
•	FPGA-based prototype or analog simulation results
•	Documentation and tutorials
Stretch Goals
•	Hardware-software co-design interface (e.g., SPI/I2C)
•	Benchmarking vs. conventional architectures
•	Support for online learning (STDP or similar)
Weekly Timeline
Week	Hours/week	Tasks
Pre-GSoC	10	Study neuromorphic systems, finalize SNN model, set up environment
Week 1	20	Model SNN in Brian2/Nengo, begin testing simple network behaviour
Week 2	20	Develop VLSI neuron/synapse schematic, simulate individual cells
Week 3	20	Integrate neuron blocks, start Verilog RTL design of SNN core
Week 4	20	Run post-synthesis simulation and area/power analysis
Week 5	20	Prepare design for FPGA (Vivado or similar) or analog backend flow
Week 6	20	Mid-term evaluation: Basic SNN working on hardware/simulator
Week 7	20	Implement learning mechanism (e.g., STDP if feasible)
Week 8	20	Interface with edge sensors or dummy input
Week 9	20	Optimization and power profiling
Week 10	20	Add stretch goals (interface, benchmarks) if time allows
Week 11	20	Finalize documentation, tutorial, hardware diagram
Week 12	20	Code freeze, submit project, make final presentation


Communication plan
Weekly sync-ups with the mentor via video call, plus asynchronous updates through Zulip or Discord. Daily or alternate-day updates via chat for blockers. GitHub issues and milestones to track progress.
Personal statement
•	Past experience I have hands-on experience with Verilog, digital IC design flows, and basic analog CMOS circuits through academic projects. I've used FPGA boards (e.g., Xilinx Spartan/Artix) and am familiar with ML frameworks such as PyTorch and TensorFlow. I’ve also contributed to open-source repositories related to AI models and RTL cores.
•	Motivation: why this project? I’m deeply fascinated by bio-inspired computing. Neuromorphic systems are the next frontier for low-power, intelligent hardware, and this project is a rare opportunity to contribute to that domain while blending my interests in AI and chip design.
•	Match: why you? I bring a unique blend of skills: circuit design, FPGA prototyping, and AI modelling. My previous work with low-power RTL design and passion for neuroscience-inspired computing makes me a strong candidate.
•	Availability I have no full-time work during GSoC. I may have some minor academic commitments, but I can allocate 18–20 hours per week consistently for the duration.
GSoC
•	GSoC experience I expect to gain mentorship, real-world open-source development experience, and deeper insights into neuromorphic hardware design. I also hope to contribute long-term to the project after GSoC.
•	Are you also applying to projects with other organisations in GSoC 2025? No, this is my only application, and my top priority.
