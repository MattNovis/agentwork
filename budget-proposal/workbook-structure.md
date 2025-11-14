# Workbook Structure Proposal

## File
- `op-budget-budget.xlsx`
- Stored in `op-budget/`
- Uses named ranges for high-level drivers to simplify formulas.

## Sheet: `Assumptions`
- **Purpose:** Centralize key drivers, version control placeholders, and flag pending confirmations.
- **Columns:** `Category`, `Driver`, `Value`, `Units`, `Status (Confirmed/Placeholder)`, `Owner`, `Notes`.
- **Named Ranges:**
  - `FiscalYearStart`, `FiscalYearEnd`
  - `OperatingDays`, `AverageDailyAttendance`
  - `StaffBenefitsRate`, `PayrollTaxesRate`
  - `InflationRate`, `UtilitiesInflationRate`
- **Formulas:**
  - `OperatingDays` defaults to `NETWORKDAYS(FiscalYearStart,FiscalYearEnd,HolidayRange)` if holiday list provided.
  - Conditional formatting to highlight `Status="Placeholder"`.

## Sheet: `Enrollment & Staffing`
- **Columns:** `Program`, `Age Group`, `Capacity`, `Avg Daily Attendance`, `Staff Ratio (Youth:Staff)`, `Required Staff FTE`, `Shift Hours`, `Annual Hours`, `Notes`.
- **Formulas:**
  - `Required Staff FTE = (Avg Daily Attendance / Staff Ratio) * (Program Hours per Week / 40)` using named range `ProgramHoursPerWeek` from `Assumptions`.
  - `Annual Hours = Required Staff FTE * 2080`.
- **Outputs:** Feeds personnel expense sheet via lookup on role type.

## Sheet: `Staffing Costs`
- **Columns:** `Role`, `FTE`, `Hourly Rate`, `Annual Salary`, `Benefits %`, `Total Compensation`, `Funding Source`, `Placeholder?`, `Notes`.
- **Formulas:**
  - `Annual Salary = FTE * 2080 * Hourly Rate` (for hourly roles) or manual entry for salaried positions.
  - `Total Compensation = Annual Salary * (1 + Benefits % + PayrollTaxesRate)` referencing `Assumptions` named ranges.
  - Data validation referencing `Enrollment & Staffing` for FTE pulls.

## Sheet: `Revenue Forecast`
- **Structure:**
  - Header rows for revenue categories (Earned, Contributions, Government, Other).
  - Columns `Category`, `Line Item`, `Monthly Amounts (Jul-Jun)`, `Total`, `Restriction`, `Confidence`.
- **Formulas:**
  - `Total = SUM(Jan:Dec)`.
  - Scenario toggles using named range `ScenarioMultiplier` to scale uncertain revenue streams.

## Sheet: `Expense Detail`
- **Sections:** Personnel (linked from `Staffing Costs`), Program, Facilities, Administrative, Contingency.
- **Columns:** `Category`, `Line Item`, `Cost Driver`, `Formula`, `Monthly Amounts`, `Total`, `Placeholder?`, `Notes`.
- **Formulas:**
  - Personnel rows reference `Staffing Costs!Total Compensation` distributed monthly via `=AnnualTotal/12` unless seasonality specified.
  - Program costs tied to enrollment counts (e.g., meals = `Avg Daily Attendance * Cost per Meal * OperatingDays/Month`).
  - Facilities costs include escalator using `UtilitiesInflationRate` from `Assumptions`.

## Sheet: `Cash Flow`
- **Columns:** `Month`, `Beginning Cash`, `Cash In`, `Cash Out`, `Net Change`, `Ending Cash`, `Minimum Target`, `Variance`, `Notes`.
- **Formulas:**
  - `Cash In = Revenue Forecast` monthly sum.
  - `Cash Out = Expense Detail` monthly sum.
  - `Net Change = Cash In - Cash Out`.
  - `Ending Cash = Beginning Cash + Net Change` (with first month seeded from `Assumptions` named range `StartingCash`).
  - Conditional formatting when `Ending Cash < Minimum Target`.

## Sheet: `Scenario Analysis`
- **Layout:** Table of scenarios (Base, Conservative, Stretch) with multipliers for key drivers.
- **Columns:** `Scenario`, `Revenue Multiplier`, `Enrollment Multiplier`, `Expense Escalation`, `Resulting Surplus/Deficit`, `Notes`.
- **Formulas:**
  - Surplus/Deficit computed referencing aggregated totals via `SUMPRODUCT` or scenario-specific outputs.
  - Use slicer or dropdown to set active scenario (optional but noted for later implementation).

## Sheet: `Checklist`
- **Purpose:** Track placeholders and approvals.
- **Columns:** `Item`, `Owner`, `Status`, `Due Date`, `Notes`.
- **Formulas:**
  - Status data validation (`Not Started`, `In Progress`, `Needs Review`, `Complete`).
  - Conditional formatting for overdue items.

## Supporting Named Ranges & Tables
- `tblRevenue`, `tblExpenses`, `tblStaffing` for structured references.
- Holiday list range `HolidayRange` (optional) for accurate operating days.

## Implementation Notes
- Protect `Assumptions` sheet except for the `Value` column to prevent accidental edits.
- Freeze top rows and key columns on detail sheets for readability.
- Include a cover sheet (optional) with project summary and version history if required by stakeholders.
