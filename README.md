# Offline Reinforcement Learning Codebase

This repository contains the **ASPC** algorithm and several baseline offline RL algorithms (WPC, IQL, TD3+BC, ReBRAC, etc.).

Paper homepage: https://ojs.aaai.org/index.php/AAAI/article/view/38924  
Venue: **AAAI 2026 (Oral)**

---

## Environment Setup

The environment dependencies are specified in `environment.yml`, which will create a Conda environment named **mujo** and install necessary packages such as `d4rl`.

```bash
# 1) Create and activate the environment
conda env create -f environment.yml
conda activate mujo
```

---

## Running the Code

Navigate to the algorithm directory and run:

```bash
cd algorithms/offline

# Run ASPC on HalfCheetah-medium-v2
python aspc.py --env=halfcheetah-medium-v2
```

You can replace `aspc.py` with other algorithm scripts, for example:

```bash
python wpc.py --env=halfcheetah-medium-v2
python iql.py --env=hopper-medium-v2
python td3_bc.py --env=walker2d-medium-v2
python rebrac.py --env=antmaze-medium-play-v2
```

Similarly, replace `--env` with any supported D4RL environment name to train on different tasks.

---

## Acknowledgments

This repository builds upon and references code from the following GitHub repositories:

1. [CORL](https://github.com/tinkoff-ai/CORL)  
2. [wPC](https://github.com/qsa-fox/wPC)  
3. [TorchOpt](https://github.com/metaopt/torchopt)

---

## License

This repository uses **Apache License 2.0** for original ASPC contributions.

Some files are adapted from third-party projects and remain under their original licenses (Apache-2.0 or MIT).  
See `THIRD_PARTY_LICENSES` and `NOTICE` for attribution and full third-party license texts.
