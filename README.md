# Seminar-Respiratory_Rate_Estimation_on_Embedded_System

This repository documents a B.Tech seminar on the topic of 

Respiratory Rate (RR) Estimation on an Embedded System, based on the research paper "Respiratory Rate Estimation on Embedded System". The seminar explores the feasibility of implementing real-time RR monitoring on resource-constrained platforms, a crucial step for the development of wearable healthcare devices. It delves into a novel algorithm and its practical implementation on a low-power microcontroller.


## Seminar Overview & Key Concepts

The seminar focuses on the design and evaluation of a system that estimates RR from photoplethysmography (PPG) signals. Key concepts covered include:


Signal Processing Pipeline: The process of acquiring and refining raw PPG data through a series of steps, including standardization, filtering, and peak detection.



Fourier Product (FP) Estimator: A novel method that improves accuracy by combining the frequency spectra of multiple respiration-induced variations from the PPG signal. This technique enhances the true respiratory signal while suppressing noise and artifacts.


Embedded System Implementation: The practical deployment of the algorithm on an embedded platform, including hardware architecture, software workflow, and resource management.




Dual-Mode Operation: An optimized approach that allows the device to operate in a continuous or intermittent mode, balancing real-time monitoring with extended battery life.

## Project Implementation & Technical Details

The core of the seminar involved implementing and evaluating the system discussed in the paper. This repository contains the code and resources related to that implementation.

Hardware: The prototype utilizes an MSP432P401R microcontroller, a SEN-15219 PPG sensor, and an HC-06 Bluetooth module.



Software: The system's software architecture is built on a function-queue scheduling mechanism that allows the microcontroller to operate efficiently in a low-power state. The algorithm itself is a lightweight implementation, and the accompanying GUI is developed in Python.

Performance: The FP method achieved a Mean Absolute Error (MAE) of 4.13 rpm on the BIDMC PPG and Respiration dataset, demonstrating a strong balance between accuracy and computational efficiency.




## How to Use

This section outlines how you can run the code and explore the implementation discussed in the seminar.

Hardware Setup: Follow the wiring diagram provided in the seminar report to connect the MSP432P401R, SEN-15219, and HC-06 Bluetooth module.

Microcontroller Firmware: Upload the embedded C code to the MSP432 using a suitable IDE like TI CCS.

GUI Application: Run the Python script to launch the GUI. This application will connect to the Bluetooth module and visualize the incoming data.

## Future Scope

Building upon this seminar, several areas can be explored as future work or a follow-up project:

Further Optimization: Investigate more advanced power-saving techniques, particularly for the power-hungry sensor and Bluetooth modules.

Algorithm Refinement: Explore incorporating machine learning models that are optimized for low-resource environments to further improve the accuracy of the RR estimation.

Extended Testing: Validate the algorithm's performance with a wider range of subjects and under more varied conditions to ensure its robustness in real-world scenarios.

## License

This project's source code is licensed under the MIT License.
