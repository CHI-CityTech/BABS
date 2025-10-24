# Bio-Aware Blended Spaces (BABS) — Stage 1 Sprint Plan (Fall Semester)

## **Thesis**

The goal of this project stage will be to investigate the translation of biosensory input from cognitive agents (human) to audiovisual output.

## **Hypothesis**

If biosensory data can be captured via physiological measurement devices (EEG, AppleWatch, Fitbit, etc), processed through via middleware (OSC, LSL, and BLE) then they can be translated into audiovisuals (MAX/MSP+Jitter, Augmented Reality)

## **Abstract**

This project performs Stage 1 of the Bio-Aware Blended Spaces (BABS) meta-project, around the Balanced Blended Space framework. The goal is to pursue a minimally-viable prototype by selecting one or more biosensors and testing whether bio-acquired data can be transformed into audiovisual outputs through well-designed mediation pathways.

## **Background**

Emerging media and experiential computing point toward an urgent and innovative landscape: **biosensory-driven environments**, where human physiological states are measured, transformed into data, and recursively mapped back into immersive spaces. These spaces can be **virtual, physical, **and **conceptual**, and may adapt dynamically in response to both **cognitive** (human) and **computational** (AI) agents.

These bio-sensory driven environments have numerous applications whether it be in exploratory research, art performances, collaborative music, or therapeutic applications.

## **Sprint Context**

This sprint focuses on **Stage 1: Core Lab Prototypes**, the foundation of the Bio-Aware Blended Spaces (BABS) meta-project. The goal is to establish a **minimally-viable prototype (MVP)** demonstrating the capture, normalization, and mapping of biosignals into immersive outputs within a lab environment. The sprint spans the **Fall semester** and emphasizes practical deliverables that scaffold future BRPS deployment (Blended Reality Performance System).


## **Objectives**

- Build a **working biosensor acquisition pipeline** using a mix of consumer wearables, research-grade devices, primitive sensors, and cameras.

- Implement **data normalization and mediation pathways** via **Lab Streaming Layer (LSL)**, Open Sound Control (OSC), and Bluetooth Low Energy (BLE) gateways.

- Develop at least one **Max/MSP + Jitter patch** translating biosignal input into audiovisual outputs.

- Create a **single-surface projection (Augmented Reality) sandbox** demonstrating real-time bio → environment → perception mediation.

- Produce **documentation and guides** to ensure reproducibility and scalability.


## **Sprint Deliverables**

For this sprint, the deliverables will consist of **one or more biosensors** chosen from the list below, based on feasibility, availability, and ongoing research/design decisions. The aim is not comprehensive integration but rather to achieve a **minimally-viable prototype (MVP)** demonstrating that the system can successfully transform bio-acquired data into mediated outputs.

**Candidate Sensor Sources:**

- Consumer wearables (Apple Watch, Fitbit, Oura, Muse) for heart rate and activity.

- Research devices (**OpenBCI**, Polar H10, Embrace Plus) for EEG, HRV, GSR.

- Primitive sensors (contact mics, piezo elements, pressure mats) for basic heartbeat or movement capture.

- Cameras (RGB + depth) for respiration, facial affect, and micro-movements.

**MVP Goals:**

1. **Biosensor Acquisition Module (Prototype)**

- Select and integrate at least one sensor from the above list.

- Establish middleware pipeline (**LSL**/OSC/BLE) for data streaming.

- **Data Normalization & Mediation Pathway Framework**

- Develop basic calibration and scaling routines.

- Demonstrate transformation of biosignal data into a normalized control stream.

- **Max/MSP + Jitter Patch**

- Translate the selected biosignal into at least one audiovisual transformation.

- Demonstrate system responsiveness and stability.

- **Projection Sandbox (Augmented Reality) Prototype**

- Project simple visual or auditory responses driven by biosignal mediation.

- Showcase real-time transformation of bio-acquired data.

- **Documentation & Technical Guide**

