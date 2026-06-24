# Bill of Materials

[← Back to README](../README.md)

Components used in the OpenRC platform.

The tables below list the off-the-shelf hardware, reference hardware, and printable STL parts. Refer to [`Feeder-Assembly-V3.STEP`](../CAD/Feeding/STEP/Feeder-Assembly-V3.STEP) and [`Bending-Assembly.STEP`](../CAD/Bending/STEP/Bending-Assembly.STEP) to see how the parts come together.

## Actuation & Control

| Component | Part / Model | Qty | Supplier | Approx. cost | Notes |
|-----------|--------------|-----|----------|--------------|-------|
| Servo motor (bending) | DYNAMIXEL XM540-W270-R | 2 | ROBOTIS (South Korea) | ~$495 ea | 1:270 gearbox, 12-bit absolute encoder, 0.088° output resolution; drives the steering knobs |
| Servo motor (feeding) | DYNAMIXEL XM430-W350-R | 1 | ROBOTIS (South Korea) | ~$335 | 1:350 gearbox, 12-bit absolute encoder, 0.088° resolution; drives the spline shaft |
| Serial controller | DYNAMIXEL U2D2 | 1 | ROBOTIS (South Korea) | ~$35 | USB ↔ RS-485 bridge |
| Motor bus | RS-485 daisy chain | 1 | ROBOTIS (South Korea) | ~$10 | Connects the three servos to the U2D2 |
| Onboard compute | NVIDIA Jetson Orin Nano Super (8 GB) | 1 | NVIDIA | ~$249 | Runs the ROS2 stack |
| Teleop input | Xbox 360 controller | 1 | Microsoft | ~$30 | |

## Imaging

| Component | Part / Model | Qty | Supplier | Approx. cost | Notes |
|-----------|--------------|-----|----------|--------------|-------|
| Colonoscope | PENTAX EC-3840LK | 1 | PENTAX Medical | quote (clinical) | Unmodified clinical scope; refurbished-market price varies |
| Video processor & light source | EPM-3300 | 1 | PENTAX Medical | quote (clinical) | Refurbished-market price varies |
| Frame grabber | Video to USB 1080P Capture device | 1 | ClearClick (USA) | ~$70 | Digitizes the video output |

## Sensing

| Component | Part / Model | Qty | Supplier | Approx. cost | Notes |
|-----------|--------------|-----|----------|--------------|-------|
| EM tracker | NDI Aurora | 1 | Northern Digital Inc. | quote (OEM) | 6-DoF distal-tip pose; sold as an OEM solution, price on request |

## Mechanical / Structure

### Purchased / Reference Mechanical Components

