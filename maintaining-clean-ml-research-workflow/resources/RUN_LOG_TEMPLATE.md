# Run Log: [Run ID]

## Meta
- **Date**: [YYYY-MM-DD HH:MM:SS]
- **Goal**: [What hypothesis are you testing?]
- **Status**: [Success/Failure/In-Progress]

## Configuration
- **Command**: `python main.py --config configs/exp1.json`
- **Parameters**:
  - `learning_rate`: 0.001
  - `model`: "llama-3-8b"
- **Environment Snapshot**: `runs/[run_id]/env_snapshot.txt`

## Results
- **Metrics**:
  - Accuracy: 0.95
  - Loss: 0.02
- **Artifacts**:
  - Plots: `runs/[run_id]/plots/`
  - Model: `runs/[run_id]/model.pt`

## Analysis
- **Observation**: [What happened?]
- **Conclusion**: [Does this support the hypothesis?]
- **Next Steps**: [What to try next?]
