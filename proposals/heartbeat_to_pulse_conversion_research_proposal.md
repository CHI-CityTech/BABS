# Research Proposal: Heartbeat-to-Pulse Conversion System within the Bio-Aware Blended Spaces (BABS) Project for Real-Time Event Triggering

## Working Title
Heartbeat-to-Pulse Conversion within the Bio-Aware Blended Spaces (BABS) Project for Real-Time Downbeat Triggering in Creative and Interactive Systems

## 1. Project Overview
This project is embedded within the broader **Bio-Aware Blended Spaces (BABS)** project as a focused research and prototyping pathway concerned with the extraction of biologically generated timing events from the human body and their conversion into usable control signals for blended environments. Within BABS, the body is treated as an active participant in a mediated system rather than merely as a passive source of biometric data. The present proposal therefore investigates one narrowly defined but foundational transaction: converting a live heartbeat into a clean digital pulse that can be assigned to selected subsystems in a modular real-time environment.

This specific pathway proposes the research, prototyping, and evaluation of a compact heartbeat-to-pulse conversion system capable of converting a live human heartbeat into a clean digital trigger pulse suitable for downstream control of assigned media, lighting, kinetic, or computational subsystems. The immediate goal is intentionally narrow: the system must detect a heartbeat event and emit a single reliable digital pulse on each valid downbeat. More advanced features such as beat-to-beat interval extraction, tempo smoothing, expressive mapping, or confidence estimation may be investigated later, but they are outside the minimum viable prototype for the first phase.

As a BABS sub-project, this work sits at the intersection of biosensing, embedded systems, real-time signal processing, and interactive performance control. It also serves as a useful test case for understanding how physiological events may function as event streams within bio-aware blended environments. In that sense, the heartbeat is treated here not as a medical diagnostic object but as a biologically generated signal source whose events can be transformed into discrete digital transactions.

## 2. Problem Statement
Many maker-oriented heart-rate sensing systems are designed to provide a derived value such as beats per minute rather than a precise and reliable per-beat trigger event. For creative systems, however, the critical requirement is often not a smoothed rate estimate but a discrete digital pulse synchronized to each detected heartbeat. Existing low-cost maker technologies vary significantly in latency, noise susceptibility, placement constraints, and the extent to which they provide access to signals suitable for one-shot event extraction.

This project addresses the following central problem: how can a low-cost DIY system acquire a live heartbeat signal and convert it into a stable, low-latency, one-pulse-per-beat digital output suitable for assignment to selected subsystems in a real-time interactive environment?

## 3. Research Goals
The first-phase goals are deliberately constrained.

The project will:

1. Identify viable low-cost sensing approaches for heartbeat event detection in a DIY maker context.
2. Compare candidate sensing technologies for their suitability as sources of a clean digital downbeat pulse.
3. Build and test at least one working prototype that emits one digital trigger per valid heartbeat.
4. Evaluate latency, false trigger rate, missed trigger rate, motion sensitivity, ease of setup, and practical integration cost.
5. Produce a documented design pathway for future expansion into richer temporal control data if desired.
6. Situate the heartbeat-to-pulse converter as a reusable BABS subsystem that may later be incorporated into larger bio-aware blended environments.
7. Clarify how physiological event streams may be assigned selectively to particular subsystems rather than presumed to function as universal control sources.

## 4. Research Questions
The project will be guided by the following questions.

The primary question is: which low-cost biosensing approach provides the most reliable pathway from live heartbeat acquisition to a one-shot digital trigger in a DIY experimental system?

Supporting questions include:

- Can a single-lead ECG front end provide sufficiently robust R-peak detection for real-time pulse generation in a maker-scale prototype?
- Under what conditions can optical pulse sensing produce a usable one-pulse-per-beat trigger, and where does it fail relative to ECG?
- What thresholding, refractory lockout, and filtering strategies are required to avoid false or duplicate triggers?
- What practical inventory, setup time, body placement, and user burden are associated with each solution type?
- Which prototype architecture is most suitable for later extension into OSC, MIDI, lighting, or embedded control environments?

## 5. Scope and Delimitations
The first phase is limited to downbeat extraction only. The target output is a single digital pulse corresponding to each detected heartbeat. The system is not intended for medical diagnosis, health interpretation, or clinical use. It is a creative and technical sensing prototype situated within the BABS project.

The project will not initially attempt to:

- classify arrhythmias,
- measure clinical ECG quality,
- estimate oxygen saturation,
- infer emotional or cognitive state,
- or control all systems globally.

