# Seismic Core Stencil

Three-dimensional stencil of a seismic core.
This code computes a 3-axis, 16th-order, 49-point stencil.
This optimization project was done for the course "Technique d'optimisation de la Parallélisation" for High Performance Computing master at Paris-Saclay university


## Getting started

### Pre-requisites
- CMake 3.16+
- C17 conforming compiler
- MPI 3.0+ implementation

### Build
```sh
cmake -S . -B <BUILD_DIR> [CMAKE_FLAGS ...]
cmake --build <BUILD_DIR> [-j]
```

### Run
```sh
<BUILD_DIR>/top-stencil [CONFIG_FILE_PATH OUTPUT_FILE_PATH]
```

### Validation
A python script is given to validate the numerical precision of the results and compute the speed up compared to reference results, make sure to use it after every optimisation step to guarentee valid results, an example for tensors of size 100x100x100.

```python
python3 ../scripts/compare.py ../reference/result_100x100x100.txt ../results/result.txt 
```

A detailled PDF report (in french ^^') showcasing all the debbuging, scalability study, optimizing steps and comparative results done for this project is given, Final mark received 17.7/20

