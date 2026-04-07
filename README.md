# Latent Group Alignment for Policy-Guided Behavioral Shift

This repository implements a CLI-based framework for **group-level behavioral alignment** using survey data, with applications to public transport carbon-incentive policies.

The pipeline combines:
- latent representation learning (NMF),
- Shapley-based attribution,
- and optimal transport–based alignment,

to design **minimal, feasible interventions** that shift a target group toward a desired reference group.

---

## 🚀 Usage (CLI)

## 🔹 Multi-seed Configuration

Set mode in:

- `configs/default.yaml`
- `configs/primary_beijing.yaml`

```yaml
mode: "single"   # options: single | multi
```

---

## 📊 Run Experiments

### 1. Beijing Survey (Primary Dataset)

```bash
python main.py --config configs/baselines_beijing.yaml
```

---

### 2. MNIST (Generalization Experiment)

```bash
python main.py --config configs/generalization_mnist.yaml
```

---

### 3. VTA Survey (Generalization Dataset)

```bash
python main.py --config configs/generalization_vta.yaml
```

---

### 4. VTA Adapter Test

```bash
python scripts/test_vta_adapter.py
```

⚠️ Make sure CSV file paths are correctly set before running this script.

---

## 📁 Project Structure

```text
.
├── main.py
├── requirements.txt
├── .gitignore
├── README.md
│
├── configs/
│   ├── ablations.yaml
│   ├── default.yaml
│   ├── generalization_mnist.yaml
│   ├── generalization_mnist_visual.yaml
│   ├── generalization_vta.yaml
│   └── primary_beijing.yaml
│
├── data/
│   ├── raw/
│   ├── interim/
│   └── processed/
│
├── outputs/
├── logs/
│
├── artifacts/
│   ├── generalization_mnist_3_to_8/
│   ├── generalization_vta_q7f/
│   └── logs/
│
├── src/
│   ├── ablations/
│   ├── baselines/
│   ├── core/
│   ├── data/
│   ├── evaluation/
│   ├── features/
│   ├── generalization/
│   ├── intervention/
│   ├── models/
│   ├── utils/
│   └── visualization/
```

## 📌 Notes

- This project is designed as a **CLI-based research pipeline**.
- No notebooks are required to run experiments.
- All inputs, outputs, and configurations are controlled via command-line arguments.
- Results are automatically saved in the `outputs/` directory.

---
