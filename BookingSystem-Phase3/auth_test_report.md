#  Authorization Test Report  
Phase 3 - Role-Based Access Control Evaluation

## Tested Roles
- **Guest** (not logged in)
- **Reserver** (standard user)
- **Administrator** (privileged user)

## Purpose of This Report
This document evaluates **what each role can and cannot do** in the current implementation of the booking system.  
Findings are based on:

- Browser testing  
- ZAP scanning  
- wfuzz endpoint discovery  
- Comparison with official specifications (points 1-10)

The goal is to confirm whether **authorization is correctly enforced** and whether the system aligns with **GDPR** and **Privacy by Design** principles.

---

# Discovered Pages & Endpoints

List **all** pages, directories, and API endpoints discovered via:
- Manual browsing  
- ZAP  
- Gobuster / wfuzz  

## Pages:
|  **Page**                       | **Description**         | **Source** |
|---------------------------------|-------------------------|------------|
|  http://localhost:8004/     |  Public Homepage  |  Browser  |
|  http://localhost:8004/login  |  Login form  |  Browser  |
|  http://localhost:8004/register  |  Regristration form  | Browser |
|  http://localhost:8004/resources  |  Add resources form  | Browser |
|  http://localhost:8004/logout  |  Logouts the user and sends him to Homepage  | wfuzz |
|  http://localhost:8004/reservation  |  reservation form | Browser

## API:
|  **Endpoint**                       |   **Method**   |      **Description**         | **Source** |
|---------------------------------|-------------------------|------------|--------------------|
|  http://localhost:8004/api/resources     |  GET  |  Lists the resources  |  Browser  |
|  http://localhost:8004/api/reservations  | GET |  Lists the reservations  |  Browser  |
|  http://localhost:8004/api/reservations/("reservation_id")  | GET |  Shows the reservation that matches the "reservation_id"  | Browser |
|  http://localhost:8004/api/users   | GET | Lists the users | Browser |
|  http://localhost:8004/api/session   | GET | Check whether the user is currently logged in | wfuzz |

### NOTE!: No /admin sites or /api/admin/ endpoints were discovered neither manually, with zap or wfuzz

---

# Guest Role (Not Logged In)

## CAN DO 🚩(High Severity)⚠️(Medium Severity)🟢(Ok)
- View public resource list - `/` - 🟢 Spec 1
- Access login form - `/login` - 🟢 Spec 2
- Access register form - `/register` - 🟢 Spec 2
- View registered reservations without identifying  - `/` - 🟢 Spec 8
- Access resources form and add a resource - `/resources` - ⚠️ A Guest should not be able to do this according to Spec 3 and the link is not clickable from the homepage if not logged in as an user. 
- View the resources API - `/api/resources` -  ⚠️ Shouldn't be able to see the resources endpoint. 
- View reservations endpoint - `/api/reservations` - 🟢 Spec 8
- View reservations based on the reservation id provided - `/api/reservations/("reservation_id")` - 🚩 Only the admin should be able to see the information displayed here or else it shouldn't display "reserver_token". Violates Spec 9 and 10.
- View the list of users and their tokens - `/api/users` - 🚩 Exposes personal data and unique identifiers. Violates Spec 9 and 10.

## CANNOT DO
- Acess the session endpoint - `/api/session` - 🟢 Expected behavior as the user is not logged in. 
- Cannot POST `/api/reservations` - `/api/reservations` - 🟢 Expected
- Cannot access reservation form - `/reservation` - 🟢 There is a "Unauthorized" messaged displayed.
- Cannot register if not over 15 years old - `/register` - 🟢 A message is displayed saying that must be over 15.
- Access admin-only features (none found) - ⚠️ Missing endpoints

---

# Reserver Role (Logged-In Standard User)

## CAN DO
- Everything a guest can do including accessing the endpoints that should only be accessible by the admin such as `/api/users`.
- Make a reservation - `/reservation` - 🟢 The user can make a reservation an also delete his own reservations.
- View their own reservations - `/` - 🟢 The user is able to see their own reservation and details.
- View other reserver's email - `/` - ⚠️ The user is able to see other reservations and this is normal, but violates Spec 9 and 10 because they are also able to see other reserver's email.
- Create a resource - `/resources` - 🟢 Expected, the button is clickable and they can submit the forms. 

## CANNOT DO
- Modify or delete other users reservations - 🟢 Expected
- Access admin-only features (none found) - ⚠️ Missing endpoints

---

# Administrator Role

## CAN DO
- View, edit, and delete reservations - 🟢 Spec 4
  - Editing works as intended
  - Deletion works as intended
- Access all public and reserver-level features - 🟢

## CANNOT DO
- Cannot delete users - ⚠️ Missing expected functionality (Spec 5)
- Cannot delete resources - ⚠️ Missing expected functionality (Spec 4)

## Issues / Deviations
- **No admin-only pages were found**
  - No `/admin`
  - No `/api/admin/*`
  - No admin dashboard

---

# Summary of Violations

### 🚩 Critical Issues
- `/api/users` exposes **all emails + tokens** → Violates Spec 9 & 10  
- `/api/reservations/{id}` exposes:  
  - reserver email (for all users)  
  - reserver_token  
  → Violates Spec 9 & 10  
- Reserver can see **other reservers’ emails** → GDPR breach   
- No admin endpoints exist → Spec 4 and 5 incomplete  

### ⚠️ Medium Issues  
- Guests can access internal APIs    
- Missing admin UI overall  
