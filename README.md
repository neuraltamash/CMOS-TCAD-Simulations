# CMOS TCAD Device Simulations

A TCAD-based study of **NMOS, PMOS, and CMOS inverter device characteristics**, covering DC device behavior, output characteristics, voltage-transfer characteristics, device structures, and channel-length effects.

## Overview

This project explores semiconductor device behavior through TCAD simulations of NMOS and PMOS devices and their use in a CMOS inverter.

The simulations investigate:

- NMOS drain current versus gate voltage
- NMOS drain current versus drain voltage
- PMOS device characteristics
- CMOS inverter voltage-transfer characteristics
- CMOS inverter DC behavior
- Channel-length dependent device behavior
- TCAD device structures
- Simulation logs and extracted results

The project is organized around simulation decks, generated device structures, simulation data, and final graphical results.

## Project Objectives

The main objectives of this project are:

- Study the electrical characteristics of NMOS and PMOS devices.
- Analyze transistor current-voltage behavior.
- Investigate the effect of gate and drain voltages on device current.
- Study CMOS inverter operation using complementary MOS devices.
- Obtain and analyze the CMOS inverter voltage-transfer characteristic.
- Compare device behavior for different channel lengths.
- Understand the relationship between TCAD device structures and electrical characteristics.
- Develop practical experience with semiconductor device simulation workflows.

## Simulation Flow

                         TCAD DEVICE SIMULATION
                                  |
                 +----------------+----------------+
                 |                                 |
                 v                                 v
              NMOS Device                       PMOS Device
                 |                                 |
                 v                                 v
           Device Structure                  Device Structure
                 |                                 |
                 v                                 v
             DC Analysis                       DC Analysis
                 |                                 |
                 +----------------+----------------+
                                  |
                                  v
                         Electrical Results
                                  |
                                  v
                         CMOS Inverter
                                  |
                                  v
                        VTC / DC Analysis
                                  |
                                  v
                         Graphical Results

## Simulations Included

### 1. NMOS ID-VG Characteristics

The NMOS drain current is evaluated as a function of gate voltage.

The simulation is used to study:

- Threshold behavior
- Subthreshold region
- Channel formation
- Drain current variation
- Gate-voltage controlled conduction

Associated deck:

    nmos_idvg.in

### 2. NMOS ID-VD Characteristics

The NMOS output characteristics are obtained by observing drain current as a function of drain voltage.

The analysis helps identify:

- Linear/triode region
- Saturation region
- Drain-current behavior
- Output characteristics of the device

Associated deck:

    04_nmos_idvg_log.in

### 3. NMOS Output Curves

Additional NMOS output-curve simulation is included for device characterization.

Associated deck:

    nmos_output_curves.in

### 4. NMOS Device Structure

The physical/device structure used for the NMOS simulations is generated and stored as a TCAD structure file.

Associated deck:

    nmos_structure.in

Generated structures:

    nmos.str
    nmos_idvg.str

### 5. PMOS ID-VG Characteristics

The PMOS transfer characteristics are studied to analyze the relationship between gate voltage and drain current.

Associated deck:

    pmos_idvg.in

### 6. PMOS Output Characteristics

PMOS output behavior is analyzed for different bias conditions.

Associated deck:

    pmos_output_curves.in

The project also includes simulations for different gate-voltage conditions:

    pmos_vsd_vgs05.log
    pmos_vsd_vgs08.log
    pmos_vsd_vgs10.log
    pmos_vsd_vgs12.log
    pmos_vsd_vgs15.log

### 7. PMOS Device Structure

The PMOS physical/device structure is generated through the TCAD simulation flow.

Associated deck:

    pmos_structure.in

Generated structures:

    pmos.str
    pmos_idvg.str

## CMOS Inverter

The project combines NMOS and PMOS devices to study CMOS inverter behavior.

The inverter simulations investigate the relationship between input and output voltages and demonstrate the switching behavior of a CMOS logic inverter.

Associated simulation decks:

    cmos_init.in
    cmos_init.cir
    cmos_inverter.in
    cmos_vtc.in

## CMOS Voltage Transfer Characteristic

The CMOS inverter VTC is used to observe how the output voltage changes with the applied input voltage.

The characteristic provides information about:

- Logic-low output
- Logic-high output
- Transition region
- Switching behavior
- NMOS/PMOS interaction
- CMOS inverter DC response

Associated deck:

    cmos_vtc.in

Simulation output:

    cmos_vtc_log_dc_1.log

## Channel-Length Comparison

The project also includes graphical analysis of device behavior for different channel lengths.

This helps demonstrate how transistor geometry influences electrical characteristics and device performance.

Result:

    channel length comparison.pdf

## Results

Final graphical results are stored in the `results/` directory.

### ID-VD / Device Characteristics

    results/idvd.pdf

### Channel-Length Comparison

    results/channel length comparison.pdf

These results provide a visual representation of the simulated device behavior and parameter-dependent characteristics.

## Device Structures

The `structures/` directory contains generated TCAD structure files.

    structures/
    ├── nmos.str
    ├── nmos_idvg.str
    ├── pmos.str
    └── pmos_idvg.str

These files represent the simulated semiconductor device structures used during the electrical analysis.

## Simulation Data

Simulation logs are stored separately from the input decks and structure files.

    simulation/

The simulation data includes:

- NMOS transfer/output characteristics
- PMOS transfer/output characteristics
- CMOS inverter VTC data
- Different PMOS bias conditions
- NMOS device analysis logs

