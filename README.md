CIRCUIT EXPLANATION
This project implements a dual-input power redundancy circuit using two LM5050-1 ideal diode controllers and two N-channel MOSFETs. The purpose of the circuit is to allow two power sources (VIN1 and VIN2) to supply a common output (VOUT).
Each LM5050-1 controls a MOSFET. When an input source is available, the controller turns on the MOSFET and allows power to flow to the output with very low voltage drop.
If one input source fails or drops below the output voltage, the LM5050-1 turns off the MOSFET to prevent reverse current from flowing back into that source.
This ensures that the load connected to VOUT continues to receive power as long as at least one input source is active.

MOSFET SELECTION
The SUM40N10-30 N-channel MOSFET was selected for this design.
It has a low RDS(on), which helps reduce power loss and heat dissipation during operation.
The MOSFET also has a suitable gate threshold voltage, allowing it to be driven effectively by the LM5050-1.
Also this one was used in the example application circuit in the datasheet.
