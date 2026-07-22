# SQL Practice

SQL queries solved on DataLemur as I build toward the Google Data Analytics Certificate and SQL for Data Science (UC Davis).

This repo will grow as I go — starting with the basics and adding queries as I learn.

## Queries

### find-candidates-with-all-skills.sql
**Problem:** Given a table of candidates and their skills, find candidates who have all three required skills (Python, Tableau, PostgreSQL) for a job, sorted by candidate ID.

```sql
SELECT candidate_id
FROM candidates
WHERE skill IN ('Python', 'Tableau', 'PostgreSQL')
GROUP BY candidate_id
HAVING COUNT(skill) = 3
ORDER BY candidate_id ASC;
```

**Approach:** Filters to the three required skills, groups by candidate, and uses `HAVING COUNT(skill) = 3` to keep only candidates who have all three.
