# CAD & Assembly Files

[← Back to README](../README.md)

The full **SolidWorks assembly** of the platform shows every part, how the components mate, and what is needed to reproduce the system. Use it together with the [Bill of Materials](bill-of-materials.md) for the off-the-shelf components and the [Hardware Platform](hardware.md) for the design rationale.

## Files

- **STEP (`.STEP`) exports** for the feeding and bending modules.

### Bending Module Components

The `CAD/Bending/` folder includes the bending module STEP export [`Bending-Assembly.STEP`](../CAD/Bending/Bending-Assembly.STEP) together with the reference hardware STEP models used by the bending module.

## Reproducing the build

1. Open the STEP export to inspect the parts and overall layout.
2. Export STL parts as needed; source the off-the-shelf components from the [Bill of Materials](bill-of-materials.md).
3. Fabricate the colon phantom following [Colon Phantom Fabrication](phantom-fabrication.md).