- Record setup, calibration, and mapping process.

- Provide troubleshooting notes.

- Outline next steps for scaling into larger BRPS environments.


## **Sprint Milestones**

- **Week 1–2:** Sensor inventory, setup, and calibration tests.

- **Week 3–4:** Establish **LSL**/OSC pipeline and basic data normalization.

- **Week 5–6:** Develop Max/MSP + Jitter patch with audio/visual mappings.

- **Week 7–8:** Projection sandbox installation and first test demos.

- **Week 9:** Refine mappings, improve latency and stability.

- **Week 10:** Document systems, draft technical guide, and prepare showcase demo.


## **Sprint Descriptions**

To provide context and inform evolving requirements, each milestone sprint is described narratively below. These descriptions are not technical specifications but rather high-level outlines to guide expectations.

- **Sprint 1 (Weeks 1–2: Sensor Setup and Calibration):** This sprint focuses on identifying which biosensors (consumer, research, primitive, or camera-based) will be trialed for the MVP. Activities include unboxing, testing, and calibrating sensors, ensuring at least one source can reliably produce usable data streams.

- **Sprint 2 (Weeks 3–4: Pipeline Integration):** Establishes the mediation pathway from sensor to software using **LSL**, OSC, or BLE. Success here is defined by seeing live data flow in a normalized format, ready for mapping.

- **Sprint 3 (Weeks 5–6: Max/MSP Patch Development):** Translates raw biosignal data into audiovisual events using Max/MSP and Jitter. At this stage, the goal is responsiveness, even if the mapping is simple or rough.

- **Sprint 4 (Weeks 7–8: Projection Sandbox Demo):** Installs the single-surface projection environment. The first visible demonstration of a bio-aware blended mediation pathway occurs here, linking sensor → data → audiovisual projection.

- **Sprint 5 (Week 9: Refinement):** Focuses on improving the stability, latency, and reliability of the pipeline. This sprint consolidates the prototype into a smoother, more predictable demo system.

- **Sprint 6 (Week 10: Documentation and Showcase):** Produces written guides, troubleshooting notes, and diagrams of mediation pathways. Culminates in a final MVP showcase that demonstrates successful bio → environment transformation.


## **End-of-Sprint Outcomes**

- A working **least-viable prototype (MVP)** of Stage 1 mediation pathways.

- Clear evidence of **bio-aware blended mediation** in action (biosignal → audiovisual output).

- Foundational infrastructure (pipelines, calibration, documentation) for Stage 2 and future BRPS deployment.

- Student and faculty team experience with biosensor integration, creative mapping, and projection-based environments.


## **Evaluation Criteria**

- **Functionality:** At least one biosignal successfully mapped into both sound and visuals.

- **Reliability:** Stable mediation pathways with <200ms latency where feasible.

- **Scalability:** Pipeline ready for integration into larger BRPS environments.

- **Documentation:** Reproducible setup instructions and troubleshooting notes.

- **Engagement:** Participant/audience response to MVP demo.

## **Ethical Considerations**

Stage 1 of the project is focused on the creative and technical capability of mapping biosignals into audiovisuals. Since this stage focuses on the feasibility of biosensory data collection and mapping into audiovisual experiences and not the accuracy of such mapping, cognitive agent participants will not be needed at this stage.

If cognitive agent participants are included in this phase of the project

- Participants will be informed of the extent of data collection as well as the purpose for the data collection

- All data collected will be used solely for this project and will not be saved or utilized for any other purposes

- All data collected will be anonymized to ensure privacy

- Methods of collecting data via physiological biosensory measurement tools will be non-invasive and pose no risk


## **Next Steps (Post-Sprint)**

- Expand from single-surface projection to multi-surface BRPS deployment (Physical & Virtual component implementation).

- Integrate recursive feedback and AI bio-aware blended spaces (Stage 2).

- Begin multi-participant mediation tests.

- Develop performance/therapeutic prototypes based on Stage 1 infrastructure.
