# Transmission Line Losses in Airport Ground Radar Communication between Remote Surveillance Antennas and Control Towers
![image](https://github.com/user-attachments/assets/1c80c9b5-dc07-4cb8-a29f-8fd7f7aad496)


## 1. Introduction

Modern air traffic control systems rely heavily on real-time data from radar installations spread across the airport perimeter. These ground-based surveillance radars are essential for aircraft movement monitoring, runway incursion prevention, and enhanced situational awareness during low-visibility operations. Typically, radar data is transmitted from remote antennas installed far from the main control tower to central processing units using high-frequency transmission lines.

However, when these radar signals travel over long distances—sometimes over 300 meters—they encounter signal degradation. This occurs due to transmission line characteristics and environmental challenges like electromagnetic interference (EMI), temperature fluctuations, and aging infrastructure. These losses can compromise signal integrity, introducing delays and inaccuracies in radar readings.

This case study examines the electrical and physical losses associated with transmission lines used in airport radar systems, highlighting issues like:

- Signal attenuation and phase distortion  
- Impedance mismatches and reflections  
- Environmental degradation in airport environments

It also proposes design solutions such as fiber-optic upgrades, impedance matching, and signal conditioning.

---
![image](https://github.com/user-attachments/assets/3d5993d2-6b28-4aae-94b3-0d355dd74c54)



## Objective

To assess the impact of long-distance signal transmission on airport radar communication and recommend engineering strategies to ensure robust, real-time radar performance from remote antennas to the control tower.

---

## 2. Problem Description

A primary ground surveillance radar located at the edge of the runway (350 meters from the air traffic control tower) communicates radar returns at 300 MHz to the processing unit. The signal is transmitted over a coaxial cable (RG-214/U) installed underground. The system requires that the signal amplitude at the receiver be at least **85%** of the transmitted signal for effective data interpretation. Over time, technicians reported signal delay, power loss, and inconsistent readings.

---
![image](https://github.com/user-attachments/assets/73b7ca09-42b1-4566-b128-baa57b5c6ff9)



## 3. Transmission Line Characteristics

| Parameter | Value |
|----------|--------|
| Cable Type | RG-214/U |
| Resistance (R) | 10.4 Ω/km |
| Inductance (L) | 240 nH/m |
| Capacitance (C) | 100 pF/m |
| Conductance (G) | Negligible |
| Length (l) | 350 m |
| Frequency (f) | 300 MHz |
| Characteristic Impedance (Z₀) | ≈ 50 Ω |
| Attenuation (α) | 0.09 dB/m @ 300 MHz |
| Velocity Factor (VF) | 0.66 |

---

## 4. Signal Attenuation Analysis

**Total Attenuation:**

α_total = 0.09 × 350 = 31.5 dB

markdown
Copy
Edit

**Output Voltage Amplitude:**

V_out = 1 × 10^(-31.5 / 20) ≈ 0.0267 V

yaml
Copy
Edit

> Only 2.67% of the original signal remains—far below the required threshold.

---

## 5. Phase Delay Calculation

**Propagation Velocity:**

v = VF × c = 0.66 × 3 × 10^8 = 1.98 × 10^8 m/s

css
Copy
Edit

**Time Delay:**

t = l / v = 350 / (1.98 × 10^8) ≈ 1.77 μs

yaml
Copy
Edit

> Delay of ~1.77 μs introduces phase skewing in radar return signals.

---

## 6. Impedance Matching and Reflections

Assuming the antenna output impedance is 75 Ω and the receiver is 50 Ω:

**Reflection Coefficient:**

Γ = (Z_L - Z_0) / (Z_L + Z_0) = (75 - 50) / (75 + 50) = 0.2

markdown
Copy
Edit

**Reflected Power:**

|Γ|² = (0.2)² = 0.04 → 4%

yaml
Copy
Edit

> Echoes and signal distortion result in reduced radar accuracy.

---

## 7. Recommendations

### 1. Use Low-Loss Transmission Media
- Replace RG-214/U with **LMR-900** or **RF-over-Fiber**.
- Fiber optic lines offer virtually zero loss over the same distance.

### 2. Impedance Matching
- Use **baluns**, **matching transformers**, or **quarter-wave transformers**.
- Ensure system-wide 50 Ω impedance to prevent reflections.

### 3. Signal Conditioning
- Install **low-noise amplifiers (LNAs)** and **equalizers**.
- Use **automatic gain control (AGC)** circuits.

### 4. Environmental Protections
- Use **EMI-shielded underground conduits**.
- Implement **UV- and water-resistant cable jackets**.

### 5. Upgrade to RF-over-Fiber
- Use **multimode fiber** with **RF-over-Fiber converters**.
- Delivers high fidelity and timing accuracy over long distances.

---

## 8. Conclusion

This study demonstrates how long coaxial cable runs in airport radar systems suffer from attenuation, delay, and impedance mismatch. The observed degradation resulted in signal levels far below operational thresholds, necessitating urgent upgrades. Transitioning to **RF-over-Fiber**, along with proper impedance matching and environmental protections, offers a sustainable, future-proof solution for airport radar communication.

---

## 9. Numerical Examples

### Example 1: RG-214/U Signal Loss
- α = 0.09 dB/m, l = 350 m  
- α_total = 31.5 dB  
- V_out ≈ 0.0267 V (2.67% of input)

### Example 2: Delay
- VF = 0.66, l = 350 m  
- t = 1.77 μs

### Example 3: Mismatch Loss
- Z₀ = 50 Ω, Z_L = 75 Ω  
- Γ = 0.2, Reflected Power = 4%

### Example 4: With LMR-900
- α = 0.013 dB/m  
- α_total = 0.013 × 350 = 4.55 dB  
- V_out ≈ 0.6 V (60% of input)

---

## 10. References

- Times Microwave – LMR Cable Specifications  
- FAA Advisory Circular 150/5220-26  
- Pozar, D. M. – *Microwave Engineering*  
- ICAO Annex 10 – Aeronautical Telecommunications  
- Optical Zonu – RF-over-Fiber White Papers  
- Belden – RG and LMR Cable Data Sheets  
