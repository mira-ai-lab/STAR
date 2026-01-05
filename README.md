# PRISM:PROBLEM-AWARE STRATEGY ROUTING FOR MATHEMATICAL REASONING WITH LLMS

This project is the official implementation of the paper“Plan Before Solving: Problem-Aware Strategy Routing for Mathematical Reasoning with LLMs” .

We propose the **PRISM (Planning and Routing through Instance Specific Modeling)** framework, which decouples the mathematical reasoning process into two stages: **policy planning** and **target execution**. The core of PRISM is a lightweight Strategy Adapter that can predict the applicability distribution of different inference strategies based on specific problems. During inference, the strategy dynamically selects the optimal execution path based on the predicted confidence level.

## 🚀Getting Start

### 1.Create a virtual environment

```
conda create -n prism python=3.10
conda activate prism
```

### 2.Install dependencies

```
pip install -r requirements.txt
```

### 3.Data Generation

The script will generate JSON file containing detailed performance metrics (correctness, process quality, efficiency) for each problem policy pair.

```
bash run_benchmark.sh
```

### 4.Inference

Before running inference, please modify the following variables in the scripts `config.py` 

- `base_model`: The basic language model.
- `adapter_path`: The path of the trained strategy adapter model.
- `dataset_paths`:The dataset path.
- `output_dir`: The output directory of the experimental results.
- `tau_c` and `tau_a`.

```
bash run_parallel_experiment.sh
```

## 📑Citation

If your research uses the PRISM framework or our dataset, please cite our paper.

```
@misc{qi2025plansolvingproblemawarestrategy,
      title={Plan before Solving: Problem-Aware Strategy Routing for Mathematical Reasoning with LLMs}, 
      author={Shihao Qi and Jie Ma and Ziang Yin and Lingling Zhang and Jian Zhang and Jun Liu and Feng Tian and Tongliang Liu},
      year={2025},
      eprint={2509.24377},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2509.24377}, 
}
```

