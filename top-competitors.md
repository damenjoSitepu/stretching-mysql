* Top Competitors ( Medium )

- Julia just finished conducting a coding contest, and she needs your help assembling the leaderboard! Write a query to print the respective hacker_id and name of hackers who achieved full scores for more than one challenge. Order your output in descending order by the total number of challenges in which the hacker earned a full score. If more than one hacker received full scores in same number of challenges, then sort them by ascending hacker_id.

- Query Answer: 

```
SET sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));
SELECT 
CONCAT(submissions.hacker_id,' ',(SELECT hackers.name FROM hackers WHERE hacker_id = submissions.hacker_id))
-- SUM(submissions.score)
-- COUNT(submissions.challenge_id) as count_submissions_full_score_from_challege
FROM submissions INNER JOIN challenges ON submissions.challenge_id = challenges.challenge_id
INNER JOIN difficulty ON challenges.difficulty_level = difficulty.difficulty_level
WHERE difficulty.score = submissions.score 
GROUP BY submissions.hacker_id
HAVING COUNT(submissions.challenge_id) > 1
ORDER BY COUNT(submissions.challenge_id) DESC, submissions.hacker_id ASC;
```