# VCO-SSI2131
A basic and generic VCO based on SSI2131

![VCO product image](./IMG_20251011_013322.jpg)

## Interface

### Main panel

| Name | Type | Description |
|:-----|:-----|:------------|
| `coarse`      | Potentiometer | 
| `fine`        | Potentiometer |
| `freq` LED    | Bi-color LED  | Voltage value for `tri`, green for positive voltage, red for negative voltage
| `pulse width` | Potentiometer | Almost full-range (0% ~ 100%) pulse width control of `pulse`
| `fm amt`      | Potentiometer | `fm` amount
| `pulse amt`   | Potentiometer | `pwm` amount
| `lfm`         | Switch button | FM type for `fm`, exponential (off) or linear (on)
| `lfm` LED     | LED           | Blue LED indicates if `lfm` switched on
| `soft`        | Switch button | Sync type for `sync`, hard (off) or soft (on)
| `soft` LED    | LED           | Blue LED indicates if `soft` switched on
| `lfo/osc`     | Toggle switch | Switch between oscillator mode and LFO mode

> *NOTICE: In LFO mode, `sync` input may not trigger oscillator sync. Not guaranteed to solve this issue.*


### Fine-tuning

There are 3 rheostats on the PCB panel

| Name       | Description |
|:-----------|:------------|
| `VR_SCALE` | Adjust frequency range (scale) for SSI2131
| `VR_HFT`   | Adjust high frequency compensation for SSI2131's exponential converter
| `VR_SINE`  | Adjust sine shaper in tri-to-sine circuit 


## Specification

### Inputs

| Name    | Type    | V<sub>min</sub> | V<sub>max</sub> | Description |
|:--------|:--------|:------|:------|:------|
| `v/oct` | Input   | 0V    | +10V  |
| `fm`    | Input   | -5V   | +5V   | 
| `sync`  | Input   | -5V   | +5V   | Triggers on rising edge
| `pwm`   | Input   | -5V   | +5V   | Pulse wave modulation, only apply for `pulse`


### Outputs
| Name    | Type    | V<sub>min</sub> | V<sub>max</sub> | Description |
|:--------|:--------|:------|:------|:------|
| `sine`  | Output  | -5V   | +5V   | Sine wave
| `tri`   | Output  | -5V   | +5V   | Triangle wave
| `saw`   | Output  | -5V   | +5V   | Downward sawtooth wave
| `pulse` | Output  | -5V   | +5V   | Pulse wave


### Physical dimension

- Height: 3U
- Width: 8hp
- Depth: 36mm


### Power Consumption

- `+12V`: 38mA
- `-12V`: 24mA
- `+5V`: N/A

----------

FAREKIND VIRTUAL ASSETS, May 2025.
