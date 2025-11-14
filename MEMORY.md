# Session Context: Python Spreadsheet Environment

**Last Updated:** 2025-11-13
**User:** mattnovis
**Project:** Agentwork Spreadsheet Environment

---

## Project Overview

Python environment for working with Excel and CSV spreadsheets using pandas, openpyxl, and xlrd libraries. The environment uses Python 3.9 with a virtual environment setup matching the Operating Budget project configuration.

---

## System Information

- **OS:** macOS (Darwin 24.0.0)
- **Shell:** zsh
- **Home Directory:** `/Users/mattnovis`
- **Python Version:** 3.9.6 (from Command Line Tools)
- **Homebrew Version:** 5.0.1
- **Homebrew Location:** `/opt/homebrew`

---

## Project Directory Structure

```
/Users/mattnovis/agentwork/
├── venv/                       # Python 3.9 virtual environment
│   ├── bin/
│   │   ├── activate           # Activation script
│   │   └── python             # Python 3.9
│   └── lib/
└── MEMORY.md                   # This file - session state/context
```

---

## Installed Python Packages

All packages installed in the virtual environment at:
`/Users/mattnovis/agentwork/venv`

| Package | Version | Purpose |
|---------|---------|---------|
| pandas | 2.3.3 | Data manipulation and analysis |
| openpyxl | 3.1.5 | Reading/writing Excel .xlsx files |
| xlrd | 2.0.2 | Reading older .xls Excel files |
| numpy | 2.0.2 | Numerical computing (pandas dependency) |
| python-dateutil | 2.9.0.post0 | Date/time utilities |
| pytz | 2025.2 | Timezone definitions |
| tzdata | 2025.2 | Timezone data |
| et-xmlfile | 2.0.0 | XML file handling (openpyxl dependency) |
| six | 1.17.0 | Python 2/3 compatibility |

---

## Configuration Files

### Shell Configuration: `~/.zshrc`

Location: `/Users/mattnovis/.zshrc`

**Optional Alias:**
```bash
# Agentwork environment alias
# Usage: Just type 'agentwork' to cd to the directory and activate the venv
alias aw='cd /Users/mattnovis/agentwork && source venv/bin/activate && python3 --version && echo "Agentwork environment ready!"'
```

**Purpose:**
- Creates `agentwork` alias for quick environment activation
- Can be added to ~/.zshrc if desired

---

## Aliases and Shortcuts

### `aw` alias

**Command:** `aw`

**What it does:**
1. Changes directory to `/Users/mattnovis/agentwork`
2. Activates the Python virtual environment
3. Displays Python version
4. Shows "Agentwork environment ready!" message

**Usage:**
```bash
$ aw
Python 3.9.6
Agentwork environment ready!
(venv) mattnovis@Matts-MacBook-Pro agentwork %
```

---

## Quick Start Guide

### Activate Environment (Method 1 - Using Alias)
```bash
aw
```

### Activate Environment (Method 2 - Manual)
```bash
cd /Users/mattnovis/agentwork
source venv/bin/activate
```

### Verify Installation
```bash
python3 --version  # Should show: Python 3.9.6
pip list           # Shows all installed packages
```

### Deactivate Environment
```bash
deactivate
```

---

## Example Code Snippets

### Read Excel File
```python
import pandas as pd

df = pd.read_excel('your_file.xlsx')
print(df.head())
```

### Write Excel File
```python
df.to_excel('output.xlsx', index=False)
```

### Read CSV File
```python
df = pd.read_csv('your_file.csv')
```

### Write CSV File
```python
df.to_csv('output.csv', index=False)
```

### Multiple Sheets
```python
with pd.ExcelWriter('output.xlsx') as writer:
    df1.to_excel(writer, sheet_name='Sheet1', index=False)
    df2.to_excel(writer, sheet_name='Sheet2', index=False)
```

---

## Session History

### Session 1: 2025-11-13

**Tasks Completed:**
1. ✅ Created project directory: `/Users/mattnovis/agentwork`
2. ✅ Created Python virtual environment (venv) using Python 3.9.6
3. ✅ Upgraded pip to version 25.3
4. ✅ Installed required packages: pandas, openpyxl, xlrd, numpy (with dependencies)
5. ✅ Created MEMORY.md adapted from Operating Budget project
6. ✅ Created `aw` alias in ~/.zshrc for quick environment activation
7. ✅ Renamed virtual environment folder from `spreadsheet_env` to `venv`
8. ✅ Updated venv activate script to display `(venv)` prompt instead of `(spreadsheet_env)`
9. ✅ Updated alias to use `python3` command for reliability
10. ✅ Tested and verified `aw` alias working correctly in new terminal sessions
11. ✅ Initialized git repository
12. ✅ Created .gitignore file
13. ✅ Installed GitHub CLI (gh) via Homebrew
14. ✅ Created GitHub repository: https://github.com/MattNovis/agentwork
15. ✅ Created budget-proposal branch
16. ✅ Set up budget-proposal project folder with documentation

