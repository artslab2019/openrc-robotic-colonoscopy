# Hardware Platform

[← Back to README](../README.md)

> For the full analytical design, parameter-optimization spaces, and mechanical fabrication of the feeding and bending modules, see the companion paper [arXiv:2509.10735](https://arxiv.org/abs/2509.10735). The summary below is intended as a platform-level overview. For part numbers and quantities see the [Bill of Materials](bill-of-materials.md); for STEP assembly exports and printable STL files see [CAD & Assembly Files](assembly.md).

OpenRC is organized into four interconnected subsystems:

1. **Control System** — operator interface and onboard compute.
2. **Robotic System** — the clip-on actuation hardware (feeding + bending modules).
3. **Video Capture** — clinical imaging chain and frame acquisition.
4. **Environment & Sensing** — the colon phantom and electromagnetic tip tracking.

---

## Control System

Teleoperation is handled by a standard **Xbox controller**, with real-time control and data logging running onboard an **NVIDIA Jetson Orin Nano Super**. A graphical user interface displays the live endoscopic feed and system state. Motor commands are dispatched from the Jetson through a **DYNAMIXEL U2D2** (USB ↔ RS-485 bridge) to the three servos, which are wired as an **RS-485 daisy chain** (ROBOTIS, South Korea).

| Input | Action |
|-------|--------|
| `R2` (right trigger) | Retraction |
| `L2` (left trigger) | Insertion |
| Analog stick | Bending (steering, X/Y) |
| `L3` (stick press) | Reset / home |

The ROS2 software stack that ties these nodes together is documented separately in [Software & ROS2 Stack](software.md).

---

## Robotic System

The robotic system is a retrofit: it clamps onto an unmodified colonoscope and drives the same insertion tube and control knobs a clinician would operate by hand. It comprises two decoupled modules.

### Feeding Module

![Feeding module design](../Figures/feeding_module.png)

The feeding module provides the single insertion/retraction degree of freedom. A single **DYNAMIXEL XM430-W350-R** servo (1:350 gearbox, 12-bit absolute encoder, 0.088° resolution) drives a **spline shaft** coupled to a **feeder-roller** that grips the insertion tube, while an opposing **idler-ball guide** maintains contact pressure and keeps the tube aligned as it is advanced or withdrawn. The module is packaged in a compact rigid cage (≈ 150 × 90 × 38 mm) that mounts at the scope entry point.

![Assembled feeding module](../Figures/feeding.png)

*The fabricated feeding module: a motor drives the spline shaft through a flexible coupling, advancing the colonoscope's insertion tube. The X/Y/Z axes denote the local tip frame.*

### Bending Module

![Bending module design](../Figures/bending_module.png)

The bending module actuates the scope's steering (knob) degrees of freedom using a **nested collet-chuck** design. Concentric collets and couplers grip the existing up/down and left/right steering knobs without modification, and two gear-driven **DYNAMIXEL XM540-W270-R** servos (1:270 gearbox, 12-bit absolute encoder, 0.088° output resolution) — commanded through the U2D2 — rotate them to deflect the distal tip. This preserves the native tendon-driven steering mechanism of the scope while making it programmatically controllable.

![Assembled bending module](../Figures/bending.png)

*The fabricated bending module: nested collets (Collet-1/2) and adaptors/couplers clamp onto the concentric steering knobs, while servo motors drive them through a gear train to deflect the distal tip.*

---

## Video Capture

Imaging uses the clinical chain end-to-end: the scope's optics are illuminated and processed by a PENTAX **EPM-3300** video processor & light source, whose output is digitized by a **ClearClick Video-to-USB 1080P capture device** (ClearClick, USA) and streamed to the compute unit. The endoscopic video is captured at **383 × 396 resolution, 30 fps**.

---

## Environment & Sensing

Distal-tip localization is provided by an **NDI Aurora electromagnetic (EM) tracker**, yielding 6-DoF tip pose (position + orientation) co-registered with the video and actuation streams. The robotized scope is exercised against a custom **colon phantom** with embedded polyps — see [Colon Phantom Fabrication](phantom-fabrication.md).
