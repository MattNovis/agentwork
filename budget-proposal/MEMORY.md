# Budget Proposal Project - Session Context

**Last Updated:** 2025-11-14
**User:** mattnovis
**Project:** Budget Proposal - Fairbanks After-School Club Operating Budget
**Branch:** budget-proposal

---

## Project Overview

Creating an operating budget for a Fairbanks after-school club (similar to Boys & Girls Club) to present to the City of Fairbanks for funding consideration.

**Purpose:**
- Develop comprehensive operating budget with Necessity and Ideal scenarios
- Show minimum viable staffing vs. full programming capabilities
- Present funding request to City of Fairbanks for club re-opening

**Tools & Libraries Available:**
- Python 3.9.6
- pandas 2.3.3 (data manipulation)
- openpyxl 3.1.5 (Excel .xlsx files)
- xlrd 2.0.2 (older .xls files)
- numpy 2.0.2 (numerical computing)

---

## Project Directory Structure

```
/Users/mattnovis/agentwork/budget-proposal/
└── MEMORY.md                   # This file - project context
```

---

## Files in This Project

| File | Purpose | Status |
|------|---------|--------|
| MEMORY.md | Session context and project documentation | ✅ Updated |
| README.md | Project background and directive | ✅ Created |
| workplan.md | 10-phase workplan and checklist | ✅ Created |
| workbook-structure.md | Detailed Excel workbook structure proposal | ✅ Created |
| op-budget-v5.xlsx | Main operating budget workbook | ✅ Active development |

---

## Session History

### Session 1: 2025-11-13

**Tasks Completed:**
1. ✅ Created `budget-proposal` branch
2. ✅ Created `budget-proposal/` folder
3. ✅ Created MEMORY.md for project context tracking
4. ✅ Added planning documents (README.md, workplan.md, workbook-structure.md)
5. ✅ Analyzed op-budget-v5.xlsx file
6. ✅ Fixed Teen Coordinator FTE error (was 41.0, corrected to 0.817)
7. ✅ Implemented split schedule (38 weeks standard + 14 weeks extended)
8. ✅ Created Necessity vs Ideal budget scenarios
9. ✅ Built Operations & Staffing Schedule sheet
10. ✅ Updated minimum viable staffing to 2 youth mentors

**Major Changes:**
- Separated Program Director and Director of Youth Development into two positions
- Created split work schedules for youth mentors (20 hrs standard, 40 hrs extended)
- Established Necessity budget baseline: $191,528 (2 Directors + 2 Youth Mentors)
- Established Ideal budget: $305,180 (adds 2 more Mentors + Teen Coordinator)

### Session 2: 2025-11-14

**Tasks Completed:**
1. ✅ Updated Ideal staffing: Changed from 4 youth mentors to 3 youth mentors + 1 front desk receptionist
2. ✅ Updated Staffing Costs sheet with new positions and FTE calculations
3. ✅ Updated Operations & Staffing Schedule for School Year and Summer sections
4. ✅ Updated Expense Detail sheet with new personnel rows and formulas
5. ✅ Committed changes to git and pushed to remote
6. ✅ Updated MEMORY.md with comprehensive project documentation

**Budget Changes:**
- Ideal budget reduced from $305,180 to $301,854 (saving of $3,326)
- Front Desk Receptionist: $18/hr, 0.635 FTE, $29,938 total compensation
- Additional Youth Mentor: Reduced from 2 positions to 1 position
- Still maintains 6 total staff for ideal programming

---

## Current Status

**Project State:** 🟢 Active development - Budget structure complete

**Current Budget Summary:**
- **Necessity**: $191,528 (4 staff: 2 Directors + 2 Youth Mentors)
- **Ideal**: $301,854 (6 staff: adds 1 Youth Mentor + 1 Receptionist + 1 Teen Coordinator)
- **Difference**: $110,326

**What's Working:**
- ✅ Staffing structure clearly defined
- ✅ Two-tier budget (Necessity vs Ideal) for presentation flexibility
- ✅ Split schedules properly calculated
- ✅ All Excel sheets synchronized
- ✅ Git repository tracking all changes

**Next Steps:**
- [ ] Add revenue projections to Revenue Forecast sheet
- [ ] Complete non-personnel expenses (meals, supplies, facilities)
- [ ] Build Cash Flow projections
- [ ] Create Scenario Analysis
- [ ] Develop executive summary for City presentation

---

## Project Requirements

**Confirmed Details:**
- **Organization**: After-school club for Fairbanks, Alaska (City-operated or 501(c)(3))
- **Audience**: City of Fairbanks Mayor and City Manager
- **Purpose**: Secure funding to re-open club after previous Boys & Girls Club closure
- **Budget Type**: Annual operating budget with two scenarios (Necessity/Ideal)
- **Fiscal Year**: To be confirmed with City
- **Operating Days**: 275 days/year (190 school days + 70 summer + 15 break days)

**Key Drivers:**
- **School Year**: 2pm-6pm, 5 days/week, 38 weeks
- **Summer**: 7am-6pm, 5 days/week, 14 weeks
- **School Breaks**: 7am-6pm, ~15 days/year
- **Benefits Rate**: 25% salaried, 18% hourly
- **Payroll Tax**: 8% (hourly positions)

