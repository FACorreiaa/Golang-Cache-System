# Golang Caching System

## Caching user information to increase database throughput and availability

This was used from someone for an interview question and I solved the assessment to practice more Go.
If within 1000 requests there are 100 uniques user ids, then there should be only a maximum 100 requests into the database but all 1000 requests should get a response with a user data.

Follow up question from the interviewer is how do you handle concurrent writes and reads to the cached map ('db' map in this example). Also would be interesting to see how would fix concurrent miss hits to the same user id (in a real case scenario, database access takes time could be the case) and caching invalidation. I know that you can not explain everything in a 20m video but these are very common interesting scenarios to solve and would be amazing to see your take :)

Use Mutex

