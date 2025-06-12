# Excel Formulas Used in HR Employee Survey Analysis

This document outlines the key Excel formulas used to clean, prepare, and analyze the survey data.

---

## 🔍 Data Profiling

**Count total responses (excluding blanks):**
```excel
=COUNTA(J2:J14600)
```

**Count blanks in response column:**
```excel
=COUNTBLANK(J2:J14600)
```

**Remove duplicates:**  
Via Excel UI: `Data > Remove Duplicates`

**Standardize text fields:**
```excel
=TRIM(I2)
```

**Find and replace inconsistencies (e.g., 'and' vs '&'):**  
Excel UI: `Find & Replace`

---

## 📊 Data Preparation (Chart Source)

**Unique list of questions:**
```excel
=UNIQUE('HR Survey Reponses'!H2:H14600)
```

**Count of each response type (1 to 4):**
```excel
=COUNTIFS('HR Survey Reponses'!H:H, A2, 'HR Survey Reponses'!J:J, 1)
=COUNTIFS('HR Survey Reponses'!H:H, A2, 'HR Survey Reponses'!J:J, 2)
=COUNTIFS('HR Survey Reponses'!H:H, A2, 'HR Survey Reponses'!J:J, 3)
=COUNTIFS('HR Survey Reponses'!H:H, A2, 'HR Survey Reponses'!J:J, 4)
```

**Average response excluding 0s:**
```excel
=AVERAGEIFS('HR Survey Reponses'!J:J, 'HR Survey Reponses'!H:H, A2, 'HR Survey Reponses'!J:J, "<>0")
```

**Convert counts to percentages:**
```excel
=[@Response1]/[@Total]
=[@Response2]/[@Total]
=[@Response3]/[@Total]
=[@Response4]/[@Total]
```

**Sort descending by average response:**  
Via Excel UI: `Sort by column (Average), Z → A`

---

## 📈 Visualization

- 100% Stacked Bar Chart: Insert → Chart → 100% Stacked Bar
- Color Scheme: Shades of red/orange (1–2), blue (3–4)
- Removed axis/title/gridlines for cleaner appearance