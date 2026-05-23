# 2.4 GHz Microstrip Patch Antenna Design

> A rectangular microstrip patch antenna designed and optimised using **Ansys HFSS**, engineered for IEEE 802.11b/g/n (Wi-Fi) and Bluetooth applications operating in the 2.4 GHz ISM band.

---

## Key Results

| Parameter | Target | Achieved |
|---|---|---|
| Resonant Frequency | 2.400 GHz | **2.3884 GHz** *(−0.48% shift due to fringing fields)* |
| Return Loss $S_{11}$ | ≤ −10 dB | **−35.76 dB** |
| VSWR | ≤ 1.50 | **1.26** *(at design marker)* |
| −10 dB Bandwidth | Maximise | **65 MHz** *(2.356 – 2.421 GHz)* |
| Peak Gain | > 2.0 dBi | **2.81 dBi** |

---

## Project Objectives

1. **Analytical Sizing** — Calculate initial patch dimensions (width $W$, length $L$, effective permittivity $\varepsilon_\text{eff}$) using the standard transmission line model.
2. **Inset Feed Optimisation** — Match the high radiating-edge impedance (200–400 Ω) down to a 50 Ω microstrip line using a cosine-squared feed taper.
3. **Parametric Sweeps** — Fine-tune resonant frequency and bandwidth by sweeping feed inset depth, gap width, and patch dimensions in HFSS.
4. **Full EM Analysis** — Characterise far-field performance, $S_{11}$, VSWR, input impedance ($Z$-parameters), and 3D radiation patterns.

---

## Design Equations

**Patch Width**

$$W = \frac{c}{2f_0}\sqrt{\frac{2}{\varepsilon_r + 1}}$$

**Effective Dielectric Constant**

$$\varepsilon_\text{eff} = \frac{\varepsilon_r+1}{2} + \frac{\varepsilon_r-1}{2}\left[1 + 12\frac{h}{W}\right]^{-1/2}$$

**Patch Length** *(accounting for fringing fields)*

$$L = \frac{c}{2f_0\sqrt{\varepsilon_\text{eff}}} - 2\,\Delta L$$

**Inset Feed Resistance**

$$R_\text{in}(y_0) = R_\text{in}(0)\cos^2\!\left(\frac{\pi}{L}\,y_0\right)$$



## Tools Used

- **Ansys HFSS** — 3D full-wave EM simulation
- **Transmission Line Model** — Analytical initial sizing
- **Parametric Sweep** — Feed and geometry optimisation

---

## References

- Balanis, C. A., *Antenna Theory: Analysis and Design*, 4th ed., Wiley, 2016.
- Pozar, D. M., *Microwave Engineering*, 4th ed., Wiley, 2011.
- IEEE Std 802.11-2020 — Wireless LAN Medium Access Control and Physical Layer Specifications.
