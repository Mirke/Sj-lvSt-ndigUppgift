# Självständig uppgift - Mikael Eriksson

```powershell
# Clone repository
git clone https://github.com/edbeeching/godot_rl_agents.git

# Change directory 
cd godot_rl_agents

# Create a Python virtual environment
python -m venv .venv

# Activate the virtual environment
& .\.venv\Scripts\Activate.ps1

# Install the godot-rl package
pip install godot-rl

# Install the godot_rl_agents package from the GitHub archive
pip install https://github.com/edbeeching/godot_rl_agents/archive/refs/heads/main.zip

# Install the development dependencies
pip install -e ".[dev]"

# Download the example environment from the hub
gdrl.env_from_hub -r edbeeching/godot_rl_BallChase

# Clear the screen
clear

# Run the first example with visualization
python examples/stable_baselines3_example.py --env_path=examples/godot_rl_BallChase/bin/BallChase.x86_64 --experiment_name=Experiment_01 --viz

# Run the second example with a speedup and visualization
python examples/stable_baselines3_example.py --env_path=examples/godot_rl_BallChase/bin/BallChase.x86_64 --experiment_name=Experiment_02 --speedup=10 --viz

# Run the third example with a speedup (no visualization)
python examples/stable_baselines3_example.py --env_path=examples/godot_rl_BallChase/bin/BallChase.x86_64 --experiment_name=Experiment_03 --speedup=10

# Start TensorBoard
tensorboard --logdir .\examples\sb3

# Open TensorBoard in the browser
Start-Process http://localhost:6006
```
