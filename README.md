# zbrush-curve-alpha-plugin.
Curve-based alpha extrusion plugin idea for ZBrush (Python). Transforms grayscale alphas into vector curves with Inflate + Sculptris Pro support.
# Curve-Based Alpha Extrusion Plugin for ZBrush

## Introduction
Traditional alpha maps in ZBrush often produce artifacts when applied to 3D meshes. The pixel-based nature of alphas can lead to jagged edges, uneven extrusion, and mesh distortion. This project proposes a plugin that replaces direct alpha extrusion with a **curve-driven workflow**, enabling cleaner results and adaptive mesh refinement.

## Features
- **Alpha Analysis**  
  Convert grayscale alpha images into vector curves by detecting contours and simplifying them into straight angles with optional smoothing.

- **Curve Generation**  
  Use algorithms (e.g., Douglas–Peucker) to approximate contours and export them as vector paths (SVG or internal ZBrush curve objects).

- **UV Mapping Integration**  
  Project generated curves onto the object’s UV map for precise alignment with mesh topology.

- **Extrusion with Inflate**  
  Apply ZBrush’s Inflate deformation along curve-based masks instead of pixel alphas, producing crisp extrusions.

- **Sculptris Pro Mode Support**  
  Enable dynamic tessellation during extrusion to adapt mesh topology in real time, ensuring sharp, non-broken lines.

## Benefits
- Eliminates jagged artifacts from pixel-based alphas.
- Produces clean, vector-like extrusions.
- Allows adaptive mesh refinement via Sculptris Pro.
- Provides more control over curve smoothing and corner sharpness.

## Technical Notes
- **Language:** Python (ZBrush API).
- **External Libraries:**  
  - OpenCV (image analysis)  
  - NumPy (array operations)  
  - Optional SVG export for curve data
- **Workflow:**  
  1. Preprocess alpha image externally.  
  2. Generate vector curves.  
  3. Import curves into ZBrush.  
  4. Apply Inflate extrusion with Sculptris Pro enabled.

## Example Use Case
1. Artist loads a grayscale alpha (e.g., architectural pattern).
2. Plugin converts alpha into clean vector curves.
3. Curves are projected onto the mesh UV.
4. Inflate extrusion is applied with Sculptris Pro enabled.
5. Result: crisp, geometric embossing without mesh tearing.

## Roadmap
- [ ] Implement alpha-to-curve conversion using OpenCV.
- [ ] Build Python interface with ZBrush API.
- [ ] Add curve smoothing and corner control parameters.
- [ ] Integrate UV projection workflow.
- [ ] Enable Inflate extrusion with Sculptris Pro.
- [ ] Provide GUI for artists inside ZBrush.

## License
MIT License (or choose another license suitable for open-source collaboration).
