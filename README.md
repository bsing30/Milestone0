# Milestone 0 - Environment & CI Setup

![CI](https://github.com/bsing30/Milestone0/actions/workflows/ci.yml/badge.svg)

## Setup Steps (Windows PowerShell)

### 1) Clone the repository
```powershell
git clone https://github.com/bsing30/Milestone0.git
cd Milestone0
```
### 2) Create and activate a virtual environment
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```
### 3) Install dependencies
```powershell
pip install -r requirements.txt
```
### 4) Run the smoke test
```powershell
pytest -q
```
## Reproducibility:-
Environment reproducibility is essential in the ML lifecycle because models must run reliably across development, testing, and deployment environments. If package versions or Python environments change, the same code can produce different results or fail completely, creating the “it works on my machine” problem. To prevent this, this project pins dependencies to exact versions in requirements.txt, so anyone can recreate the same environment and get consistent behavior.

This milestone applies reproducibility principles such as dependency pinning, isolated virtual environments, and automated validation through CI. The GitHub Actions workflow installs the dependencies inside a clean runner and executes a simple smoke test using pytest to confirm the environment works from scratch. This helps detect setup issues early and reduces risk before deployment. In real MLOps workflows, environment management supports deployment success by keeping the runtime consistent between training, testing, and production systems, improving reliability and preventing failures caused by mismatched dependencies.










