# Atum Senet

This repository contains a single Jupyter notebook (`senet.ipynb`) that trains an AI agent to play the ancient Egyptian board game **Senet** using an evolutionary (genetic) algorithm and an adaptive opponent curriculum.

## Contents

- `senet.ipynb` — end-to-end training notebook, including evaluation and experiment logging.
- `LICENSE` — MIT license.

## Requirements

The notebook installs its Python dependencies in the first cell:

- Python 3
- `numpy`, `matplotlib`, `pyrsistent`, `wandb`

The notebook also relies on the Senet game engine modules (for example: `ai_pruning`, `game_state_pyrsistent`, `board`, `rules_silent`, `sticks`) which are expected to be available on the path.

> **Note:** The current notebook assumes a Kaggle-style path: `/kaggle/input/senet-files`.

## Running the notebook

1. Open `senet.ipynb` in Jupyter or Kaggle.
2. Make sure the Senet engine modules are available and update the `sys.path.append(...)` line if your path differs.
3. Configure Weights & Biases logging by setting `WANDB_API_KEY` or running `wandb login` (avoid hardcoding keys in the notebook).
4. Run all cells to start training.

## Outputs

Depending on which sections you enable, the notebook can produce:

- Checkpoints under `/kaggle/working/checkpoints`
- Training curves and artifacts logged to Weights & Biases
- Final model weights exported as JSON

## License

MIT — see [LICENSE](LICENSE).
