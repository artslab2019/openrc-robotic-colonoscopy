# Colon Phantom Testbed & Fabrication

[← Back to README](../README.md)

![Colon phantom fabrication](../Figures/phantom_fabrication.png)

Because commercial colonoscopy simulators are designed primarily for navigation training and do not contain detectable polyps, we developed a custom silicone colon phantom with **embedded colorectal cancer (CRC) polyps of varying stages**, enabling end-to-end evaluation of both maneuverability and AI-enabled lesion detection. Fabrication proceeds in two stages: forming the polyps, then casting the colon wall with the polyps embedded.

---

## Polyp Fabrication

Polyps were designed to span the **Paris classification** of CRC lesion morphologies.

1. **Rigid masters.** High-resolution polyp masters were printed on a Digital Anatomy Printer (Stratasys J750) in Vero PureWhite to capture fine surface texture.
2. **Negative molds.** Each master was used to cast a negative silicone mold inside a 3D-printed container and cap (Prusa i3 MK3S+, ABS).
3. **Silicone casts.** After demolding, the mold surface was treated with Ease Release 200 (Mann Technologies), then filled with a flesh-tone-pigmented silicone mixture (Smooth-On). This yields the final soft polyps — **11 polyps, labeled P1–P11.**

---

## Colon Phantom Fabrication

The phantom wall is cast using a simple, modular, **unfolded mold** (a flat base mold plus a core cap), avoiding the leakage, complex assembly, and polyp-embedding difficulties of traditional core-based molding. Dimensions follow the reported average human colon (external diameter **D ≈ 60 mm**):

- **Base mold:** nine half-cylinder channels, radius **r = 12.5 mm**, spanning a width **W = 190 mm** (the phantom circumference once wrapped).
- **Core cap:** nine half-cylinders, radius **r = 11 mm**, producing a uniform **1.5 mm wall thickness** against the base mold.

**Process:**

1. Mix Ecoflex 00-30 (Smooth-On, parts A:B = 1:1), pigment flesh-tone, and degas in a vacuum chamber.
2. Dispense ≈ 10 mL into each half-cylinder channel; randomly place the 11 prefabricated polyps on the poured layer (ensuring adhesion while preserving surface texture).
3. Assemble and clamp the core cap to hold the polyps and maintain uniform wall thickness; cure ≈ 4 hours at room temperature.
4. Demold the flat sheet, wrap it around a cylindrical tube, and secure with a holder; seal the seam with Ecoflex 00-35 Fast (Smooth-On) to form a continuous cylinder.
5. Fabricate additional segments and join them with the same procedure to extend length. Each segment is **225 mm** long.

The fully assembled phantom is supported by 3D-printed stands and clamps to form **straight or curved** sections, permanently embedding clinically representative polyps for both navigation and detection studies.
