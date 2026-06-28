# Claude Code Context — 3D Prints Repo

## What this repo is

Storage for 3D print files, organised by project. The primary design tool is
[gfthings](https://github.com/PaulBone/gfthings), a Python CLI that generates
[Gridfinity](https://gridfinity.xyz/specification/) storage components.

## Directory layout

```
models/<project>/   STL, 3MF, STEP files + per-project README
prints/<project>/   G-code (machine/slicer-specific)
assets/<project>/   Photos, preview renders
```

## gfthings setup

Install once per session if not already available:

```bash
pip install gfthings
```

Verify:

```bash
gfbin --help
gfbase --help
```

### Key commands

```bash
# Baseplate (desktop — no screws/magnets)
gfbase -x <W> -y <D> --short -o <file>.stl

# Bin
gfbin -x <W> -y <D> -z <H> [options] -o <file>.stl
```

### Gridfinity units

- 1 unit = **42mm**
- `-z` height: each unit ≈ 7mm; minimum is 3 (≈21mm internal)
- Printer: **Bambu Labs X2D** — confirm build volume before generating large baseplates

### Common bin options

| Flag | Effect |
|------|--------|
| `-s 0` / `--scoop 0` | Disable front scoop (for flat/stackable items) |
| `-d N` | N divisions (splits bin into N compartments) |
| `--no-label` | No label shelf |
| `--no-lip` | No stacking lip |
| `--magnet-dia 6` | Magnet hole diameter (default 6mm) |

## Workflow

1. User describes what they want to organise
2. Determine bin dimensions in gridfinity units based on item physical size
3. Run `gfbin` / `gfbase` commands to generate STL files into `models/<project>/`
4. Write a `README.md` in the project folder with commands used and print settings
5. Commit and push

## Projects

### gridfinity-starter

Desktop organiser for craft supplies, Anker MagBak batteries, and portable power banks.
Files in `models/gridfinity-starter/`. See its README for layout and commands.

## Print settings (general defaults)

- Material: PLA or PETG
- Layer height: 0.2mm
- Infill: 15–20%
- Supports: not needed for Gridfinity parts
- Orientation: upright as exported