Instead, the heartbeat pulse will function as one assignable event stream among others in a modular BABS architecture. This framing is important. Within BABS, physiological data are not assumed to govern an entire environment indiscriminately. Rather, they are treated as one class of possible inputs that may be mapped to selected components, media processes, or interaction pathways according to the design of the specific experiment or installation.

## 6. Candidate Solution Types
Several technical pathways should be considered and compared rather than assuming a single answer at the outset.

### A. Single-Lead ECG-Based Detection
This is the leading candidate for the first prototype. A single-lead ECG front end captures the heart’s electrical activity directly and offers the clearest pathway to R-peak detection. The expected signal-processing chain is:

body electrodes -> ECG front end -> ADC sampling -> peak detection -> refractory lockout -> digital pulse output

Advantages include sharper beat timing, more direct access to event structure, and better suitability for one-shot pulse generation. Disadvantages include electrode placement, body contact requirements, and the need for careful electrical isolation.

This solution family includes modules such as AD8232-based or AD8233-based front ends, either as breakouts or evaluation boards.

**Physical Implementation (Practical Prototype Configuration)**

In typical maker implementations the AD8232 is **not the sensor itself**, but rather an analog front-end amplifier that conditions signals coming from skin electrodes. The sensing chain is therefore:

ECG electrodes on body -> electrode lead wires -> AD8232 analog front end -> microcontroller analog input

Typical electrode placement for experimental single-lead detection uses three adhesive electrodes placed approximately at:

- right upper chest (RA)
- left upper chest (LA)
- lower torso reference (RL)

The AD8232 breakout board (typically ~3 cm × 3 cm) is connected to a microcontroller such as an ESP32, Arduino, or RP2040 board using a small number of wires (power, ground, analog output, and optional lead-off detection pins).

For experimental use the electronics may be arranged in one of three configurations:

1. **Bench prototype configuration** — electrodes connected to a breadboard-mounted AD8232 and microcontroller for debugging and waveform inspection.
2. **Wearable belt-pack configuration** — electrodes on the chest connected by short leads to a small enclosure containing the AD8232, microcontroller, and battery pack.
3. **Body-mounted module configuration** — the sensing electronics mounted close to the electrodes in a compact enclosure to reduce motion noise.

For the purposes of this project the second configuration (electrodes + small electronics enclosure worn on belt or pocket) is expected to provide the best balance between signal stability and experimental flexibility.

### B. Optical PPG-Based Detection
Optical sensing detects blood-volume changes using light rather than the heart’s electrical event. A photoplethysmography module may be easier to wear or integrate in some contexts, but the resulting signal is usually more vulnerable to motion artifacts, contact inconsistency, and timing ambiguity when the goal is a precise downbeat pulse.

The signal chain is typically:

optical sensor -> digital or analog pulse waveform -> peak detection -> refractory lockout -> digital pulse output

Representative modules include:

- MAX30102 optical pulse / pulse-oximeter module
- OpenBCI **PulseSensor** analog optical heart rate module

The PulseSensor in particular is widely used in the maker and OpenBCI ecosystem because it provides a directly readable analog waveform that can be sampled easily by a microcontroller. However, because the optical pulse represents blood flow rather than the electrical heartbeat event, the signal often exhibits broader peaks and is more sensitive to finger movement or inconsistent pressure.

In practice these sensors are commonly mounted on:

- fingertip
- earlobe
- soft finger clip or foam pad

While these sensors are easier to deploy than ECG electrodes, they are expected to produce less precise beat timing for impulse-generation purposes.

### C. Mechanical Pulse Sensing
Mechanical approaches use vibration, pressure, or body-surface movement to infer pulse events. Piezo discs, force-sensitive resistors, and contact microphones have all been used experimentally in DIY contexts.

Advantages include low cost and high experimental flexibility. Disadvantages include major susceptibility to motion, mounting inconsistency, and typically poorer repeatability than ECG.

This approach should be treated as exploratory rather than primary unless early tests prove unexpectedly robust.

### D. Existing Wearable Consumer Devices as Upstream Sources
A fourth solution type is to investigate whether existing wearables can expose sufficiently immediate heartbeat events. This includes devices marketed for meditation, fitness, or brain sensing.

The main research issue here is that many consumer devices expose only derived values such as BPM, smoothed pulse estimates, or restricted SDK outputs rather than raw event-quality beat signals. This category may still be reviewed as a comparative case, but it is unlikely to be the main solution for a reliable DIY pulse converter.

## 7. Working Hypothesis
The working hypothesis is that a single-lead ECG-based system will provide the most reliable low-cost pathway for converting heartbeat into a clean digital pulse because it captures the electrical event directly and therefore offers clearer peak timing than optical or mechanical alternatives.

