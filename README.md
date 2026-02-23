# **Bio-Aware Blended Spaces (BABS)**

*A student-led Meta-Project developed collaboratively within the Center for Holistic Integration (CHI)*

## **Overview**

**Bio-Aware Blended Spaces (BABS)** is an interdisciplinary research and
engineering initiative designed to explore how **biosensory data** can
be transformed into **responsive, immersive environments** through
defined **mediation pathways**. Built upon the **Balanced Blended Space
(BBS)** framework and implemented within the **Blended Reality
Performance System (BRPS)** architecture, BABS connects **human
physiological expression** and **computational responsiveness** in
shared physical--virtual spaces.

The project demonstrates how **cognitive agents (humans)** and
**computational agents (AI systems)** can **co-experience and co-shape**
an environment symmetrically---transforming biosignals such as heart
rate, EEG, or movement into audiovisual or kinetic responses. Each
transformation forms a distinct mediation pathway that can be studied,
documented, and extended.

[The full initial proposal can be found here](https://github.com/CHI-CityTech/BABS/blob/main/proposals/Bio-Aware%20Blended%20Spaces%20full%20proposal.md)  
  
Check in the proposals folder ot this repository for current, future, and speculative opportunities.  More specifically:  
[Potential research project areas](https://github.com/CHI-CityTech/BABS/blob/main/proposals/babs_potential_research_projects.md)

### **Repository Scope**
This repository contains public research materials, conceptual documentation, and academic prototypes related to the BABS meta-project.
## **Goals**

1.  Develop mediation pathways that translate biosignals into
    audiovisual, tactile, and environmental outputs.
2.  Establish bio-aware blended systems that function symmetrically
    between human and AI participants.
3.  Prototype the integration of physical, virtual, and conceptual
    elements through BRPS.
4.  Create an open framework for future research, art, and educational
    applications within CHI.

## **Project Phases**

| Phase | Focus | Description |
|-------|-------|-------------|
| **1** | Core Prototype | Establishes the baseline system: single or small set of biosensors → data normalization → audiovisual mediation. |
| **2** | Recursive Feedback | Introduces AI interpretation and feedback, enabling adaptive or emergent behavior. |
| **3** | Full Deployment | Integrates robotics, spatialized sound, and projection systems within the BRPS environment. |
| **4** | Applied Extensions | Expands applications to performance, therapy, education, and distributed collaboration. |

## **System Architecture (Simplified Mediation Pathways)**

**Cognitive Agent (Human)** → *(biosignal acquisition via sensors)* →
**Mediation Pathway 1: Capture Layer** → *(LSL/OSC normalization)* →
**Mediation Pathway 2: Data Layer** → *(Max/MSP + Jitter mapping)* →
**Mediation Pathway 3: Transformative Layer (Audio/Visual/Physical
Output)** → *(feedback)* → **Cognitive Agent**.

**Computational Agent (AI)** → *(receives normalized biosignal data)* →
**Mediation Pathway 4: Interpretation Layer (Machine Learning)** →
*(modifies system state)* → **Mediation Pathway 5: Recursive Feedback
Layer** → *(co-informs human and AI state)* → **Blended Environment**.

## **Technology Stack**

-   **Sensors:** OpenBCI, Muse, Empatica E4, Polar H10, Apple Watch,
    Fitbit, and camera-based biosensing.\
-   **Middleware:** Lab Streaming Layer (LSL), Open Sound Control (OSC),
    Bluetooth Low Energy (BLE), MQTT.\
-   **Software:** Max/MSP + Jitter, TouchDesigner, Ableton Live,
    Unity/Unreal (projection mapping).\
-   **Environment:** BRPS immersive projection, multichannel audio,
    robotic or kinetic interfaces.

## **Repository Structure**

    /BABS
    │
    ├── /docs                      # Research papers, proposals, phase overviews, BBS mediation pathway diagrams
    │   ├── /meta                  # Meta-project structure, theoretical framing, BBS/BPRS alignment
    │   └── /workflows             # Lab workflows, sprint plans, contribution guidelines
    │
    ├── /phase1_prototype          # Stage 1 MVP code & materials
    │   ├── /max_patches           # Max/MSP + Jitter patches for biosignal mapping
    │   ├── /projections           # Visual materials for projection sandbox
    │   ├── /audio                 # Sound patches, test tones, spatial prototypes
    │   └── /middleware_tests      # LSL/OSC/BLE connectivity demos
    │
    ├── /hardware                  # Sensor configuration & calibration
    │   ├── /wearables             # Apple Watch, Fitbit, Oura documentation & scripts
    │   ├── /research_sensors      # OpenBCI, Muse, Empatica, Polar
    │   ├── /primitive_sensors     # Contact mics, piezos, mats
    │   └── /camera_biosensing     # RGB/depth camera scripts & posture/respiration extraction
    │
    ├── /software                  # Scripts, utilities, and data-handling tools
    │   ├── /lsl                   # Lab Streaming Layer setup & stream definitions
    │   ├── /osc                   # OSC utilities, routing tables, bridge scripts
    │   ├── /ble                   # Bluetooth Low Energy helpers
    │   └── /ai_models             # Early ML classifiers (Phase 2+)
    │
    ├── /assets                    # Visual, audio, kinetic media used across phases
    │   ├── /textures              # Gradients, noise fields, visualizers
    │   ├── /video_loops           # Projection loops & motion overlays
    │   └── /sound                 # Test tones, impulse responses, biosignal-linked tones
    │
    ├── /data                      # Biosignal logs & normalized examples
    │   ├── /raw                   # Direct sensor streams (time-limited, non-sensitive)
    │   ├── /normalized            # Cleaned & scaled data for mediation testing
    │   └── /mapping_examples      # CSV/JSON showing bio → control mapping
    │
    └── README.md                  # You are here

## **Contributing**

Researchers and students are encouraged to contribute to BABS as part of
the **CHI meta-project ecosystem**. Each contribution should follow
CHI's collaborative AI principles and BBS-aligned documentation
standards: - Maintain transparency of mediation pathways. - Include
calibration data and mapping logic. - Document all human--AI interaction
modes.

## **Citation**

If you use BABS materials in your research, please cite: \> Smith, D, & Duperval, F.
(2025). *Bio-Aware Blended Spaces (BABS): A Balanced Blended Space
Meta-Project.* Center for Holistic Integration, City Tech (CUNY).  

## **Contact**

**Project Director:** Dr. David B. Smith\
Center for Holistic Integration (CHI) -- City Tech (CUNY)\
📧 david.smith@citytech.cuny.edu\
🌐 https://github.com/CHI-CityTech

**Lead Researcher:** Francky Duperval\
Class of 2028 -- City Tech (CUNY)\
📧 Francky.Duperval@mail.citytech.cuny.edu\
🌐 https://github.com/franckydup/Francky-Duperval
