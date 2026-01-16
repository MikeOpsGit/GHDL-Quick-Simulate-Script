# GHDL Quick Simulate Script
A bash script to simplify VHDL simulation using GHDL and GTKWave.

## Description
This script automates the process of importing VHDL files, compiling entities, running simulations, and optionally opening waveform files in GTKWave.

## Usage
To simulate a VHDL testbench:

```bash
./simulate <testbench_file.vhd> [entity_name] [options]
```

Options:
- `-o output_file`: Specify the output waveform file (default: entity.ghw)

- `--no-import`: Skip import VHDL files step (don't run `ghdl -i *.vhd`)

- `-i import_path`: Path to search for VHDL files to import (default: current directory and subdirs)  
  *Note 1: Subdirs will be searched as well in the import_path.*  
  *Note 2: Files are filtered to just files that end with `.vhd`*

- `--no-open`: Do not open the waveform in GTKWave

Run `./simulate` with no arguments to see the full help message.

Example:
```bash
./simulate my_testbench.vhd
```
## Notes
- Only tested on Linux (Ubuntu)
- Requires GHDL and GTKWave to be installed