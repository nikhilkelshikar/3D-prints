# Gridfinity Starter Set

Desktop organizer for craft supplies, Anker MagBak batteries, and portable power banks.
Generated with [gfthings](https://github.com/PaulBone/gfthings) v0.8.0.

## Files

| File | Description | Dimensions |
|------|-------------|------------|
| `baseplate_5x4.stl` | Desktop baseplate (short/no screws) | 210 × 168 mm |
| `pen-holder_1x4.stl` | Pens/markers lying horizontal, scoop front | 42 × 168 mm, ~28mm tall |
| `craft-misc_2x2_3div.stl` | 3-division bin for small craft supplies | 84 × 84 mm, ~35mm tall |
| `magbak-batteries_2x2.stl` | Flat tray for MagBak batteries | 84 × 84 mm, ~21mm tall |
| `powerbanks_2x3.stl` | Bin for Li-ion power banks | 84 × 126 mm, ~35mm tall |

## Layout on 5×4 baseplate

```
 1    2    3    4    5
+----+----+----+----+----+  y=1
|    | MagBak 2x2  |    |
| 1x4+-----------+ |    |  y=2
|    | craft  | PB |    |
| pen| 2x2    | 2x3|    |  y=3
|    | 3div   |    |    |
+----+----+----+----+----+  y=4
```

Rough arrangement — mix and match bins freely, Gridfinity snaps anywhere on the grid.

## Print Settings

- **Material:** PLA or PETG
- **Layer height:** 0.2mm
- **Infill:** 15–20%
- **Supports:** None needed
- **Orientation:** Print upright (as oriented in STL)

## gfthings Commands

```bash
# Baseplate
gfbase -x 5 -y 4 --short -o baseplate_5x4.stl

# Bins
gfbin -x 1 -y 4 -z 4 -s 15 -o pen-holder_1x4.stl
gfbin -x 2 -y 2 -z 5 -d 3 -o craft-misc_2x2_3div.stl
gfbin -x 2 -y 2 -z 3 --scoop 0 --no-label -o magbak-batteries_2x2.stl
gfbin -x 2 -y 3 -z 5 --scoop 0 --no-label -o powerbanks_2x3.stl
```
