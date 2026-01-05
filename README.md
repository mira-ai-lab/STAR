# STAR: STRATEGY-AWARE ROURTING FOR MATHEMATICAL REASONING

This project is the official implementation of the paper **"STAR: STRATEGY-AWARE ROURTING FOR MATHEMATICAL REASONING"**.

We propose the **STAR (STrategy-Aware Routing for mathematical reasoning**) framework, which decouples the mathematical reasoning process into two stages: **instance-specific strategy evaluation** and **targeted execution**. The core of STAR is a lightweight Strategy Adapter that can predict the applicability distribution of different inference strategies based on specific problems. During inference, the strategy dynamically selects the optimal execution path based on the predicted confidence level.

## Installation

```bash
conda create -n star python=3.10
conda activate star
pip install -r requirements.txt
```
## Usage

### Data Generation

The script will generate JSON file containing detailed performance metrics (correctness, process quality, efficiency) for each problem policy pair.

```
bash run_benchmark.sh
```

### Inference

Before running inference, please modify the following variables in the scripts `config.py` 

- `base_model`: The basic language model.
- `adapter_path`: The path of the trained strategy adapter model.
- `dataset_paths`:The dataset path.
- `output_dir`: The output directory of the experimental results.
- `tau_c` and `tau_a`.

```
bash run_parallel_experiment.sh
```
