# PyFlow – Mini Data Pipeline (Python Only)

This project builds a simple end-to-end data pipeline using pure Python.
The goal is to read raw CSV data, validate it, transform it, and store clean
and rejected records while collaborating as a team using GitHub.

------------------------------------------------------------

FLOW OF HOW WE WORK

1. The project structure is already created and pushed to the `main` branch.
   The `main` branch is considered stable and must not be pushed to directly.

2. Each team member first clones the repository to their laptop.

   git clone https://github.com/officialgovindnandre7/pyflow_data_pipeline.git
   cd pyflow_data_pipeline

3. Before writing any code, each team member creates their own feature branch
   based on the task assigned to them.

   Examples:
   git checkout -b feature/ingest
   git checkout -b feature/validate
   git checkout -b feature/transform
   git checkout -b feature/load
   git checkout -b feature/logger

4. Each member works only on their assigned file inside the `pipeline` folder.
   No one should change the folder structure or edit other team members’ files.

   ingest.py    → read CSV data
   validate.py  → apply business validation rules
   transform.py → clean and standardize data
   load.py      → write output CSV files
   logger.py    → logging setup

5. After writing code, the member tests it locally by running:

   python main.py

   The code should run without errors.

6. When the work is ready, the member saves the changes to Git locally.

   git status
   git add <assigned_file>
   git commit -m "Implemented <module> logic"

7. The member then pushes ONLY their feature branch to GitHub.

   git push origin feature/<module>

   This does NOT affect the `main` branch.

8. After pushing, the member goes to GitHub and creates a Pull Request (PR).
   The PR compares their feature branch with `main`.

9. The Team Lead reviews the Pull Request, suggests changes if required,
   and merges it into the `main` branch after approval.

10. After a PR is merged, all team members update their local `main` branch.

    git checkout main
    git pull origin main

------------------------------------------------------------

PROJECT STRUCTURE (DO NOT CHANGE)

pyflow_data_pipeline/
|
|-- data/
|   |-- raw/
|   |   |-- users_raw.csv
|   |-- processed/   (auto-created, not pushed to GitHub)
|
|-- pipeline/
|   |-- __init__.py
|   |-- ingest.py
|   |-- validate.py
|   |-- transform.py
|   |-- load.py
|   |-- logger.py
|
|-- main.py
|-- config.py
|-- requirements.txt
|-- README.md
|-- .gitignore

------------------------------------------------------------

PIPELINE FLOW

Raw CSV
→ Ingest
→ Validate
→ Transform
→ Load
→ Clean & Rejected CSV Output

------------------------------------------------------------

IMPORTANT RULES

- No one pushes directly to the `main` branch.
- All changes go through feature branches and Pull Requests.
- Output files and logs are not pushed to GitHub.
- Always pull the latest `main` before starting new work.

------------------------------------------------------------

RESUME STATEMENT

Built an end-to-end data pipeline using pure Python with modular ingestion,
validation, transformation, and loading layers, collaborating via GitHub
using feature branches and pull requests.
