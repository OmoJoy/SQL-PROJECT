Question 1: Total sales records being analyzed.

SQL Queries: select count(*) from all_sessions s join analytics n on s.fullvisitorid = n.fullvisitorid

Answer: There are 113633 matching records between the analytics and the all_sessions table.

Question 2: Total number of unique visitors (fullVisitorID).

SQL Queries: select distinct(s.fullvisitorid) from all_sessions s join analytics n on s.fullvisitorid = n.fullvisitorid

Answer: We have a total of 1657 unique visitors based on the fullvisitorid column.

Question 3: Total number of unique visitors (VisitID)

SQL Queries: select distinct(s.visitid) from all_sessions s join analytics n on s.fullvisitorid = n.fullvisitorid

Answer: We have a total of 1700 unique visitors based on the visitid columns.



Question 4: 

SQL Queries:

Answer:



Question 5: 

SQL Queries:

Answer:
