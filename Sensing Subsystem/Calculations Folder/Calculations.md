# Calculations

## BPW34:

Reverse Voltage: Max: 60V (will never reach)\


## TSAL4400:

Forward Voltage: Typ: 1.35V; Max: 1.6V\
Forward Current: Recommend: 100mA; Max: 200mA\

## 2N3904 PNP Transistor:

Desired Ic = 100mA (to run TSAL4400 at recommended current) \
Gain: For Ic = 100mA, Gain = 150\
Ib = Ic/Gain = 100mA/150=0.67mA\
Rb = (3.3-0.9)/0.67mA=3.6k =3.9K\
-> Ic=92mA\
-> Rc= 20 =22