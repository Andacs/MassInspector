# Changelog

## 1.0.0

- Initial free runtime code plugin targeting Unreal Engine 5.8 and Win64.
- Added a Blueprint-spawnable inspector component with mass, world center, velocity, and simulation snapshots.
- Added mass-weighted actor centers, non-simulating bounds/mass fallback, and welded-body deduplication.
- Added configurable debug points, mass labels, combined center spheres, support traces, and velocity arrows. Overlay geometry draws in the foreground (yellow points, 16 cm cyan spheres, 2.5 px lines) and does not depend on HUD labels.
- Added a console-controlled world overlay (`MassInspector.Show`, `.Labels`, `.MaxBodies`, `.Filter`) with nearest-camera capping, camera-manager/world-origin fallback, paused redraws, and activation logs. Startup values from device profiles and `-DPCVars` are honoured.
- Added Blueprint library queries, physics-independent math, and a center drawing helper.
- Added six guarded `MassInspector.Core.*` automation tests, including Game/PIE overlay regression coverage, plus setup/API documentation.
- Shipping retains data queries and omits debug drawing and console controls (`ENABLE_DRAW_DEBUG`). No content assets or third-party runtime dependencies.