A secondary hypothesis is that optical pulse sensing may still be adequate for low-demand experimental contexts, but will produce higher false-trigger and missed-trigger rates under motion or inconsistent placement.

## 8. Proposed System Architecture
The first-phase prototype should use a modular architecture so that sensing, detection, and output remain separable and can later be integrated into the larger BABS framework.

### Functional Architecture
1. Sensor acquisition layer
2. Signal conditioning and sampling layer
3. Peak detection layer
4. Refractory lockout / debounce layer
5. Digital pulse output layer
6. Logging and evaluation layer
7. BABS integration layer for routing the validated pulse to selected subsystems

### Conceptual Event Flow
heartbeat signal -> validated beat event -> one-shot digital pulse -> assignable BABS event stream

### Core Detection Rule
A pulse should be emitted only when:

- the incoming signal exceeds a threshold,
- the waveform shape or slope is consistent with a valid beat event,
- and the system is not within an active refractory lockout window.

This lockout is essential to prevent multiple pulses from a single beat or from noise immediately surrounding the event.

Within BABS, the output of this prototype should be understood as a modular event source. It may be routed to selected audio, visual, haptic, kinetic, computational, or logging processes, but those mappings should remain external to the pulse-conversion core. This separation will preserve reusability and allow the same heartbeat event stream to participate in different experimental mediation pathways.

## 9. Methodology
The project should proceed through a staged experimental workflow.

### Phase 1: Comparative Review and Bench Selection
Select representative components from at least three sensing categories: ECG, optical PPG, and mechanical sensing. Review documentation, required wiring, signal accessibility, and probable event latency.

### Phase 2: Prototype Construction
Build at least one ECG-based prototype and, if feasible, one comparative optical prototype. Use a common microcontroller platform where possible so that differences arise primarily from sensing method rather than entirely different computing stacks.

### Phase 3: Signal Capture and Trigger Testing
Acquire data from live use sessions under controlled conditions. For each prototype, examine:

- whether the beat is visually detectable,
- whether a threshold-based detector can produce one pulse per beat,
- whether motion or contact changes cause false or missed pulses,
- and whether the trigger feels sufficiently immediate for real-time use.

### Phase 4: Quantitative Evaluation
Evaluate candidate systems using the following metrics:

- pulse detection success rate,
- false trigger rate,
- missed beat rate,
- duplicate trigger rate,
- trigger latency,
- setup burden,
- user comfort,
- and hardware complexity.

### Phase 5: Integration Trial
Connect the resulting digital pulse to a downstream component such as an LED, GPIO-driven trigger stage, software event logger, OSC sender, or MIDI pulse generator. The purpose is not full system integration but proof that the pulse can function as a useful control event.

## 10. Experimental Output Forms
The prototype should support several output modes, even if only one is used initially.

The minimum output is:

- one digital pulse per validated beat.

Potential output options for testing include:

- microcontroller GPIO high pulse,
- optoisolated trigger output,
- serial event timestamp,
- OSC beat message,
- MIDI note or clock-derived pulse,
- or LED flash for visual confirmation.

## 11. Safety and Ethics
Because this project involves body-connected sensing, safety must be explicit even in a maker context. All prototypes must be battery-powered during body contact testing. Any connection to larger external systems should be electrically isolated. The system must be clearly framed as a non-medical prototype for creative and experimental use only.

Documentation should also note user consent, comfort, and data minimalism. If data logs are stored, they should contain only what is necessary for technical evaluation.

## 12. Inventory Required for Tests
The inventory below is organized into core, comparative, measurement, output, and safety categories. Not every item is mandatory for the first build, but this list provides a realistic testing inventory.

### A. Core ECG Prototype Inventory
- AD8232 single-lead ECG breakout board or equivalent
- Optional AD8233 breakout or evaluation board for comparison
- Disposable ECG electrodes
- Electrode lead cable set
- ESP32 development board or Teensy or RP2040 board
- Breadboard and jumper wires
- Battery pack or USB battery supply
- Onboard status LED or external LED with resistor
- Small enclosure or mounting plate for bench stability

### B. Optical Prototype Inventory
- MAX30102 optical pulse sensor module or equivalent
- OpenBCI PulseSensor module
- Finger clip, foam mount, or soft fixture for stable contact
- Second microcontroller if a parallel setup is preferred
- Jumper wires and small mounting materials

### C. Mechanical / Exploratory Prototype Inventory
- Piezo disc or contact vibration sensor
- Force-sensitive resistor and interface resistor set
- Adhesive or strap-based mounting materials
- Simple op-amp breakout or conditioning board if required

