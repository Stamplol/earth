# 3D Earth & Geological Structure Explorer (โลก 3 มิติ และโครงสร้างทางธรณีวิทยา)

An interactive, 100% procedural **3D Earth & Internal Geological Structure** web application built with **Three.js (ES Modules)**, **HTML5 OffscreenCanvas**, and **custom GLSL shaders**, featuring a responsive **Thai-language (ภาษาไทย)** educational HUD.

## Key Highlights

- **100% Procedural Visuals (Zero External Textures or 3D Models at Runtime):**
  - Compact inline Polyline-encoded mathematical coastlines, 72 major lakes + Caspian Sea, `-200m/-1000m/-3000m` ocean shelf bathymetry, mountain belts, desert massifs, and ice shelves anchored to Natural Earth `1:50m` physics geometry, layered with a spherical Signed Distance Field, 3D Simplex Noise, `ridgedFbm`, and domain warping.
  - Multi-map `2048×1024` procedural `CanvasTexture` generation: NASA Blue Marble–calibrated Albedo biome map, Tangent-Space Normal map, Roughness map (glossy ocean specular vs. matte land), Night-Side City Lights emissive mask, redesigned `2048×1024` curl-advected synoptic satellite Cloud layer (Rossby fronts, ITCZ convection, trade-wind cumulus, desert clear-sky windows, cloud-top directional relief & cast surface shadows), and `512×256` Milky Way dust band + 4,800-star 3D starfield.
- **Custom GLSL Shaders:**
  - Night-side city lights, twilight terminator blending, and real-time projected cloud shadows on `MeshStandardMaterial`.
  - Cloud-top directional relief self-shadowing and atmospheric scattering glow.
  - Sealed geological cross-sections showing oceanic vs. continental Moho crust thickness contrast, Upper Mantle convection streaks, Lower Mantle high-pressure gradient, animated liquid Outer Core geodynamo turbulence, and pulsing radiant Inner Core.
- **Interactive Exploration Modes:**
  - **Full Globe (`โลกเต็มใบ`)**, **1/8 Octant Cutaway (`ผ่าตัดโครงสร้าง`)**, and **Exploded View (`แยกชั้นโครงสร้าง`)**.
  - Smart click-vs-drag detection, `23.4°` axial tilt rotation, sun angle slider, cloud toggle, direct 3D layer raycasting with hover tooltips, and smooth camera viewport framing.
  - Universe Sandbox–inspired simulation HUD with a top-left telemetry strip, unified bottom control dock, and responsive right-side property inspector (`3×2` layer grid + `40vh` collapsible bottom sheet on mobile) detailing all 5 internal layers in Thai.

## Running Locally

Open `index.html` directly in a modern browser or serve with any static file server (no build tools required):

```bash
python3 -m http.server 8080
```