**Configuration:**
- Based on existing Operating Budget spreadsheet environment
- Same package versions for consistency across projects
- Ready for spreadsheet manipulation and data analysis tasks
- Alias tested and confirmed working: shows "Python 3.9.6" and "(venv)" prompt
- Git repository tracking all changes
- Using branch workflow for project isolation

### Session 2: 2025-11-14

**Tasks Completed:**
1. ✅ Continued work on budget-proposal branch
2. ✅ Updated Ideal budget staffing structure (3 mentors + 1 receptionist)
3. ✅ Modified op-budget-v5.xlsx workbook via Python/openpyxl
4. ✅ Updated all Excel sheets: Staffing Costs, Operations Schedule, Expense Detail
5. ✅ Committed and pushed changes to GitHub
6. ✅ Updated both MEMORY.md files with comprehensive documentation

**Budget Work:**
- Reduced Ideal budget from $305,180 to $301,854
- Changed ideal staffing: 3 youth mentors + 1 front desk receptionist (instead of 4 mentors)
- Maintained 6 total staff for ideal programming
- All formulas synchronized across sheets

---

## Current Status

**Environment State:** ✅ Fully configured and actively in use

**Active Projects:**
- 📊 **budget-proposal**: Fairbanks after-school club operating budget
  - Branch: `budget-proposal`
  - Status: Active development
  - Latest: Updated Ideal staffing with receptionist position

**Ready for:**
- Reading/writing Excel files (.xlsx, .xls)
- Reading/writing CSV files
- Data analysis with pandas
- Working with Claude Code on spreadsheet tasks
- Agent automation workflows
- Version control with git/GitHub

**Verified Working:**
- ✅ `aw` alias activates environment correctly
- ✅ Python 3.9.6 available
- ✅ Prompt displays `(venv)` when activated
- ✅ All packages installed and accessible
- ✅ Git repository synced with GitHub
- ✅ openpyxl Excel manipulation working

**No Outstanding Issues**

---

## Important Notes

1. **Virtual Environment:** Always activate the venv before running Python scripts:
   - Quick way: `aw` alias
   - Manual way: `source venv/bin/activate`

2. **Python Version:** This environment uses Python 3.9.6 from Command Line Tools (different from the Operating Budget env which uses Python 3.13.9 from Homebrew)

3. **Package Versions:** Matched to Operating Budget environment for consistency

4. **Git Repository:**
   - Location: `/Users/mattnovis/agentwork`
   - Remote: https://github.com/MattNovis/agentwork
   - Main branch: `main`
   - Active branch: `budget-proposal`
   - Always commit and push changes regularly

5. **Branch Workflow:**
   - Create feature branches for new projects
   - Keep main branch clean
   - Example: `budget-proposal` branch for budget work

---

## Next Steps / Future Tasks

**Budget Proposal Project:**
- [ ] Complete revenue projections (City allocation, fees, grants)
- [ ] Finalize non-personnel expenses (meals, supplies, etc.)
- [ ] Build cash flow projections
- [ ] Create scenario analysis
- [ ] Develop executive summary for City presentation

**Environment Enhancements:**
- [ ] Add matplotlib if data visualization needed
- [ ] Add jupyter if notebook analysis needed
- [ ] Create Python scripts for budget calculations/reporting

---

## Troubleshooting

### Virtual Environment Not Activating
```bash
# Make sure you're in the right directory
cd /Users/mattnovis/agentwork

# Check if venv exists
ls -la venv/

# Try activating manually
source venv/bin/activate
```

### Alias Not Working
```bash
# Reload shell configuration
source ~/.zshrc

# Check if alias exists
alias | grep aw
```

### Package Import Errors
```bash
# Make sure venv is activated (you should see (venv) in prompt)
# Reinstall packages if needed
pip install --force-reinstall pandas openpyxl xlrd
```

### Wrong Python Version
```bash
# Check which Python is being used
which python

# Should show: /Users/mattnovis/agentwork/venv/bin/python
# If not, make sure venv is activated
```

---

## Commands Reference

### Environment Management
```bash
aw                             # Activate virtual environment (using alias)
source venv/bin/activate       # Activate virtual environment (manual)
deactivate                     # Deactivate virtual environment
which python                   # Check which Python is being used
python --version               # Check Python version
pip list                       # List installed packages
pip install <package>          # Install new package
```

### Git & GitHub
```bash
git status                     # Check repository status
git branch                     # List branches
git checkout <branch>          # Switch to branch
git checkout -b <branch>       # Create and switch to new branch
git add <file>                 # Stage file for commit
git commit -m "message"        # Commit staged changes
git push                       # Push commits to remote
git pull                       # Pull changes from remote
gh repo view --web            # Open GitHub repo in browser
```

### File Operations
```bash
ls -la                  # List files with details
cd <directory>          # Change directory
pwd                     # Print working directory
```

### Homebrew
```bash
brew --version          # Check Homebrew version
brew install <package>  # Install software
brew upgrade <package>  # Upgrade software
brew list               # List installed packages
```

---

## Project Location

**Base Directory:** `/Users/mattnovis/agentwork`
**Virtual Environment:** `/Users/mattnovis/agentwork/venv`
**Context File:** `MEMORY.md` (this file)

---

**End of Session Context**
