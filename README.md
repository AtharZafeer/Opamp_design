# Opamp_design
I design an opamp with the mentioned specification
The specifications are: 
  VDD/VSS   2.5/-2.5V
  Slew Rate   +5/-5V/μS
  Load capacitor  5pF
  MAX Vin Common Mode 2.1V
  Min Vin Common Mode -1.3V
  Max Vout 2.2V
  Min Vout -2.2V
  Gain Bandwidth 5MHz
  Differential Gain >80dB
  Phase Margin >60٥
  𝑆𝑛(𝑓) [𝑛𝑉/√ 𝐻𝑧] 34

NMOS Model .model NMOD1CAP NMOS LEVEL=1
            + vto = 0.71 gamma = 0.01
            + phi = 0.6 kp= 182e-6
            + lambda = 0.01
            + tox = 9.6e-9
            + cj = 350e-6 cjsw = 120e-12
            + pb = 0.8 mj=0.33 mjsw = 0.33
            + cgso = 0.046e-9 cgdo = 0.046e-9

PMOS MODEL .model PMOD1CAP PMOS LEVEL=1
           + vto = -0.901 gamma = 0.01
           + phi = 0.6 kp= 41.5e-6
           + lambda = 0.01
           + tox = 9.6e-9
           + cj = 350e-6 cjsw = 120e-12
           + pb = 0.8 mj=0.33 mjsw = 0.33
           + cgso = 0.046e-9 cgdo = 0.046e-9
           
          
Achieved results:

VDD/VSS                2.5/-2.5V
Slew Rate              4.9/-5.14 V/uS
max Vin Common Mode    2.2V
min Vin Common Mode    -1.8V
max Vout               2.5v
Min Vout               -2.5V
𝑆𝑛(𝑓) [𝑛𝑉/√ 𝐻𝑧]       55.666359 nV/Hz½
Power dissipation      0.22mW
Gain bandwidth         6MHz
Phase Margin           >60
Differential Gain      >80dB
