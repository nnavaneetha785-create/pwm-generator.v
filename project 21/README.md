# PWM Generator using Verilog

## 📌 Project Description

This project implements a **Pulse Width Modulation (PWM) Generator** using Verilog HDL.

PWM is a technique used to control the average power delivered to a device by changing the **duty cycle** of a digital pulse signal while keeping the frequency approximately constant.

The design uses an 8-bit counter and an 8-bit duty-cycle input to generate the PWM output.

## ⚙️ Features

* 8-bit PWM resolution
* Programmable duty cycle
* Synchronous counter operation
* Reset functionality
* Simple RTL design
* Simulation-ready testbench

## 🧠 Working Principle

The PWM generator continuously increments a counter from 0 to 255.

The PWM output is:

* `HIGH` when `counter < duty_cycle`
* `LOW` when `counter >= duty_cycle`

The duty cycle can be approximately calculated as:

**Duty Cycle (%) = (duty_cycle / 256) × 100**

### Example

| Duty Cycle Input | Approx. Output Duty Cycle |
| ---------------: | ------------------------: |
|               64 |                       25% |
|              128 |                       50% |
|              192 |                       75% |
|              255 |                     ~100% |

## 🔌 Inputs and Outputs

| Signal       | Direction |  Width | Description             |
| ------------ | --------- | -----: | ----------------------- |
| `clk`        | Input     |  1 bit | Clock signal            |
| `reset`      | Input     |  1 bit | Reset signal            |
| `duty_cycle` | Input     | 8 bits | Controls PWM duty cycle |
| `pwm_out`    | Output    |  1 bit | Generated PWM signal    |

## 🛠️ Tools Used

* Verilog HDL
* Icarus Verilog / ModelSim / Vivado
* GTKWave for waveform visualization

## 📂 Project Structure

```text
pwm-generator-verilog/
├── README.md
├── pwm_generator.v
├── pwm_generator_tb.v
└── simulation/
    └── pwm_waveform.png
```

## 🧪 Simulation

The testbench verifies the PWM generator at different duty-cycle values:

1. 25% duty cycle
2. 50% duty cycle
3. 75% duty cycle
4. ~100% duty cycle

The waveform should show that the HIGH duration increases as the duty-cycle value increases.

## 📊 Expected Output

```text
Duty Cycle = 64
PWM Output  → 25% HIGH, 75% LOW

Duty Cycle = 128
PWM Output  → 50% HIGH, 50% LOW

Duty Cycle = 192
PWM Output  → 75% HIGH, 25% LOW

Duty Cycle = 255
PWM Output  → Approximately 100% HIGH
```

## 🎯 Applications

PWM generators are commonly used in:

* Motor speed control
* LED brightness control
* Power electronics
* Servo control
* Digital-to-analog conversion
* Embedded systems

## 📚 Concepts Learned

* PWM generation
* Duty-cycle control
* Counters in Verilog
* RTL design
* Testbench development
* Digital waveform simulation

## 👩‍💻 Author

Navaneetha

**B.Tech – Electronics and Communication Engineering**
