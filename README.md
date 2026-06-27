# Practical Course Performance Analysis
### Dept. of Science Technology · ND II (Morning)
**Semester:** First · **Lecturer:** OLUMODEJI I.A.

---

## Dataset Overview

| Field | Detail |
|-------|--------|
| Sheets | 3 (`nd2`, `ND2 CO23`, `nd2 co19`) |
| Course | Practical for STP 211 and STP 212 (Code: STP 211, Unit: 2.0) |
| Assessment weights | Exam 40% · Practical 40% · CA 20% |

### Schema

```
SNO          int       Serial number
MATRIC       str       Matriculation number (e.g. ST/24/1-0002)
SNAME        str       Student surname
INIT         str       Student initials
Exam         float     Examination score (weighted ×0.4, max ≈ 40)
Pract        float     Practical score (weighted ×0.4, max ≈ 38)
CA           float     Continuous Assessment score (weighted ×0.2, max ≈ 17)
Total        float     Aggregate total (out of 100)
```

---

## Cohort Summary

| Group | Enrolled | Sat exam | Absent | Pass | Fail |
|-------|----------|----------|--------|------|------|
| ND2 2024 (main) | 194 | 162 | 32 | 154 | 8 |
| Carryover 2023 | 3 | 3 | 0 | 3 | 0 |
| Carryover 2019 | 1 | 1 | 0 | 1 | 0 |
| **Total** | **198** | **166** | **32** | **158** | **8** |

---

## Main Cohort Analysis (ND2 2024)

### Descriptive Statistics (162 active students)

| Metric | Exam (/40) | Practical (/38) | CA (/17) | Total (/100) |
|--------|-----------|-----------------|----------|--------------|
| Mean | 19.56 | 28.57 | 14.13 | 62.27 |
| Median | 21.0 | 30.0 | 15.0 | 66.0 |
| Std Dev | 7.68 | 5.73 | 2.44 | 15.44 |
| Min | 1.0 | 10.0 | 5.0 | 16.0 |
| Max | 40.0 | 38.0 | 17.0 | 95.0 |
| 25th pct | 15.0 | 25.0 | 14.0 | 53.0 |
| 75th pct | 25.0 | 30.0 | 16.0 | 70.0 |

### Attendance

- **83.5%** of enrolled students sat the exam (162/194)
- **16.5%** recorded zero scores — treated as absent/non-participating
- All 32 absent students have Total = 0 across all three components, confirming complete non-participation rather than partial scores

### Grade Distribution (Federal Polytechnic grading scale)

| Grade | Score Range | Count | % of Active |
|-------|-------------|-------|-------------|
| A | ≥70 | 54 | 33.3% |
| B | 60–69 | 57 | 35.2% |
| C | 50–59 | 28 | 17.3% |
| D | 45–49 | 2 | 1.2% |
| E | 40–44 | 13 | 8.0% |
| F | <40 | 8 | 4.9% |
| **Pass (≥40)** | | **154** | **95.1%** |
| **Fail (<40)** | | **8** | **4.9%** |

### Score Distribution by Band

| Band | Range | Count |
|------|-------|-------|
| 90–100 | A (distinction) | 1 |
| 80–89 | A (merit) | 13 |
| 70–79 | A | 40 |
| 60–69 | B | 57 |
| 50–59 | C | 28 |
| 40–49 | D/E (borderline) | 15 |
| <40 | F (fail) | 8 |

---

## Component Analysis

### Utilisation Rate (avg as % of maximum)

| Component | Avg Score | Max Observed | Utilisation |
|-----------|-----------|-------------|-------------|
| Exam | 19.56 | 40 | **48.9%** |
| Practical | 28.57 | 38 | **75.2%** |
| CA | 14.13 | 17 | **83.1%** |
| Total | 62.27 | 95 | 62.3% |

Students perform significantly better in Practical and CA components than in the written examination. The 26-point gap between practical utilisation (75.2%) and exam utilisation (48.9%) is the most critical pedagogical finding.

### Inter-component Correlations

