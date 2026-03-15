# Project Proposal
## Distributed Acoustic Sensing and Ambisonic Spatial Analysis System

## Project Context

The purpose of this project is to investigate how a performance environment can acquire an **acoustic awareness of its own activity**. Rather than treating microphones only as recording devices, the proposed system treats them as **sensors within an environmental perception layer**. In this framework the room itself becomes capable of listening to the acoustic field produced by performers, audience members, and technical systems.

This work sits within the broader development of the **Blended Aware Built Space (BABS)** initiative, which explores how physical environments can acquire sensing capabilities that allow them to perceive events occurring within them. Within BABS, acoustic sensing is only one modality among many (others include environmental sensors, motion sensing, visual sensing, and biometric inputs), but sound offers a particularly rich source of information because it encodes spatial relationships, human activity, and system output simultaneously.

The present project focuses specifically on the **acoustic sensing layer** of that system.

Rather than relying on a single microphone or a traditional recording configuration, the system combines multiple complementary sensing strategies. Distributed microphones observe sound energy at many points in the room. Precision measurement microphones provide reliable calibration and impulse-response analysis. A spatial microphone based on ambisonic capture measures the directional structure of the sound field.

Together these instruments allow the environment to observe sound at multiple spatial scales, from localized acoustic events to the overall directional structure of the room's sound field.

The resulting information can then be analyzed computationally and used to inform responsive behaviors in lighting systems, projection systems, spatial audio playback, or other environmental components.

---

# Objectives

The primary objective of this project is to design and evaluate an acoustic sensing architecture suitable for a research-oriented immersive performance environment.

More specifically, the project seeks to:

- establish a distributed network of microphones capable of detecting acoustic events throughout the space
- capture directional information about the sound field using ambisonic techniques
- investigate how multiple sensing approaches can be combined to infer spatial properties of acoustic events
- provide real-time or near-real-time acoustic data streams to computational systems
- enable the environment to respond to sound events as part of interactive performance systems

The project is not intended to produce a finished commercial system. Instead it serves as an **engineering and research platform** through which multiple experiments can be conducted.

---

# System Architecture

The sensing architecture is organized into three conceptual layers. Each layer captures different properties of the acoustic environment and operates at a different level of spatial abstraction.

## Reference Measurement Layer

The reference measurement layer consists of high-precision microphones used primarily for calibration, validation, and acoustic measurement tasks. These microphones are capable of accurately capturing the frequency response and impulse characteristics of the environment.

Examples include measurement microphones such as Earthworks or Neumann reference microphones that may already be available within the laboratory environment.

These microphones are typically used in controlled measurement scenarios rather than as permanently installed sensors. For example, they may be used to measure the impulse response of the room, evaluate the spatial distribution of sound produced by the speaker system, or calibrate other microphones in the sensing network.

The purpose of this layer is to ensure that experimental measurements can be grounded in reliable acoustic reference data.

---

## Distributed Acoustic Sensor Layer

The distributed sensor layer forms the primary listening network of the environment.

Multiple omnidirectional microphones are placed at strategic locations throughout the room. These microphones continuously capture acoustic activity occurring in different regions of the space.

Unlike the reference microphones, which emphasize measurement precision, the distributed microphones prioritize **coverage and redundancy**. Their role is to provide information about how acoustic events propagate through the environment.

Possible placement locations include:

- structural frames or scenic elements
- walls or ceiling mounting points
- projection screen structures
- equipment racks or architectural features

The microphones in this layer allow the system to estimate where sound events occur and how they spread across the room. By comparing signals across multiple sensors, it becomes possible to explore techniques such as:

- acoustic onset detection
- time-difference-of-arrival estimation
- spatial energy mapping
- zone-based activity detection

Although individual microphones in this layer may not be laboratory-grade instruments, the network as a whole can provide meaningful spatial information when analyzed collectively.

---

## Ambisonic Spatial Capture Layer

While distributed microphones capture sound at multiple locations, an ambisonic microphone captures the **directional structure of the sound field at a single point**.

Ambisonic microphones contain several capsules arranged in a tetrahedral geometry. By combining the signals from these capsules mathematically, it becomes possible to estimate both the pressure of the sound field and the directional components of sound arriving from different directions.

First-order ambisonic systems produce four signals commonly referred to as **B-format channels**:

- W: omnidirectional pressure
- X: front-back directional component
- Y: left-right directional component
- Z: vertical directional component

These signals encode the local acoustic field as a set of spatial components that can later be decoded to different playback formats or analyzed computationally.

In the context of the sensing system, the ambisonic microphone functions as a **spatial probe**. It allows researchers to observe the directional characteristics of sound events and compare them with information obtained from the distributed microphone network.

This dual perspective—multiple spatial sensors combined with a directional field measurement—creates opportunities for investigating acoustic localization and spatial field analysis.

---

# Signal Processing Pipeline

Once acoustic signals are captured by the microphones, they are routed to multichannel audio interfaces connected to a central processing system.

Within the computational environment, several stages of analysis may occur. The specific algorithms used may vary depending on the research objectives of individual projects, but the general workflow includes:

1. acquisition of multichannel audio streams
2. preprocessing and normalization
3. feature extraction
4. spatial inference
5. event interpretation

Feature extraction may involve identifying characteristics such as acoustic onsets, spectral energy distributions, or time delays between sensors. These features can then be used to infer properties of acoustic events occurring in the environment.

For example, an impulsive sound may be detected by several microphones at slightly different times. By analyzing these differences, it may be possible to estimate the approximate location of the sound source.

The resulting information can then be used by other systems within the environment.

---

# Integration with Responsive Systems

