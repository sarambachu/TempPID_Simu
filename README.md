# PID Control Simulation in MATLAB

This repository contains MATLAB simulations demonstrating **PID (Proportional-Integral-Derivative) control** applied to a simple thermal system. The project explores how different PID tunings affect system behavior and compares controlled vs uncontrolled scenarios.

---

## Project Overview

- **Goal:** Simulate a temperature control system and visualize how PID parameters influence system response.
- **System Model:** First-order thermal system:

`{dT}/{dt} = -a(T - T_env}) + b . u`

Where:
  - T = system temperature
  - T_env = ambient temperature
  - u = control input (heater)
  - a, b = system constants

- **PID Control:** Adjusts `u` to maintain a target temperature (`setpoint`) using:

`u = K_p *e + K_i{int(e) dt} + K_d({de}/{dt})`

Where e = T_setpoint - T

---

## Scripts Included

| Script | Description |
|--------|-------------|
| `Good_Tuning.m` | Demonstrates well-tuned PID response. |
| `Good_vs_Bad_Tuning.m` | Compares well-tuned vs poorly-tuned PID controllers. |
| `No_Control_vs_PID.m` | Compares system response without control vs PID control. |

---

## Features

- Clamp control signals (`u`) to realistic limits.  
- Visualize system response over time with MATLAB plots.  
- Explore effects of **bad PID tuning**: overshoot, oscillations, and slow settling.  

---

## How to Run

1. Open MATLAB.  
2. Navigate to this repository folder.  
3. Run any of the scripts (`.m` files) to simulate and visualize PID behavior.  

---

## Insights

- **High `Kp`** → Fast response but may overshoot.  
- **High `Ki`** → Eliminates steady-state error but may cause oscillations.  
- **Low `Kd`** → Underdamped, oscillatory response.  
- **High `Kd`** → Overshoot followed by slow decay; can overreact to rapid changes.  

---

## Optional Enhancements

- Add more visualizations for control signal `u` over time.  
- Introduce noise to simulate a real-world thermal system.  
- Create functions to reuse PID logic across different scripts.

---

## Author

Sara Mbachu – Industrial Automation and Control Systems Engineer
