# Atomiq Hackathon – Hybrid Quantum-Classical Term Deposit Campaign Pipeline

**Team:** Luisa Pegoraro, Jiya Maurya

**Final answer:** six customers to contact, and P(at least 3 subscribe) = _TBD_

## Pipeline

| Stage        | Notebook                          | Input                                                                       | Output                       |
| ------------ | --------------------------------- | --------------------------------------------------------------------------- | ---------------------------- |
| 1 – Predict  | `notebooks/stage1_predict.ipynb`  | `data/Stage1_Train`, `data/Stage1_Test`                                     | `results/stage1_results.csv` |
| 2 – Select   | `notebooks/stage2_select.ipynb`   | `results/stage1_results.csv`, `data/Stage2_Data`, `data/Stage2_Constraints` | `results/stage2_results.csv` |
| 3 – Simulate | `notebooks/stage3_simulate.ipynb` | `results/stage2_results.csv`                                                | `results/stage3_results.csv` |

### Handoff file contract (Stage 1 → 2)

`results/stage1_results.csv` must have the columns:
`customer_id, probability, rank, top10_flag`

Until Stage 1 is done, run `python src/make_fake_stage1.py` to create a placeholder so Stages 2–3 can be developed in parallel.

## Who owns what

- **Stage 1:** _name_
- **Stages 2–3:** _name_
- **README / report / presentation:** both

Edit only the notebooks you own, to avoid merge conflicts.

## How to run

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
# put the organizers' data files in data/
jupyter lab
```

Run the notebooks in order: Stage 1 → 2 → 3.

## Reproducibility

- Global seed: `SEED = 42` (set in `src/config.py`)
- Simulator: Qiskit Aer `AerSimulator`, shots: _TBD_
- Package versions: see `requirements.txt` (record `pip freeze` output before submitting)

## Results

_TBD: summary of each stage, classical vs quantum comparison, error analysis, limitations, business recommendation._
