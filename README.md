# Rockone Drone

Rocket-shaped drone with single central propeller.

## Project Structure

```
rockone/
├── cad/                    # CAD models
│   ├── components/         # Individual parts
│   │   ├── propeller/     # Propeller assembly
│   │   ├── motor_mount/   # Motor mounting structure
│   │   ├── duct_system/   # Aerodynamic duct and vanes
│   │   └── fuselage/      # Main body
│   │
│   └── assemblies/         # Assembled systems
│       └── rockone.FCStd   # Complete drone assembly
│
├── analysis/               # Engineering analysis
│   ├── fem/               # Finite element analysis
│   │   ├── propeller/     # Propeller structural analysis
│   │   └── assembly/      # Full assembly FEM
│   │
│   └── cfd/               # Computational fluid dynamics
│       ├── propeller/     # Isolated propeller CFD
│       └── full_aircraft/ # Complete aircraft CFD
│
└── scripts/               # Automation and utilities
    └── *.py               # Python scripts for design automation
```

## Git Workflow

```bash
# Clone
git clone https://github.com/kasattejaswi/cad-rockone.git
cd cad-rockone

# Create feature branch
git checkout -b feature/propeller-design

# Commit changes
git add .
git commit -m "Add initial propeller geometry"
git push origin feature/propeller-design

# Create pull request
```

## FreeCAD Setup

### Required Workbenches
- Part Design
- Part
- Sketcher
- Assembly 4 (recommended)
- FEM
- CFD

### Component Files
Each component is stored in a separate FreeCAD file:
- `cad/components/propeller/propeller.FCStd`
- `cad/components/motor_mount/motor_mount.FCStd`
- `cad/components/duct_system/duct.FCStd`
- `cad/components/fuselage/fuselage.FCStd`

### Assembly
The complete drone is assembled in:
- `cad/assemblies/rockone.FCStd`

Uses `App::Link` to reference component files.

## Development Process

See [cad-workflow](https://github.com/kasattejaswi/cad-workflow) for detailed workflow documentation.