**Still To Define:**
- Enrollment capacity by age group
- Revenue sources and amounts (City allocation, fees, grants)
- Facility cost (rent vs. in-kind from City)
- Meal program details and vendor quotes
- Insurance quotes
- Transportation needs
- Marketing/outreach budget

---

## Technical Notes

**Environment:**
- Working Directory: `/Users/mattnovis/agentwork`
- Project Folder: `budget-proposal/`
- Git Branch: `budget-proposal`
- Git Repository: https://github.com/MattNovis/agentwork
- Python Virtual Environment: Activate with `aw` alias or `source venv/bin/activate`

**Available Commands:**
```bash
aw                          # Activate virtual environment
cd budget-proposal          # Navigate to project folder
python3 script.py           # Run Python scripts
git status                  # Check git status
git push                    # Push changes to GitHub
```

---

## Data Files

**Excel Workbook: op-budget-v5.xlsx**

**Sheets:**
1. **Assumptions** - Key drivers and parameters
2. **Enrollment & Staffing** - Capacity and FTE calculations
3. **Staffing Costs** - Personnel compensation details
4. **Revenue Forecast** - Revenue projections (to be completed)
5. **Expense Detail** - All expenses with monthly breakdown
6. **Cash Flow** - Monthly cash flow (to be completed)
7. **Scenario Analysis** - What-if scenarios (to be completed)
8. **Operations & Staffing Schedule** - Daily operations breakdown

---

## Budget Details

### Staffing Structure

**Necessity Budget ($191,528):**
- Program Director: $50,000 salary → $62,500 w/ benefits
- Director of Youth Development: $50,000 salary → $62,500 w/ benefits
- Youth Mentors (2): $20/hr, 0.635 FTE each → $66,528 total w/ benefits

**Ideal Budget Additions ($110,326):**
- Additional Youth Mentor (1): $20/hr, 0.635 FTE → $33,264 w/ benefits
- Front Desk Receptionist: $18/hr, 0.635 FTE → $29,938 w/ benefits
- Teen Coordinator: $22/hr, 0.817 FTE → $47,124 w/ benefits

**Total Ideal Budget: $301,854**

### FTE Calculations

**Split Schedule:**
- Standard Period: 38 weeks
- Extended Period: 14 weeks

**Youth Mentor FTE:**
- Standard: 20 hrs/wk × 38 wks = 760 hrs
- Extended: 40 hrs/wk × 14 wks = 560 hrs
- Total: 1,320 hrs ÷ 2,080 = 0.635 FTE

**Teen Coordinator FTE:**
- Standard: 30 hrs/wk × 38 wks = 1,140 hrs
- Extended: 40 hrs/wk × 14 wks = 560 hrs
- Total: 1,700 hrs ÷ 2,080 = 0.817 FTE

---

## Scripts and Code

**Python Scripts:**
- Using openpyxl for Excel manipulation
- All updates done programmatically to maintain formula integrity

**Key Operations:**
- Reading/writing Excel formulas
- Calculating FTE from hours
- Applying benefits and payroll tax rates
- Synchronizing multiple sheets

---

## Questions & Decisions

**Open Questions:**
- What is the City's expected contribution vs. other revenue sources?
- Will the City provide facility space in-kind or charge rent?
- What enrollment numbers are realistic for Fairbanks?
- Are there existing grants or funding commitments?
- What insurance requirements does the City have?
- Will meal program be required (USDA reimbursement)?

**Key Decisions Made:**
1. Two-tier budget approach (Necessity vs Ideal) for presentation flexibility
2. Split schedule model (38 weeks standard + 14 weeks extended)
3. Two director positions at $50k each (Program Director + Dir. of Youth Development)
4. Minimum viable staffing: 4 on-site (2 directors + 2 youth mentors)
5. Ideal staffing: 6 on-site (adds 1 youth mentor + 1 receptionist + 1 teen coordinator)
6. Benefits: 25% salaried, 18% hourly + 8% payroll tax
7. Using openpyxl for all Excel updates to preserve formulas
8. Git branch workflow for version control

---

## Important Notes

1. **Branch Workflow:** This project lives on the `budget-proposal` branch
   - All commits pushed to: https://github.com/MattNovis/agentwork

2. **Budget Philosophy:**
   - Necessity = Minimum to safely operate
   - Ideal = Full programming with optimal ratios

3. **Staffing Ratios:**
   - Necessity: 4 staff provides basic supervision
   - Ideal: 6 staff allows better youth:staff ratios and specialized programming

4. **Formula Integrity:**
   - All Excel updates done via Python (openpyxl)
   - Preserves formulas and cell references
   - Never manually edit calculated cells

5. **Placeholder Tracking:**
   - Insurance: $30,000 (placeholder)
   - Facility rent: $19,200 (placeholder)
   - Meals: $0 (awaiting vendor quote)
   - Utilities: $0 (assuming City in-kind)

6. **Git Commits:**
   - Commit after each major change
   - Use descriptive commit messages
   - Always include budget impact in commit message

---

## Resources & References

**Documentation:**
- pandas: https://pandas.pydata.org/docs/
- openpyxl: https://openpyxl.readthedocs.io/
- Python datetime: https://docs.python.org/3/library/datetime.html

---

**End of Session Context**
