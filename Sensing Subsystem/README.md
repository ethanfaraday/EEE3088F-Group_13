# Sensing Subsysystem

## Author
Ethan Faraday

## Author's Note
This folder is for the design of the sensing module for the Micro-mouse design project. This was a very enjoyable design project despite certain setbacks.

## Navigation of this repo
In this repository, you will find all the files needed to design and build the PCB, and finally the code required to interface it with the STM32 board. In "KiCad Design Files' you will find all the design files required to build the PCB. In 'Datasheets' you will find the datasheets for the components used. In 'Code/ADC/src/main.c' you will find the code for interfacing with the STM32 board.

## Design Decisions:

The main design decision came down to which components to choose for the emitter and detector of the infared light. Ultimately we chose to use the TSAL4400 manufactured by Vishay Intertech as the emitter, and the PD333-3B/H0/L2 manufactured by Everlight Elec as the receiver. For both components, the relative radiant power vs wavelength is greatest around 950nm, which is the typical wavelength of IR light. If you would like to recreate this project, make sure that both the reciever and detector overlap in this regard. 

We decided that the receiver must be powered by the PWM pin from the micro-controller in order to save power. This meant that in order for a valid signal to be read from the ADC the output from the receiver should go through a HPF, or else the ADC signal would constantly be fluctuating and would not be easy to get a reasonable logic signal. 

Lastly, different resistor and capacitor values were used in order to ensure the designed PCB works according to plan. 

## Improvements and Recommendations
The footprint for the IR Emitter's and Receivers should be chosen so that it is angled horizontally with the board. This will save a lot of time and reduces extra soldering required.
