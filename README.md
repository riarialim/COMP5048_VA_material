# COMP5048: Visual Analytics – Group Allocation Script  
**Automated Student Grouping with Fairness & Friend Pairing Logic (2024 Edition)**  
**Created by:** Maria Yu Qian Lim

---

## What This Is

This Python-based tool automates the process of grouping students for assignments in the COMP5048 Visual Analytics unit. It supports fair random allocation, friend pairing, and Canvas integration—all while saving time for tutors and ensuring better collaboration outcomes.

---

## Tools & Tech Stack

- **Language:** Python 3  
- **Environment:** Jupyter Notebook  
- **Libraries:**
  - `pandas` – for working with structured data
  - `random` – for reproducible shuffling
  - `math` – for group size logic

---

## Key Features

- **Tutorial Integrity Check**
    - Ensures all students in a group are from the **same tutorial session**

- **Smart Group Allocation**
    - Randomly assigns students into evenly sized groups
    - Customisable group size
    - Handles leftover students smoothly

- **Friend Pairing Support**
    - Students can nominate **one friend**
    - Script guarantees they are **grouped together** and ensures each student appears in **only one pair**
    - Pairs are treated as a unit during random allocation

- **Engagement-Aware Grouping**
    - Flags students with low class engagement (for example, absent to most classes or not submitting previous assignments)
    - Ensures they are **spread across groups**, not clustered together
    - Places them as the **last member added** in otherwise formed groups

- **Canvas-Ready Output**
    - Outputs results to a clean `.csv` file
    - Tutors can **upload directly to Canvas** or post announcements without extra editing

---

## Example Workflow for Tutors

1. **Collect nominated friend pairs** (student IDs) prior to the grouping session.
2. **Review engagement levels** of students without nominated pairs to flag any who may be uncontactable or inactive.
3. **Run the script** during the grouping session and input:
   - The desired group size (default is 4)
   - The list of nominated pairs
4. The script will automatically:
   - Ensure all friend pairs are from the **same tutorial**
   - Lock friend pairs together during random group assignment
   - Apply **engagement-aware logic** to avoid grouping multiple low-engagement students together
5. **Review the group allocation output** before finalizing groupings.
6. **Export the final `.csv`** and upload it directly to Canvas for group announcement or assignment setup.

---

## Why I Made This

> Grouping students randomly is simple, but grouping them **fairly**, while considering participation levels and friendships, is hard.  
> This script brings both structure and empathy to group formation—saving time for tutors and improving student experience.

---

## Included File

- `Assignment_2_Grouping-2024.ipynb`: Full working notebook
  - Input parsing & validation
  - Friend & tutorial checks
  - Engagement-aware allocation
  - Canvas-ready `.csv` export


