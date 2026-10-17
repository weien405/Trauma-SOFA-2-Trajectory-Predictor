# Trauma SOFA-2 trajectory predictor

Streamlit research prototype for early prediction of unfavorable 72-hour SOFA-2 trajectory membership in critically ill patients with trauma.

## Run and deploy

- Streamlit entrypoint: `app.py`
- Required Python version: 3.12
- Frozen model: `model/XGBoost_FINAL_TRAINING_ONLY_PIPELINE.pkl`
- Expected model SHA-256: `ef4917e9dd145e1699d2dac644798ac24fad8f2b67bc5a2fd80b2f2f12479bf1`

Install the pinned dependencies and run:

```text
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

For Streamlit Community Cloud, select the existing GitHub repository, the `main` branch, and `app.py` as the main file path. No secrets are required when the verified model is stored at the repository-relative path above.

## Frozen predictor

The model uses 14 inputs collected by the end of the first 24 hours after ICU admission. It returns the probability of persistent-high or worsening SOFA-2 trajectory membership over 0–72 hours. It does not estimate mortality and does not produce four-class probabilities.

The model, preprocessing parameters, feature order and class direction are frozen. The application verifies the model checksum, the 14-feature order and class order `[0, 1]` before accepting input.

## Scope

Research use only. Not intended for clinical diagnosis or treatment decisions. The model was evaluated in 72-hour landmark-eligible research cohorts and has not been established for all patients admitted to an ICU.

No patient-level MIMIC-IV or eICU-CRD records, credentials or database extracts are included. Do not add patient data to this repository.