| Component | Part / Model | Qty | Supplier | Buy link | Notes |
|-----------|--------------|-----|----------|----------|-------|
| Feeding lead screw | 97783A170 | 1 | McMaster-Carr | [97783A170](https://www.mcmaster.com/97783A170/) | 100 mm lead screw; CAD reference in [`100mm-Lead Screw_97783A170.STEP`](../CAD/Feeding/STEP/100mm-Lead%20Screw_97783A170.STEP) |
| Feeding ball bearing | 7804K117 | 1 | McMaster-Carr | [7804K117](https://www.mcmaster.com/7804K117/) | Stainless steel ball bearing; CAD reference in [`7804K117_Stainless Steel Ball Bearing_7804K117.STEP`](../CAD/Feeding/STEP/7804K117_Stainless%20Steel%20Ball%20Bearing_7804K117.STEP) |
| Bending compression spring | 2006N518 | 1 | McMaster-Carr | [2006N518](https://www.mcmaster.com/2006N518/) | 302 stainless steel corrosion-resistant compression spring; CAD reference in [`2006N518_302 Stainless Steel Corrosion-Resistant Compression Springs_2006N518.STEP`](../CAD/Bending/STEP/2006N518_302%20Stainless%20Steel%20Corrosion-Resistant%20Compression%20Springs_2006N518.STEP) |
| Bending plastic sliding bearing | GSM-4448-16 | 2 | igus | [GSM-4448-16 search](https://www.igus.com/search?q=GSM-4448-16) | Plastic sliding bearing; CAD reference in [`GSM_4448_16_2.STEP`](../CAD/Bending/STEP/GSM_4448_16_2.STEP) |

### Feeding Module STL Exports

| Component | STL file |
|-----------|----------|
| Actuation module assembly | [`feeding-actuation-module.stl`](../CAD/Feeding/STL/feeding-actuation-module.stl) |
| Base plate | [`feeding-base-plate.stl`](../CAD/Feeding/STL/feeding-base-plate.stl) |
| Top plate | [`feeding-top-plate.stl`](../CAD/Feeding/STL/feeding-top-plate.stl) |
| Side plate | [`feeding-side-plate.stl`](../CAD/Feeding/STL/feeding-side-plate.stl) |
| End support, left | [`feeding-end-support-left.stl`](../CAD/Feeding/STL/feeding-end-support-left.stl) |
| End support, mid | [`feeding-end-support-mid.stl`](../CAD/Feeding/STL/feeding-end-support-mid.stl) |
| End support, right | [`feeding-end-support-right.stl`](../CAD/Feeding/STL/feeding-end-support-right.stl) |
| Half bearing, 1 | [`feeding-half-bearing-1.stl`](../CAD/Feeding/STL/feeding-half-bearing-1.stl) |
| Half bearing, 2 | [`feeding-half-bearing-2.stl`](../CAD/Feeding/STL/feeding-half-bearing-2.stl) |
| Motor coupler | [`feeding-motor-coupler.stl`](../CAD/Feeding/STL/feeding-motor-coupler.stl) |
| Coupler | [`feeding-coupler.stl`](../CAD/Feeding/STL/feeding-coupler.stl) |
| Nut connector | [`feeding-nut-connector.stl`](../CAD/Feeding/STL/feeding-nut-connector.stl) |
| Spline nut, 1 | [`feeding-spline-nut-1.stl`](../CAD/Feeding/STL/feeding-spline-nut-1.stl) |
| Spline nut, 2 | [`feeding-spline-nut-2.stl`](../CAD/Feeding/STL/feeding-spline-nut-2.stl) |
| Spline shaft | [`feeding-spline-shaft.stl`](../CAD/Feeding/STL/feeding-spline-shaft.stl) |
| Cap | [`feeding-cap.stl`](../CAD/Feeding/STL/feeding-cap.stl) |

### Bending Module STL Exports

| Component | STL file |
|-----------|----------|
| Motor cage, S | [`bending-motor-cage-s.stl`](../CAD/Bending/STL/bending-motor-cage-s.stl) |
| Motor cage, variant | [`bending-motor-cage-2.stl`](../CAD/Bending/STL/bending-motor-cage-2.stl) |
| Motor coupling | [`bending-motor-coupler.stl`](../CAD/Bending/STL/bending-motor-coupler.stl) |
| Collet, 1 | [`bending-collet-1.stl`](../CAD/Bending/STL/bending-collet-1.stl) |
| Collet, 2 | [`bending-collet-2.stl`](../CAD/Bending/STL/bending-collet-2.stl) |
| Adaptor, 1 | [`bending-adaptor-1.stl`](../CAD/Bending/STL/bending-adaptor-1.stl) |
| Adaptor, 2 | [`bending-adaptor-2.stl`](../CAD/Bending/STL/bending-adaptor-2.stl) |
| Coupling, 1 | [`bending-coupling-1.stl`](../CAD/Bending/STL/bending-coupling-1.stl) |
| Coupling, 2 | [`bending-coupling-2.stl`](../CAD/Bending/STL/bending-coupling-2.stl) |
| Coupling, 3 | [`bending-coupling-3.stl`](../CAD/Bending/STL/bending-coupling-3.stl) |

## Phantom Materials

| Material | Part / Model | Supplier | Approx. cost | Notes |
|----------|--------------|----------|--------------|-------|
| Colon wall silicone | Ecoflex 00-30 | Smooth-On | ~$33 (2 lb) | Body of the phantom |
| Seam sealant | Ecoflex 00-35 Fast | Smooth-On | ~$40 (trial) | Joins segments |
| Polyp silicone | `TODO` (Smooth-On) | Smooth-On | `TODO` | Flesh-tone pigmented |
| Mold release | Ease Release 200 | Mann Technologies | ~$19 (12 oz) | |
| Pigment | `TODO` | Smooth-On | `TODO` | Flesh-tone |