```
           Exam    Pract    CA    Total
Exam       1.00    0.926  0.854   0.976
Pract      0.926   1.00   0.962   0.984
CA         0.854   0.962  1.00    0.940
Total      0.976   0.984  0.940   1.00
```

All three components correlate very strongly with the total (r ≥ 0.854). A student's practical performance is the single best predictor of final grade (r = 0.984).

### Practical Score Clustering

Practical scores are not continuous — they cluster at discrete values:

| Practical Score | Students | Implied Tier |
|----------------|----------|-------------|
| 10 | ~8 | Minimum / near-zero engagement |
| 23 | ~20 | Low tier |
| 25 | ~16 | Below average |
| 28 | ~24 | Average |
| 30 | ~43 | Good |
| 35 | ~38 | Very good |
| 38 | ~13 | Excellent |

This banded pattern indicates rubric-based marking with discrete performance tiers rather than continuous scoring.

---

## Key Findings

### Finding 1 — Bimodal class distribution
The score distribution is bimodal with clusters around 60–70 (modal B-grade band) and 40–50 (borderline zone). The gap between 44 and 50 is sparsely populated, suggesting a natural divide between engaged and at-risk students.

### Finding 2 — Practical competence exceeds exam competence
Students perform 26 percentage points better in practical work than written examinations. This is consistent with a course where hands-on skills are the primary learning outcome, but the exam gap warrants review of exam preparation and question design.

### Finding 3 — Absenteeism is the largest single risk
32 students (16.5%) have zero scores across all components. If the absent cohort is excluded, the class performance profile is excellent. Reducing absenteeism is the highest-leverage intervention available.

### Finding 4 — F-grade students show holistic disengagement
All 8 failing students received the minimum scores across all three components simultaneously. This is not random — it indicates complete course non-engagement rather than specific subject difficulty.

### Finding 5 — Carryover success rate is 100%
All 4 carryover students from previous sessions passed. This suggests the course content and assessment structure are accessible to repeat students and that the practical-heavy format aids remediation.

---

## Recommendations

### For the lecturer (OLUMODEJI I.A.)

1. **Investigate the 32 absent students early** — identify whether absences are medical, personal, or structural, and flag persistent absentees to the department.
2. **Early intervention for E-grade students** — the 13 borderline students (40–44) need targeted practical coaching; a 5-mark improvement from any component would move them to C.
3. **Exam preparation sessions** — the 26-point gap between practical and exam utilisation suggests students struggle to transfer practical knowledge to written format. Structured mock exam practice is recommended.
4. **Investigate the 8 F-grade students** — holistic minimum scores suggest non-participation. These students should be contacted before the next semester for welfare checks.
5. **Review practical marking rubric** — the banded discrete scoring pattern (10, 23, 25, 28, 30, 35, 38) limits differentiation between students at each tier. A more granular rubric could better reward incremental improvement.

### For the department

1. **Monitor carryover duration** — the 2019 carryover (6-year) is unusually long. A maximum carryover period policy should be consistently enforced.
2. **Attendance tracking system** — 16.5% absence rate in a single course is high. A centralised digital attendance system would enable earlier intervention.

---

## Methodology

```python
import pandas as pd
import numpy as np

# Load main sheet
df = pd.read_excel("STP_213_2026.xlsx", sheet_name="nd2", header=None)
df.columns = ['SNO','MATRIC','SNAME','INIT','Exam','Pract','CA','Total']
df = df.iloc[11:]  # skip header rows
df = df[df['MATRIC'].astype(str).str.startswith('ST/')]

# Convert to numeric
for col in ['Exam','Pract','CA','Total']:
    df[col] = pd.to_numeric(df[col], errors='coerce').fillna(0)

# Separate active from absent
df_active = df[df['Total'] > 0].copy()
df_absent = df[df['Total'] == 0].copy()

# Grading function (Nigerian polytechnic scale)
def grade(score):
    if score >= 70: return 'A'
    elif score >= 60: return 'B'
    elif score >= 50: return 'C'
    elif score >= 45: return 'D'
    elif score >= 40: return 'E'
    else: return 'F'

df_active['Grade'] = df_active['Total'].apply(grade)
```

---

*Analysis: OLUMODEJI IBUKUN*
