# 3D Prints

A repository for storing 3D print files, organized by project.

## Directory Structure

```
models/
  <project-name>/
    *.stl / *.3mf / *.obj    # print-ready files
    *.step / *.f3d / *.scad  # source/editable files
    README.md                 # print settings, notes
prints/
  <project-name>/
    *.gcode                   # sliced files (machine-specific)
assets/
  <project-name>/
    *.png / *.jpg             # photos, previews
```

## File Types

| Extension | Type | Notes |
|-----------|------|-------|
| `.stl` | Mesh | Universal, most slicer-compatible |
| `.3mf` | Mesh | Preferred — carries color, scale, orientation |
| `.step` | CAD source | Editable in Fusion 360, FreeCAD, etc. |
| `.f3d` | Fusion 360 source | Native Fusion 360 format |
| `.scad` | OpenSCAD source | Parametric, text-based |
| `.gcode` | Sliced | Machine-specific; include slicer settings in filename or README |

## Naming Convention

`<descriptive-name>_v<version>.<ext>`

Example: `phone-stand_v2.stl`
