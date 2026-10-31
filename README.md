<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img src="assets/banner-light.svg" alt="Nebiyu Tadesse. Embedded systems, motor control and robotics." width="100%">
</picture>

I'm a mechanical and electrical and computer engineer, a University of Colorado Boulder alum, and I build the layer where
software meets hardware: motor controllers, sensors, secure embedded Linux, and the robots that use them.
I like systems that are portable, testable and documented well enough that someone else can pick them up.

**[HardFOC](https://github.com/hardfoc)** · [What I build](#what-i-build) · [HardFOC in one picture](#hardfoc-in-one-picture) ·
[Start here](#start-here) · [Also public](#also-public) · [Toolbox](#toolbox)

## What I build

| | |
|:--|:--|
| **Motor control and drivers** | Hardware-agnostic C++ drivers for motor, motion and sensing chips, written so the same driver runs on any board through a thin interface. |
| **Board platforms** | A shared platform layer, board support and CI for ESP32-class controllers, from pin configuration up to firmware. |
| **Embedded Linux** | Building a whole board's software stack from source, and teaching how it works. |
| **Robotics** | Simulation, control and test benches for robots and instruments. Most of this work is private, so this page shows the public parts. |

## HardFOC in one picture

[**HardFOC**](https://github.com/hardfoc) is the open-source organization I maintain for a hardware-based FOC (field-oriented control)
motor driver board and the software around it. It has 40+ public repositories, more than twenty of them drivers, and
most have their own documentation site.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/hardfoc-stack-dark.svg">
  <img src="assets/hardfoc-stack-light.svg" alt="HardFOC software stack: board firmware on top of hf-core, on top of a board layer and portable libraries, on top of more than twenty hardware-agnostic drivers. Shared CI and ESP-IDF tooling applies to every layer." width="100%">
</picture>

### Start here

| Repository | What it is |
|:--|:--|
| [`hf-core`](https://github.com/hardfoc/hf-core) · [docs](https://hardfoc.github.io/hf-core/) | The shared platform layer: handlers, RTOS utilities, driver integration and CANopen, in C++20. |
| [`hardfoc-vortex-v1`](https://github.com/hardfoc/hardfoc-vortex-v1) | Firmware for the Vortex v1 controller board. |
| [`hf-tmc9660-driver`](https://github.com/hardfoc/hf-tmc9660-driver) · [docs](https://hardfoc.github.io/hf-tmc9660-driver/) | Hardware-agnostic driver for the TMC9660 motor controller. A good example of the driver pattern. |
| [`hf-tmc5160-driver`](https://github.com/hardfoc/hf-tmc5160-driver) · [docs](https://hardfoc.github.io/hf-tmc5160-driver/) | Hardware-agnostic driver for the TMC5160 stepper driver. |
| [`hf-internal-interface-wrap`](https://github.com/hardfoc/hf-internal-interface-wrap) · [docs](https://hardfoc.github.io/hf-internal-interface-wrap/) | The ESP-IDF wrappers that keep drivers free of platform code. |
| [`hf-general-ci-tools`](https://github.com/hardfoc/hf-general-ci-tools) · [docs](https://hardfoc.github.io/hf-general-ci-tools/) | Shared CI for the whole ecosystem. |
| [`hf-espidf-ci-tools`](https://github.com/hardfoc/hf-espidf-ci-tools) · [docs](https://hardfoc.github.io/hf-espidf-ci-tools/) | CI for ESP-IDF projects with one or many applications, driven by a YAML file. |

All repositories are listed on the [HardFOC organization page](https://github.com/hardfoc). Issues and discussions are welcome there.

## Also public

| Repository | What it is |
|:--|:--|
| [`embedded-linux-primer`](https://github.com/N3b3x/embedded-linux-primer) | Build the whole software stack of an embedded Linux board from source, one small board directory at a time. |
| [`openballbot-rl`](https://github.com/N3b3x/openballbot-rl) | Fork of [salehiac/OpenBallBot-RL](https://github.com/salehiac/OpenBallBot-RL): a MuJoCo ballbot simulator with reinforcement-learning tools for uneven terrain. |
| [`EyeTrackerEmbed`](https://github.com/N3b3x/EyeTrackerEmbed) | Fork of [JEOresearch/EyeTracker](https://github.com/JEOresearch/EyeTracker): a lightweight Python eye tracker. |

## Toolbox

**Languages:** C and C++ (up to C++20), Python and Shell.
**Embedded:** ESP-IDF and RTOS portability layers, CANopen, peripheral drivers, and embedded Linux built from source.
**Engineering practice:** GitHub Actions with reusable workflows, static analysis and linting in CI, generated documentation sites, and design notes kept next to the code.

<sub>Most of my work lives in private repositories, so the public profile is a small slice of it.</sub>
