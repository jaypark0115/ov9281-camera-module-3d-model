# OV9281 Camera Module 3D Reference Model

![Isometric render of the OV9281 camera module reference model](docs/images/00-isometric-render.png)

A real-size mechanical reference model of the OV9281 camera module used in a four-camera motion-capture system. The model was created to support enclosure design, cage mounting, component-clearance checks, and ribbon-cable routing before working with the physical camera.

## Project status

This repository currently documents the model through rendered views and physical size-check photographs. The editable CAD source, neutral STEP export, printable STL files, and measured dimension sheet will be added after the design data is prepared for release.

| Item | Status | Planned location |
| --- | --- | --- |
| Rendered reference views | Available | `docs/images/` |
| Physical model comparisons | Available | `docs/images/` |
| Editable CAD source | Coming later | `cad/source/` |
| STEP exchange model | Coming later | `cad/step/` |
| STL reference model | Coming later | `models/stl/` |
| Dimension drawing and measurement notes | Coming later | `dimensions/` |

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

These photographs document the visual fit-check stage. Exact dimensions and tolerances are intentionally not published yet; they will be included with the dimension sheet after the source data is reviewed.

## Intended use

Once the model files are released, this repository is intended to help with:

- camera enclosure and cover design;
- mounting-bracket and cage-interface design;
- lens and rear-component clearance checks;
- ribbon-cable exit and bend-space planning;
- early fit checks before installing the real camera.

Verify the released model against your own module before fabrication. Camera-module revisions, lens assemblies, and cable configurations may differ.

## Repository layout

```text
.
|-- README.md
|-- cad/
|   |-- source/       # Editable CAD source, to be released
|   `-- step/         # Neutral STEP export, to be released
|-- dimensions/       # Dimension drawing and measurement notes, to be released
|-- docs/
|   `-- images/       # Renders and physical comparison photographs
`-- models/
    `-- stl/          # Printable reference model, to be released
```

## Related project

The model was developed while extending a four-camera motion-capture system from camera calibration and tracking to drone position feedback and closed-loop flight experiments.

- [Four-Camera Motion-Capture System — Second Implementation](https://jaypark0115.github.io/jay-tech-notes/pages/planned/03-mocap-second-implementation.html)
- [Jay Tech Notes](https://jaypark0115.github.io/jay-tech-notes/)

## Release notes

There is no downloadable CAD geometry in the current documentation-only release. Future releases will identify the available formats, source-software version, units, revision, and any known dimensional limitations alongside the model files.

