# OV9281 Camera Module 3D Reference Model

![Isometric render of the OV9281 camera module reference model](docs/images/00-isometric-render.png)

A real-size mechanical reference model of the OV9281 camera module used in a four-camera motion-capture system. The model was created to support enclosure design, cage mounting, component-clearance checks, and ribbon-cable routing before working with the physical camera.

## Documentation

This repository documents the reference model through rendered views and physical size-check photographs.

| Documentation | Location |
| --- | --- |
| Rendered reference views | `docs/images/` |
| Physical model comparisons | `docs/images/` |

## Why this model was made

The camera module is part of an indoor drone motion-capture system built around four OV9281 cameras and a Jetson computer. A camera mount cannot be designed from the PCB outline alone: the lens barrel, rear-side components, mounting holes, and ribbon-cable exit all affect the enclosure and the final camera orientation.

This reference model was therefore used as an intermediate mechanical artifact:

1. measure the physical camera module;
2. reproduce its main mechanical features in CAD;
3. print a size-check model;
4. compare the print with the real module from the front, rear, and side;
5. use the verified shape while designing the cage-mounted camera enclosure.

The repository is focused on mechanical integration. It is not an electrical schematic, optical simulation, or manufacturer-certified mechanical drawing.

## Rendered views

| Isometric | Front |
| --- | --- |
| ![Isometric CAD render](docs/images/00-isometric-render.png) | ![Front CAD render](docs/images/01-front-render.png) |

| Rear | Side |
| --- | --- |
| ![Rear CAD render](docs/images/03-rear-render.png) | ![Side CAD render](docs/images/04-side-render.png) |

The views show the PCB outline, mounting-hole locations, lens barrel, rear component volume, and ribbon-cable direction represented in the reference model.

## Physical size check

The printed reference was placed next to the actual camera module to compare the features that matter when designing a housing.

| Front comparison | Rear comparison |
| --- | --- |
| ![Physical front comparison](docs/images/05-front-size-check.jpg) | ![Physical rear comparison](docs/images/06-rear-size-check.jpg) |

### Side and lens-height comparison

![Physical side comparison](docs/images/07-side-size-check.jpg)

These photographs document front, rear, and side fit checks against the physical camera module.

## Intended use

The reference model supports:

- camera enclosure and cover design;
- mounting-bracket and cage-interface design;
- lens and rear-component clearance checks;
- ribbon-cable exit and bend-space planning;
- early fit checks before installing the real camera.

Verify dimensions against your own module before fabrication. Camera-module revisions, lens assemblies, and cable configurations may differ.

## Repository layout

```text
.
|-- README.md
|-- cad/
|   |-- source/       # Editable CAD source area
|   `-- step/         # Neutral STEP exchange area
|-- dimensions/       # Dimension drawings and measurement notes
|-- docs/
|   `-- images/       # Renders and physical comparison photographs
`-- models/
    `-- stl/          # Printable reference model area
```

## Related project

The model was developed while extending a four-camera motion-capture system from camera calibration and tracking to drone position feedback and closed-loop flight experiments.

- [Four-Camera Motion-Capture System — Second Implementation](https://jaypark0115.github.io/jay-tech-notes/pages/planned/03-mocap-second-implementation.html)
- [Jay Tech Notes](https://jaypark0115.github.io/jay-tech-notes/)
