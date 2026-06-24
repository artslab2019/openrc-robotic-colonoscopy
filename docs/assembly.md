# CAD & Assembly Files

[← Back to README](../README.md)

The released CAD package provides STEP assembly exports and STL files for the printable parts. Use it together with the [Bill of Materials](bill-of-materials.md) for the off-the-shelf components and the [Hardware Platform](hardware.md) for the design rationale.

## Files

- **STEP (`.STEP`) assembly exports** for the feeding and bending modules.
- **STL (`.stl`) files** for the printable feeding and bending module parts.

## Assembly References

- Feeding module: [`Feeder-Assembly-V3.STEP`](../CAD/Feeding/STEP/Feeder-Assembly-V3.STEP)
- Bending module: [`Bending-Assembly.STEP`](../CAD/Bending/STEP/Bending-Assembly.STEP)

## Reproducing the build

1. Open the STEP assembly export to inspect how the parts fit together.
2. Print the STL parts; we printed the parts in PLA.
3. Source the off-the-shelf components from the [Bill of Materials](bill-of-materials.md).
4. Fabricate the colon phantom following [Colon Phantom Fabrication](phantom-fabrication.md).
