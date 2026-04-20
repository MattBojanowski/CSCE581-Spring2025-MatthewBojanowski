# Quiz 3 Feedback - Matthew Bojanowski

**Q1: 58 / 70**
**Q2: 30 / 30**
**Total: 88 / 100**

---

## Q1 - 58 / 70

- **-10**: The notebook's label-generation rule is substantively incorrect for this task. It marks a row as `primary` whenever the source URL contains one of `elections`, `sos`, or `vote` plus the state name, which incorrectly pulls many `vote411` secondary-source rows into the primary class and undermines the core primary-vs-secondary classification target.
- **-2**: The source dataset itself has malformed `NM`/`TX` entries and uses `DL` for Delaware, so this is only a small deduction. The submitted combined CSV and sample-output artifact reflect those source irregularities instead of explicitly normalizing or documenting them.

## Q2 - 30 / 30

Complete and well documented.