One of the motivations for developing an acoustic sensing system is to enable interactions between sound events and other components of the environment.

For example, acoustic events detected by the sensing system might trigger or influence:

- lighting transitions
- projection mapping systems
- spatial audio playback
- generative visual systems
- robotic or mechanical elements

In this context the acoustic sensing system becomes part of a broader environmental perception layer. Rather than merely reproducing sound, the performance space acquires the ability to **perceive and interpret acoustic activity** occurring within it.

This capability opens possibilities for interactive performances in which the environment responds dynamically to performers, audience members, or autonomous systems.

---

# Hardware Components

The system requires several categories of hardware infrastructure.

## Microphones

The sensing system includes three types of microphones:

- reference measurement microphones used for calibration
- distributed omnidirectional microphones forming the sensor network
- an ambisonic microphone capturing directional sound-field information

## Audio Infrastructure

Microphones are connected to multichannel audio interfaces providing:

- microphone preamplification
- analog-to-digital conversion
- synchronization of multiple channels

These interfaces feed audio streams to the central processing computer.

## Computing Environment

A central workstation performs signal acquisition and analysis. Depending on the experimental goals of individual research projects, the computing environment may include:

- digital signal processing frameworks
- real-time audio analysis tools
- machine learning systems for acoustic event classification

---

# Research Opportunities

Because the system combines multiple sensing strategies, it supports a wide range of potential investigations. Examples include:

## Spatial Acoustic Mapping

Using distributed microphones and ambisonic capture to estimate how acoustic energy propagates through the environment.

## Acoustic Event Detection

Developing algorithms capable of identifying specific classes of acoustic events such as speech, percussive sounds, or environmental noise.

## Localization Experiments

Exploring techniques for estimating the spatial origin of sound events based on timing differences between microphones.

## Interactive Performance Systems

Linking acoustic events to generative visual or sonic processes.

## Immersive Audio Research

Studying how spatial audio playback interacts with the acoustic characteristics of the room.

---

# Implementation Phases

The project may be developed through several overlapping phases.

## Phase 1 – Infrastructure Deployment

Install distributed microphones and confirm reliable signal acquisition from all channels. Deploy the ambisonic microphone and verify decoding workflows.

## Phase 2 – Measurement and Calibration

Use reference microphones to measure the acoustic characteristics of the room and calibrate distributed sensors.

## Phase 3 – Algorithm Development

Develop analysis tools capable of detecting acoustic events and estimating spatial properties of sound sources.

## Phase 4 – Environmental Integration

Connect acoustic analysis outputs to lighting, projection, and spatial audio systems.

## Phase 5 – Experimental Applications

Conduct research experiments exploring environmental awareness and interactive performance.

---

# System Overview Diagram

Below is a conceptual ASCII diagram of the proposed sensing architecture. Because it is plain text it can be embedded directly in Markdown documents and will render correctly in GitHub repositories.

```text
                    DISTRIBUTED ACOUSTIC SENSING SYSTEM
                    -----------------------------------

                  [ Acoustic Events in the Room / Sound Field ]
                                   |
         ---------------------------------------------------------------
         |                              |                              |
         |                              |                              |
         v                              v                              v

+---------------------+      +---------------------+      +----------------------+
| Distributed MEMS    |      | Reference /         |      | Ambisonic Spatial    |
| Microphones         |      | Measurement Mics    |      | Microphone           |
| (I2S / local nodes) |      | (analog / XLR)      |      | (B-format / 4 ch)    |
+---------------------+      +---------------------+      +----------------------+
         |                              |                              |
         |                              |                              |
         v                              v                              v

+---------------------+      +---------------------+      +----------------------+
| ESP32 Sensor Nodes  |      | Multichannel Audio  |      | 4-ch Audio Interface |
| / local acquisition |      | Interface / Preamps |      | / decoder input      |
+---------------------+      +---------------------+      +----------------------+
         |                              |                              |
         |                              |                              |
         -----------------------+--------+------------------------------
                                 |
                                 v

                   +--------------------------------------+
                   | Central Processing / Analysis System |
                   |--------------------------------------|
                   | - acquisition                        |
                   | - event detection                    |
                   | - spectral / temporal analysis       |
                   | - TDOA / spatial inference           |
                   | - room-state modeling                |
                   +--------------------------------------+
                                 |
               -----------------------------------------------
               |                     |                      |
               |                     |                      |
               v                     v                      v

   +-------------------+   +---------------------+   +----------------------+
   | Acoustic Event    |   | Spatial Analysis /  |   | BABS Room-State /    |
   | Detection         |   | Localization        |   | Mediation Layer      |
   +-------------------+   +---------------------+   +----------------------+
                                 |
                                 v

                   +--------------------------------------+
                   | Environmental / Performance Response |
                   |--------------------------------------|
                   | - lighting                           |
                   | - projection                         |
                   | - spatial audio control              |
                   | - robotics / kinetic response        |
                   +--------------------------------------+
                                 |
                                 v

                   +--------------------------------------+
                   | 7.1.4 Playback / Anchor Speakers /  |
                   | Other Actuators in the Room         |
                   +--------------------------------------+
```

# Role within the BABS Initiative

Within the broader BABS initiative this project contributes the **acoustic perception layer**. By enabling the environment to observe and interpret sound events, the system supports research into how built spaces can function as active participants in mediated experiences.

Rather than treating the room as a passive container for performance, the acoustic sensing system allows the environment to act as a listener, observer, and potential collaborator within the performance ecology.

This perspective aligns with the broader goals of the BABS project, which seeks to explore how sensing, computation, and responsive systems can transform built environments into interactive and perceptually aware spaces.

