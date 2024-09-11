# Emergency Department Simulation

###### **Authors**: Ziad Ahmed & Shivam Missar
###### **Emails**: ziad.ahmed@nhs.net | shivam.missar@nuh.nhs.uk
###### **Date**: 04/09/2024

###### Part of the Graduate scheme  by NTU


## Problem Statement
Many departments within the Emergency Department (ED) are under-resourced due to inefficient resource management. This has led to some areas being over-resourced while others are left exposed, resulting in longer patient wait times. Our goal is to create a simulation that highlights resource optimization strategies to reduce patient wait times and improve efficiency within the ED.

## Background
The National Health Service (NHS) has been facing increasing pressure due to rising demand for emergency services, leading to significant delays in patient treatment. In recent years, NHS ED wait times have consistently exceeded target levels, with some patients waiting hours for treatment or even a bed. This resource strain within ED departments has created bottlenecks, increasing patient frustration and, in some cases, compromising the quality of care.

As hospitals continue to experience this imbalance in resource allocation, it is vital to find ways to optimize existing resources effectively to reduce wait times and ensure that patient care is timely and efficient.

## Goal
The goal of this simulation project is to explore and model resource allocation in EDs to identify strategies that:
- **Decrease patient wait times** by more effectively managing and distributing resources.
- **Optimize bed utilization** to reduce inefficiencies in how hospital resources are allocated among different acuity levels (Major, Minor, and Resus).

## Methods Used
### Simulation Design
The simulation was built within the programming language known as **Python** which supports a thousands of different libaries and frameworks. For this particular case, a simulation framework was developed within Python to model patient flow through ED.


 Patients were classified into three acuity levels:
- **Major** (high severity),
- **Minor** (low severity),
- **Resus** (emergency).

The simulation models patient arrivals, bed assignments, wait times, and the flow through the medical process, simulating 30 days of operations. The simulation was configured with varying bed allocations for each acuity level to assess the impact on patient wait times and bed occupancy.

### Approach
- **Arrival Patterns**: Modeled using Poisson distributions to simulate realistic patient arrival times.
- **Bed Usage**: The simulation tracked bed occupancy for each acuity level in the ED.
- **Queue Lengths**: Measured the number of patients waiting for beds at any given time.
- **Resource Allocation**: Tested different scenarios to evaluate how changing the number of available beds affects patient wait times and queue lengths.



## Risks and Limitations
- **Patient behavior variability**: The simulation assumes that patients behave in predictable patterns, but real-world variables, such as unexpected surges in patient arrivals, may differ.
- **Resource constraints**: The model assumes fixed bed availability but does not take into account staffing shortages, equipment availability, or other real-world limitations that could affect ED operations.
- **External factors**: Delays in patient transfer or discharge, as well as hospital-specific policies, were not considered in the simulation, which could impact the findings.

## Packages Used
The following **Python** libraries were used for the development and execution of the simulation:
- **SimPy**: Used to model the discrete event simulation of patient flow and bed allocation.
- **Pandas**: For data manipulation and analysis.
- **NumPy**: Used for numerical computations and generating random variables.
- **Matplotlib**: For plotting and visualizing the simulation results.
- **Seaborn**: For enhanced data visualization.
- **Prophet**: Used for time series forecasting to analyze patient arrival trends.



## Results
The simulation revealed several key findings:
- **Major patients** consistently faced long queues, even with high bed allocations, showing that demand for Major beds often outstrips supply.
- **Minor patients** showed moderate fluctuations in bed usage, with occasional queue spikes but generally manageable wait times.
- **Resus patients** had low occupancy and minimal queues, indicating that resources for this group were sufficient.

### Recommendations
- **Increase Major bed allocation**: The demand for Major patients consistently exceeded the available beds, causing long queues. Increasing the number of beds for Major patients would help reduce wait times significantly.
- **Dynamic bed management**: Implementing dynamic bed allocation strategies could optimize resource utilization by shifting beds between acuity levels based on real-time demand.
- **Scenario testing**: Future simulations should explore more scenarios such as crisis situations (e.g., flu outbreaks) to stress-test resource allocation strategies.

## Conclusion
This project has demonstrated how a simulation model can help optimize resource allocation in the ED, reducing patient wait times and improving overall efficiency. By increasing Major bed availability and implementing dynamic resource management strategies, hospitals can better handle fluctuations in demand and alleviate strain on ED resources.
