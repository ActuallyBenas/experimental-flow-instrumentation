# Experimental Fluid Flow & Instrumentation | Bernoulli Principle

**University of Central Florida · Mechanical Engineering Measurements (EML 3033C) · Summer 2026**  
**Tools:** LabVIEW, NI 9215 DAQ, Pitot-static tube, differential pressure transducers, Microsoft Excel

> **Project type:** Four-person academic laboratory project. Results presented below were obtained by the team. **Before publishing:** describe your personal contributions accurately in the section below and confirm permission to share the team's materials.

## Project overview

This experiment investigated steady airflow through a converging-diverging duct. The team calibrated two differential pressure transducers, collected pressure measurements with a Pitot-static probe and LabVIEW data-acquisition setup, and compared the resulting velocity and pressure trends with the Bernoulli and continuity equations. Uncertainty analysis was used to evaluate the reliability and limitations of the measurements.

**[View the illustrated three-page case study (PDF)](Bernoulli_Flow_Instrumentation_Case_Study.pdf)** — includes calibration plots, velocity and pressure profiles, the LabVIEW configuration, and analysis of total-pressure losses.

## Key results

| Quantity | Reported result |
| --- | --- |
| Pressure-transducer calibration | **R² = 0.9998** for each of two sensors |
| Measurement locations | **30 nominal positions** along the duct (as described in the report) |
| Peak measured centerline velocity | **30.6 m/s** near the narrowest section |
| Mean Bernoulli constant | **163.8 ± 16.4 Pa** (reported 95% confidence interval for mean) |
| Mean estimated mass flow rate | **0.0472 ± 0.0035 kg/s** (reported 95% confidence interval for mean) |
| Air-density uncertainty | **0.0019 kg/m³ (0.17%)** |

## Engineering approach

1. **Sensor calibration:** Apply positive and negative gauge pressures to two pressure transducers and fit linear voltage-to-pressure relations (R² = 0.9998 for both).
2. **Data acquisition:** Connect the sensors and Pitot-static probe through an NI 9215 DAQ and the LabVIEW virtual instrument.
3. **Flow measurement:** Record static and dynamic pressures at nominally 30 positions along the converging-diverging duct.
4. **Analysis:** Use Bernoulli's equation and continuity relationships to calculate local centerline velocity, total pressure, and a mass-flow estimate; evaluate uncertainty using Excel.
5. **Interpretation:** Compare observed distributions with ideal-flow predictions, and identify where nonideal effects and measurement limitations matter.

### Reported calibration equations

Pressure in Pa; transducer output voltage in V:

- **Transducer 1:** `P = 560.48 V - 2728.5`
- **Transducer 2:** `P = 505.34 V - 2548.7`

These are calibration relationships for the lab's experimental setup, not universal sensor specifications.

## Discussion

As the duct converged, the measured flow accelerated and the static pressure decreased, consistent with the Bernoulli and continuity relationships. The stagnation-pressure estimate was approximately **193.7 Pa at the entrance** and **192.4 Pa near the throat**, but fell to approximately **72.2 Pa near the exit**. This pattern is consistent with viscous losses in the diverging region; flow separation was discussed as a possibility, not directly measured.

One important limitation was that a Pitot-static tube measured **centerline velocity**, whereas calculating mass flow as `rho × area × centerline velocity` effectively assumes that velocity is uniform across the duct. Boundary layers make that assumption imperfect and help explain why the location-by-location mass-flow estimates varied.

The team also encountered unreliable readings from an initial workbench setup and restored usable measurements by switching to another bench. Additional uncertainty sources included probe alignment, transducer calibration drift, tubing condition, instrumentation resolution, and geometric measurements.

## Possible extensions

- Perform repeated measurements at each location to estimate run-to-run variability.
- Traverse the Pitot probe across the duct's cross section to estimate mean velocity more accurately.
- Compare measured pressure loss with a numerical model, keeping modeling assumptions explicit.


### My Contributions

This was a four-person team project completed during the Summer 2026 semester as part of UCF's Mechanical Engineering Measurements Laboratory.

My contributions included:

- **Experimental Setup and Instrumentation:** Assisted with setting up the converging-diverging duct experiment, connecting pressure transducers, and positioning the Pitot-static tube to measure airflow properties.
- **Sensor Calibration:** Participated in calibrating two differential pressure transducers and evaluating voltage-pressure relationships using linear regression.
- **Data Collection and Troubleshooting:** Assisted with collecting static and dynamic pressure measurements using LabVIEW and troubleshooting equipment issues to obtain reliable experimental data.
- **Engineering Analysis:** Analyzed experimental measurements using Bernoulli's equation and continuity principles to determine airflow velocity, mass flow rate, and pressure variations.
- **Technical Documentation:** Contributed to preparing the final laboratory report, including experimental results, graphs, uncertainty analysis, and engineering conclusions.
