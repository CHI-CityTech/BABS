## **Candidate Sensor Sources:**

- Consumer wearables (Apple Watch, Fitbit, Oura, Muse) for heart rate and activity.

- Research devices (OpenBCI, Polar H10, Embrace Plus) for EEG, HRV, GSR.

- Primitive sensors (contact mics, piezo elements, pressure mats) for basic heartbeat or movement capture.

- Cameras (RGB + depth) for respiration, facial affect, and micro-movements.

## **Considerations**

- Do I need access to the device itself or the space that it is regularly used in along with the person using it?

## **Evaluation Criteria**

- Intuitiveness of Use

- Extent of raw data that is able to be accessed through the sensor) (Need access to the raw biosignals and physiological data)

## **Consumer Biosensors**

- Apple Watch

- Raw sensor and usage data are available only to researchers through the SensorKit framework, after obtaining user consent and ethics committee approval.

- Users can export a summary of their health data from the Health app.

- Apple's ResearchKit and SensorKit frameworks are designed for medical research and make data collection systematic and scalable.

- Fitbit

- Intraday data (e.g., 1-minute resolution heart rate) is available to developers and researchers via the Web API, but full raw biosignals are not.

- The Fitbit Web API and tools for researchers (e.g., via the All of Us research program) are well-documented for collecting large-scale data.

- Oura

- Accessing detailed data requires using the web platform to download CSV or JSON files. Designed more for aggregate daily metrics than granular data streams

- Detailed data, including PPG data like resting heart rate and heart rate variability (HRV), can be exported in spreadsheet format (CSV/JSON) via the Membership Hub.

- **MUSE**

- Accessing detailed data requires using the web platform to download CSV or JSON files. Designed more for aggregate daily metrics than granular data streams.

- The Muse SDK provides direct access to raw EEG, PPG, and accelerometer streams. The device is specifically designed for this type of detailed signal access for developers and researchers.

## **Research Biosensors**

- **OpenBCI**

- Data is accessible through open-source software and can be streamed or saved as CSV files for analysis in programs like MATLAB or EDFBrowser.

- PolarH10

- Raw Inter-Beat-Intervals (IBI) data can be accessed using the Polar app or third-party logging tools, though some full raw data streams may be restricted.

- **EmbracePlus**

- Provides direct access to high-quality, continuous raw data in formats like Avro. Designed specifically for research and avoids "black box" algorithms.

- Access requires partnerships/licensing

Based on the parameters of Stage 1 and the ability of each of the sensors to provide raw unprocessed data

The best candidates are

- OpenBCI

- **Raw Data**: Full raw EEG/EMG/ECG.

- **Signal Quality**: Research-grade, open hardware, highly validated.

- **Integration**: Python SDK + OSC streaming → direct into MAX/MSP.

- MUSE

- **Raw Data**: Raw EEG available through Muse SDK.

- **Signal Quality**: Consumer-grade, noisier than OpenBCI, but validated for meditation/research.

- **Integration**: Python libraries exist (e.g., `muselsl` for streaming EEG). Works with real-time audiovisual feedback.

- PolarH10

- **Raw Data**: Raw ECG can be accessed via SDK. More commonly provides R-R intervals (IBI).

- **Signal Quality**: Highly validated for HRV research, robust for chest-strap ECG.

- **Integration**: Python libraries available (Bluetooth Low Energy). Can stream into MAX/MSP.

- EmbracePlus

- Raw Data: Provides raw EDA, PPG, accelerometer, temperature (for research license).

- Signal Quality: Clinical/research-grade, validated across multiple studies.

- Integration: Research SDK allows real-time streaming into Python.

- Shimmer3

- Raw Data: Full access to raw ECG, PPG, EMG, EDA, accelerometer, gyroscope.

- Signal Quality: High-quality, validated, research-grade.

- Integration: Python SDKs available; streams directly into analysis pipelines.

- BITalino

- Raw Data: Fully open access (ECG, EDA, EMG, PPG, accelerometer).

- Signal Quality: Lower fidelity than Shimmer3/BioPac, but adequate for prototyping.

- Integration: Excellent Python support, easy streaming to MAX/MSP.

My choices are Open BCI or MUSE for EEG

PolarH10 or Open BCI or Shimmer3 or BITalino for Heart Rate/ECG/EKG

Other biosensor data collection will be looked at later
