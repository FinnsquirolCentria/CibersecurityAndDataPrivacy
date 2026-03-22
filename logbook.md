# Logbook

| Date  | Used hours | Subject(s) |  Outcome(s) |
| :---         |     :---:      |     :---:      |     :---:      |
| 25.1.2026 | 0,5 | Creating Repository and loogbook | Repository and loogbok |
| 1.2.2025 | 1 | Reading what is SQL injection | Understanding SQL injection and its usage |
| 1.2.2025 | 1 | Solving SQL injection vulnerability in WHERE clause allowing retrieval of hidden data lab| Lab solved using the examples that I learned |
| 1.2.2025| 0,5 |  Learning about login bypass usin SQL injection | Understanding how bypassing login works|
| 1.2.2025| 1 |  Solving SQL injection vulnerability allowing login bypass lab | Lab solved using the principles learned|
| 2.2.2025| 1,5 |  Learning about Authentication vulnerabilities | Learned about the vulnerabilities in password-based login|
| 2.2.2025| 1 |  Getting familiarized with Burp suite| Learned how to use Burp intruder|
| 2.2.2025| 1 |  Solving Username enumeration via different responses lab| Solved using Burp Intruder|
| 2.2.2025| 0,5 | Learning about resetting user password method| Learned about URL tokenization|
| 2.2.2025| 1 |  Solving Password reset broken logic lab| Solved using Burp Repeater|
| 2.2.2025| 0,5 |  Learning about access control| Learned about the access control vulnerabilities|
| 2.2.2025| 0,5 |  Solving Unprotected admin functionality lab| Solved using Burp Repeater by checking robots.txt|
| 2.2.2025| 0,5 |  Solving User role can be modified in user profile lab| Solved using Burp Repeater and adding roleid|
| 4.2.2026 | 0,5 | Setting up Docker environment for Booking System Phase 1 | Started containers; web app accessible at http://localhost:8001 |
| 4.2.2026 | 0,5 | Run OWASP ZAP automated scan | ZAP scan completed; multiple Medium/Low alerts
| 4.2.2026 | 0,5 | Created a Zap report | Saved ZAP output to `zap_report_round1.md` and added brief ZAP summary |
| 4.2.26 | 1 | Manual testing of registration | Manual registration attempts returned server error (registration failed); could not consistently confirm SQLi/XSS or password exposure |
| 5.2.2026 | 1,5 | Write test report | Created `test_report_diegofinnila.md` documenting ZAP findings, stability issues and recommended fixes |
| 10.2.2026 | 3 | Re-Run ZAP Scan and write Discussion Post | Created a ZAP report for the updated version and wrote a discussion post based on the findings compared between the first website version and the updated one |
| 17.2.2026 | 3 | Re-Run ZAP Scan for Part1 and checked the database manually| Created a ZAP report that included high alerts and found passwords were in plaintext|
| 17.2.2026 | 6 | Learning to crack passwords with different methods|Cracked 6 out of 10 passwords|
| 25.2.2026 | 7,5 | Performing an authorization test |Found pages and endpoints using different tools and tested POSTS. Created a zap report and own findings report |
| 16.3.2026 | 1 | Solving SQL injection UNION attack, determining the number of columns returned by the query | Solved by modifying the category parameter to add additional columns containing NULL value until it the internal server error dissapeared|
| 16.3.2026 | 1 | Solving SQL injection UNION attack, finding a column containing text | Solved by modifying the category parameter to add additional columns containing NULL, and replacing the NULL values for the one provided by the lab value until the internal server error dissapeared|
| 16.3.2026 | 1 | Solving SQL injection UNION attack, retrieving data from other tables | Solved by determining the number of columns and retrieving the users info|
| 16.3.2026 | 1 | Solving SQL injection UNION attack, retrieving multiple values in a single column | Solved by determining the number of columns and retrieving the users info using Burp Repeater|
| 16.3.2026 | 1,5 | Solving SQL injection with filter bypass via XML encoding | Solved by performing a UNION attack using hackvertor extension in Burp Repeater |
| 16.3.2026 | 1,5 | Solving SQL injection attack, querying the database type and version on Oracle | Solved by performing a UNION attack using Burp Repeater, determining number of columns, data types and finally outputing the version|
| 17.3.2026 | 1 | Solving SQL injection attack, querying the database type and version on MySQL and Microsoft | Solved by performing a UNION attack using Burp Repeater|
| 17.3.2026 | 1 | Solving SQL injection attack, listing the database contents on non-Oracle databases | Solved by performing a UNION attack using Burp Repeater by determining the name of the table and the columns it has|
| 17.3.2026 | 0,5 | Solving SQL injection attack, listing the database contents on Oracle | Solved by performing a UNION attack using Burp Repeater by determining the name of the table and the columns, then retrieving the usernames and password based on the table name info|
