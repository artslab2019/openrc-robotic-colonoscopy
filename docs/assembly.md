# CAD & Assembly Files

[← Back to README](../README.md)

The full **SolidWorks assembly** of the platform shows every part, how the components mate, and what is needed to reproduce the system. Use it together with the [Bill of Materials](bill-of-materials.md) for the off-the-shelf components and the [Hardware Platform](hardware.md) for the design rationale.

## Files

- **SolidWorks assembly** (`.SLDASM` + part files) of the feeding and bending modules and the phantom molds/stands.
- **STEP (`.STEP`) export** of the assembly, openable without a SolidWorks license.
- **STL files** for the 3D-printable parts (module cages, collets/adaptors/couplers, support plates, phantom base mold, core cap, stands, and clamps).

## Reproducing the build

1. Open the SolidWorks assembly (or the STEP export) to inspect the parts, mates, and overall layout.
2. Export/print the STL parts; source the off-the-shelf components from the [Bill of Materials](bill-of-materials.md).
3. Fabricate the colon phantom following [Colon Phantom Fabrication](phantom-fabrication.md).