### D. Measurement and Logging Inventory
- Oscilloscope, logic analyzer, or both
- USB serial logging connection
- Laptop with Arduino IDE or PlatformIO
- Breadboard power supply or regulated battery source
- Optional high-resolution external ADC if signal quality testing requires more precision than the built-in ADC

### E. Output and Integration Inventory
- GPIO test LED
- Optoisolator board for safe trigger isolation
- Transistor driver stage if higher-current pulse output is needed
- MIDI interface or USB-MIDI capable microcontroller if MIDI pulse testing is desired
- OSC-capable software environment for event verification
- Terminal block or patch connector system for bench routing

### F. Safety and Practical Bench Inventory
- Battery-only test protocol materials
- Nonconductive mounting surface
- Cable labels and strain relief
- Spare jumper wires and headers
- Alcohol wipes or skin prep materials for electrodes
- Storage bags or bins for disposable components

## 13. Recommended Initial Procurement Set
If budget or time requires a reduced first purchase, the most efficient initial set is:

- 2 x AD8232 ECG modules
- disposable ECG electrodes in bulk
- 1 x ESP32 development board
- breadboard and jumper kit
- 1 x USB battery pack
- 1 x optoisolator module
- LEDs and resistors
- 1 x MAX30102 module for comparison
- basic enclosure and cable management supplies

This reduced set is sufficient to evaluate the leading hypothesis while preserving one comparative pathway.

## 14. Test Plan
The following tests are recommended.

### Test 1: Basic Beat Visibility
Confirm that the waveform is detectable and stable under quiet stationary conditions.

### Test 2: Single Pulse Integrity
Measure whether exactly one digital pulse is emitted per beat under controlled conditions.

### Test 3: Refractory Window Tuning
Vary the lockout interval to determine the best balance between duplicate suppression and missed beats.

### Test 4: Motion Sensitivity
Repeat tests during mild body movement to determine which sensor approaches remain usable.

### Test 5: Trigger Latency
Measure the delay between signal event and digital pulse output using logging or test instrumentation.

### Test 6: Downstream Integration
Use the emitted pulse to trigger a downstream event such as a light flash, software event message, or simple media cue.

## 15. Evaluation Criteria
The preferred prototype will be the one that best satisfies the following criteria:

- one pulse per valid heartbeat,
- low false-trigger rate,
- low missed-trigger rate,
- low practical latency,
- manageable setup complexity,
- acceptable user comfort,
- low cost,
- and straightforward extensibility.

## 16. Expected Deliverables
The project should produce the following deliverables.

1. A written comparative review of candidate sensing approaches.
2. A working prototype for heartbeat-to-digital-pulse conversion.
3. A bill of materials and wiring documentation.
4. Embedded code or pseudocode for the pulse-generation logic.
5. Bench test notes and performance results.
6. A BABS-oriented integration note describing how the validated heartbeat pulse may be routed to selected subsystems within a bio-aware blended environment.
7. Recommendations for phase-two extensions such as interval extraction, OSC output, MIDI output, or multi-channel event mapping.

## 17. Anticipated Next Steps Beyond Phase One
Once a stable one-shot pulse system is demonstrated, future phases may extend the design to include:

- beat-to-beat interval extraction,
- tempo smoothing,
- confidence estimation,
- multiple assignable output channels,
- OSC or network transport,
- MIDI pulse or clock translation,
- and integration into larger modular interactive systems.

## 18. Conclusion
This project proposes a disciplined first step within the broader Bio-Aware Blended Spaces project by focusing narrowly on a heartbeat-to-pulse converter. Rather than attempting to build a full expressive biosensing environment immediately, the research begins with the simpler and more defensible engineering target of producing one reliable digital pulse per validated heartbeat. By comparing ECG, optical, mechanical, and wearable-derived approaches, the project will identify the most practical maker-scale pathway for transforming heartbeat into a robust real-time control signal.

The most likely outcome is that a single-lead ECG-based prototype will provide the clearest and most reliable route to a usable downbeat pulse. Even if later development expands toward richer temporal interpretation, this first prototype will establish the core transaction required for future BABS work: the conversion of a live physiological event into an assignable digital trigger within a modular bio-aware blended system.

Embedded in BABS, the value of this work is not limited to heartbeat sensing alone. It serves as a concrete prototype for how physiological signals may enter a blended environment as event streams, be selectively assigned to specific subsystems, and participate in broader mediated interaction architectures without being mistaken for universal control sources.

