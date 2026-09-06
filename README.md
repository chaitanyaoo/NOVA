# NOVA

Team productivity platform — create projects, add tasks, bring in team members
and track progress. Built for the full-stack intern assignment.

## Stack

- Backend: Python (Flask), SQLAlchemy, SQLite
- Auth: JWT (PyJWT), passwords hashed with werkzeug
- Frontend: plain HTML/CSS/JS, no build step
- Deployment: Docker / docker-compose

## Running with Docker (recommended)

```
docker-compose up --build
```

Then open http://localhost:5000. The SQLite database lives in `./data/nova.db`
on the host, so your data survives container restarts.

## Running without Docker

```
cd backend
python -m venv venv
source venv/bin/activate      # venv\Scripts\activate on Windows
pip install -r requirements.txt
python app.py
```

Open http://localhost:5000.

## How it works

- Register an account, then create a project — you become its owner.
- Add teammates to a project by their account email (they need to have
  registered already).
- Add tasks and move them between To do / In progress / Done using the
  dropdown on each task card.
- Project progress is just done tasks / total tasks, shown as a bar on the
  dashboard and on the project page.
- Only the project owner can add/remove members or delete the project.

