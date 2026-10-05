# CampusFix AI — Public Deployment

## Local run
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python app.py

## Render deployment
1. Upload this folder to a GitHub repository.
2. On Render, create a Web Service and connect the repository.
3. Build command: `pip install -r requirements.txt`
4. Start command: `gunicorn app:app`
5. Choose a free plan for a hackathon demo.

Important: this version uses SQLite. On Render's default ephemeral filesystem, complaint data can be lost after a restart/redeploy. For persistent production data, move to Postgres or use a paid persistent disk.
