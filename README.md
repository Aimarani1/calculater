# calculator-project

A tiny Python calculator (add, subtract, multiply, divide) with automated
tests and a GitHub Actions CI pipeline that runs the tests on every push
and pull request to `main`.

## Folder structure

```
calculator-project/
├── calculator.py
├── test_calculator.py
├── requirements.txt
├── README.md
├── .gitignore
└── .github/
    └── workflows/
        └── ci.yml
```

## Run locally

You need Python 3.11 or newer installed.

```bash
# 1. Go into the project folder
cd calculator-project

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the tests
pytest -v
```

You should see 5 tests pass.

## Push to GitHub and see CI run

1. Create a new empty repository on GitHub (no README, no .gitignore).
2. In the project folder, run:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/calculator-project.git
git push -u origin main
```

3. Open your repository on GitHub and click the **Actions** tab.
4. You will see the **Python CI** workflow running. A green check means
   all tests passed; a red X means something failed (click it to see why).
