# Chicago Marathon 2026 Training Block EDA

## Goal
Analyze a 16-week marathon training plan to explore mileage progression,
workout intensity, and long run structure leading into Chicago 2026.

## Project structure
- `training_block_eda.qmd` — main analysis (Quarto, renders to HTML)
- `data/paces.csv` — pace zones with intensity scale (1=easy → 6=mile)
- `data/training.csv` — week-by-week plan (mileage, speed sessions, long runs)

## Data model notes
- Intensity is a numeric scale merged from paces_df onto training_df
- `long_run_intensity = 0` means the long run had no structured pace component
- `speed_total_workout_distance` is derived: n_reps × rep_distance

## Stack
- Python (venv), pandas, matplotlib
- Quarto for rendering (`quarto render training_block_eda.qmd`)
