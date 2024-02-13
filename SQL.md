# Something about Database
## Thứ tự thực thi câu lệnh SQL
`1. FROM/JOIN` $\to$ `2. WHERE` $\to$ `3. GROUP BY` $\to$ `4. HAVING` $\to$`5. SELECT` $\to$ `6. DISTINCT` $\to$ `7. ORDER BY` $\to$ `8. LIMIT`

Example: 
``` sql
SELECT -- No. 5
  DISTICNT character, class -- No. 6
  AVG(starts, experience_points) AS average_experience
FROM character
JOIN stats ON character.character_id = stats.character_id -- No. 1
WHERE stats.level >= 10 -- No. 2
GROUP BY character.class -- No. 3
HAVING AVG(stats.experience_points) > 2000 -- No. 4
ORDER BY average_experience DESC -- No. 7
LIMIT 10; -- No. 8
```