This separation makes it easier to distinguish simulation inputs from generated outputs.

## Simulation Decks

All primary simulation input files are organized under:

    decks/

### Decks

| Simulation | File |
|---|---|
| NMOS ID-VG | `nmos_idvg.in` |
| NMOS ID-VD / analysis | `04_nmos_idvg_log.in` |
| NMOS output curves | `nmos_output_curves.in` |
| NMOS structure | `nmos_structure.in` |
| PMOS ID-VG | `pmos_idvg.in` |
| PMOS output curves | `pmos_output_curves.in` |
| PMOS structure | `pmos_structure.in` |
| CMOS initialization | `cmos_init.in` |
| CMOS circuit | `cmos_init.cir` |
| CMOS inverter | `cmos_inverter.in` |
| CMOS VTC | `cmos_vtc.in` |

## Project Structure

    CMOS-TCAD-Simulations/
    │
    ├── decks/
    │   ├── 04_nmos_idvg_log.in
    │   ├── cmos_init.cir
    │   ├── cmos_init.in
    │   ├── cmos_inverter.in
    │   ├── cmos_vtc.in
    │   ├── nmos_05um_idvg.in
    │   ├── nmos_idvd.in
    │   ├── nmos_output_curves.in
    │   ├── nmos_structure.in
    │   ├── pmos_idvg.in
    │   ├── pmos_output_curves.in
    │   └── pmos_structure.in
    │
    ├── docs/
    │
    ├── results/
    │   ├── idvd.pdf
    │   └── channel length comparison.pdf
    │
    ├── simulation/
    │   ├── cmos_vtc_log_dc_1.log
    │   ├── idvd_vgs05.log
    │   ├── idvd_vgs10.log
    │   ├── idvd_vgs15.log
    │   ├── nmos_idvg_log.log
    │   ├── pmos_idvg.log
    │   ├── pmos_vsd_vgs05.log
    │   ├── pmos_vsd_vgs08.log
    │   ├── pmos_vsd_vgs10.log
    │   ├── pmos_vsd_vgs12.log
    │   └── pmos_vsd_vgs15.log
    │
    ├── structures/
    │   ├── nmos.str
    │   ├── nmos_idvg.str
    │   ├── pmos.str
    │   └── pmos_idvg.str
    │
    └── README.md

## Key Concepts Studied

### MOSFET Transfer Characteristics

The transfer characteristic describes the relationship between gate voltage and drain current.

It is useful for analyzing:

- Threshold voltage
- Subthreshold conduction
- Device turn-on
- Gate-controlled current

### MOSFET Output Characteristics

The output characteristic describes drain current as a function of drain voltage for different gate-voltage conditions.

It provides insight into:

- Linear operation
- Saturation
- Drain-current modulation
- Device output behavior

### CMOS Inverter

A CMOS inverter uses complementary NMOS and PMOS devices to perform logical inversion.

             VDD
              |
             PMOS
              |
              +------ VOUT
              |
             NMOS
              |
             GND

              |
             VIN
       drives both gates

The inverter output changes according to the applied input voltage.

### Voltage Transfer Characteristic

The VTC represents:

    VOUT = f(VIN)

and is used to analyze the switching behavior of the CMOS inverter.

## Channel-Length Effects

Channel length is an important MOSFET design parameter.

Changing channel length can influence:

- Drain current
- Device drive strength
- Output characteristics
- Short-channel behavior
- Switching characteristics

The project includes a dedicated channel-length comparison to study these effects through simulation.

## Verification and Analysis

The simulation workflow follows:

    Simulation Deck
          |
          v
    TCAD Device Simulation
          |
          v
    Device Structure
          |
          v
    Electrical Analysis
          |
          v
    Simulation Logs
          |
          v
    Graph Generation
          |
          v
    Result Analysis

The generated logs and structure files are retained alongside the final graphical results to provide traceability between the simulation setup and observed device behavior.

## Applications

The concepts explored in this project are relevant to:

- CMOS digital circuits
- Semiconductor device engineering
- VLSI design
- MOSFET characterization
- Integrated circuit design
- Device modeling
- TCAD-based semiconductor research
- Logic-gate design
- Process/device optimization

## Tools and Technologies

- TCAD device simulation
- DeckBuild simulation workflow
- Semiconductor device modeling
- MOSFET analysis
- CMOS circuit analysis
- PDF-based result analysis

## Learning Outcomes

This project provided practical experience in:

- MOSFET device characterization
- NMOS and PMOS simulation
- TCAD simulation workflows
- Device structure generation
- ID-VG analysis
- ID-VD analysis
- CMOS inverter analysis
- Voltage-transfer characteristics
- Channel-length comparison
- Simulation-data interpretation
- Semiconductor device modeling
- Organizing simulation inputs and outputs

## Future Improvements

Possible extensions include:

- Automated parameter sweeps
- Threshold-voltage extraction
- Subthreshold-slope extraction
- Transconductance analysis
- Drain-induced barrier lowering analysis
- CMOS noise-margin extraction
- Switching-point extraction
- Power-delay analysis
- Additional channel-length comparisons
- Automated result plotting
- Comparison with analytical MOSFET models

## Author

**Altamash Ayaz**

B.Tech — Electronics & Communication Engineering

**Jamia Millia Islamia, New Delhi, India**

## License

This project is released under the **MIT License**.