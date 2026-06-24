# Bill of Materials

[← Back to README](../README.md)

Components used in the OpenRC platform.

The tables below list the off-the-shelf hardware only. Printed mechanical parts are provided as STEP exports in [CAD & Assembly Files](assembly.md) and can be exported to STL as needed.

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

See [CAD & Assembly Files](assembly.md) for the STEP exports used to generate the printed mechanical parts.

## Phantom Materials

| Material | Part / Model | Supplier | Approx. cost | Notes |
|----------|--------------|----------|--------------|-------|
| Colon wall silicone | Ecoflex 00-30 | Smooth-On | ~$33 (2 lb) | Body of the phantom |
| Seam sealant | Ecoflex 00-35 Fast | Smooth-On | ~$40 (trial) | Joins segments |
| Polyp silicone | `TODO` (Smooth-On) | Smooth-On | TODO | Flesh-tone pigmented |
| Mold release | Ease Release 200 | Mann Technologies | ~$19 (12 oz) | |
| Pigment | `TODO` | Smooth-On | TODO | Flesh-tone |
