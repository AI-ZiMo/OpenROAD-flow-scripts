# Qwen Notes

This file contains notes and documentation related to the use of Qwen with the OpenROAD-flow-scripts project.

## Project Initialization

To initialize the OpenROAD-flow-scripts project:

1. Clone the repository with submodules:
   ```bash
   git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts
   cd OpenROAD-flow-scripts
   ```

2. Install dependencies using the setup script (requires sudo):
   ```bash
   sudo ./setup.sh
   ```
   This script handles:
   - Initializing submodules if needed
   - Installing base dependencies
   - Installing common dependencies in the project's `dependencies` directory

3. Build the project:
   ```bash
   ./build_openroad.sh --local
   ```

4. Verify the installation by sourcing the environment and running basic commands:
   ```bash
   source ./env.sh
   yosys -help
   openroad -help
   ```

5. Test the flow with a simple design:
   ```bash
   cd flow
   make
   ```
   This runs the complete flow from RTL to GDSII for the default 'gcd' design using the 'nangate45' PDK.

## Additional Resources

- [OpenROAD-flow-scripts Documentation](https://openroad-flow-scripts.readthedocs.io/en/latest/)
- [Build Locally Guide](./docs/user/BuildLocally.md)
- [Flow Tutorial](https://openroad-flow-scripts.readthedocs.io/en/latest/tutorials/FlowTutorial.html)