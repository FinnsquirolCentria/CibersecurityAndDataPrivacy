# PortSwigger 
## Completed Labs
<img width="1158" height="464" alt="image" src="https://github.com/user-attachments/assets/b3e824cc-0b40-43a6-81b4-c42ec6332c92" />

List:

* SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
* SQL injection vulnerability allowing login bypass
* SQL injection attack, querying the database type and version on Oracle
* SQL injection attack, querying the database type and version on MySQL and Microsoft
* SQL injection attack, listing the database contents on non-Oracle databases
* SQL injection attack, listing the database contents on Oracle
* SQL injection UNION attack, determining the number of columns returned by the query
* SQL injection UNION attack, finding a column containing text
* SQL injection UNION attack, retrieving data from other tables
* SQL injection UNION attack, retrieving multiple values in a single column
* SQL injection with filter bypass via XML encoding
* Unprotected admin functionality
* User role can be modified in user profile
* Username enumeration via different responses
* Password reset broken logic

# The Booking system project

## Phase 1

* What worked/what didn't work: I understood how to use OWASP ZAP, but wasn't familiar on how to find high alerts at first
* What took the most time: Getting familiar with ZAP
* What did you learn from this phase: How to use ZAP in order to find alerts and have a first glance regarding the potential security issues

## Phase 2
* What worked/what didn't work: Dictionary and rever hash lookup worked quite well. Mask (non‑dictionary) attack didn't worked for this Phase, got nothing using this method.
* What took the most time: Performing Mask (non‑dictionary) attack.
* What did you learn from this phase: Learning how to crack passwords and getting even more familiar with ZAP reports

## Phase 3
* What worked/what didn't work: Discovered pages and endpoints efficiently. I was having problems when testing the roles, but I think it was because I was overthinking it.
* What took the most time: Both discovering pages and endpoints, but it was mostly because I was overthinking that there was more than it actually was and I kept retrying
* What did you learn from this phase: The different ways to discover pages and endpoints

## Reflection
During this topic, I learned how surprisingly easy it is to create a vulnerable website and how many different ways those vulnerabilities can be exploited. Working through these exercises helped me understand why security needs to be considered from the very beginning of development, not as an afterthought. PortSwigger also strengthened my understanding of common attack vectors and the techniques used to detect and prevent them. Overall, the combination of theory, labs, and the booking system project gave me a much clearer picture of the security measures required to build a secure and reliable web application.

# Logbook
* Total hours spent: 44,5
- Github repo and logbook: 0,5
- SQL injection: 14
- Authentication: 5
- Access control vulnerabilities: 1,5
- Phase 1: 10
- Phase 2: 6
- Phase 3: 7,5
