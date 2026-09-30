# Student Performance Predictor
A small classroom project: **Frontend → Flask API → scikit-learn model → AWS EC2**.

It predicts a student's final score from study hours, attendance, and previous score. The dataset is synthetic and this is an educational demo, not a real academic decision system.

## Run locally
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python ml/train_model.py
python backend/app.py
```
Open http://127.0.0.1:5000

Windows PowerShell activation:
```powershell
.venv\Scripts\Activate.ps1
```

## Test API
```bash
curl -X POST http://127.0.0.1:5000/predict -H "Content-Type: application/json" -d '{"study_hours":5,"attendance":85,"previous_score":72}'
```

## Structure
```text
frontend/       HTML/CSS/JavaScript
backend/        Flask API + saved ML model
ml/             training script + synthetic CSV
deployment/     AWS EC2 guide
```
