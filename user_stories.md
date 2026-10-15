# User Story Template

**Title:**
_As a [user role], I want [feature/goal], so that [reason]._

**Acceptance Criteria:**
1. [Criteria 1]
2. [Criteria 2]
3. [Criteria 3]

**Priority:** [High/Medium/Low]
**Story Points:** [Estimated Effort in Points]
**Notes:**
- [Additional information or edge cases]

---

# Admin User Stories

## User Story 1: Admin Login
**Title:**
_As an Admin, I want to log into the portal with my username and password, so that I can manage the platform securely._

**Acceptance Criteria:**
1. Admin can enter username and password on the login page.
2. System validates credentials and grants access upon successful login.
3. Error message is displayed for invalid credentials.

**Priority:** High  
**Story Points:** 3  
**Notes:** Ensure password is encrypted during transit and authentication.

---

## User Story 2: Admin Logout
**Title:**
_As an Admin, I want to log out of the portal, so that I can protect system access._

**Acceptance Criteria:**
1. Logout option is accessible from all admin dashboard pages.
2. Clicking logout ends the session and redirects to the login screen.
3. Navigating back using the browser history does not re-authenticate without logging in.

**Priority:** High  
**Story Points:** 1  
**Notes:** Clear all session tokens upon logout.

---

## User Story 3: Add Doctors
**Title:**
_As an Admin, I want to add doctors to the portal, so that patients can book appointments with them._

**Acceptance Criteria:**
1. Form is provided to enter doctor details (name, specialization, email, availability).
2. System validates that required fields are filled correctly.
3. New doctor profile is saved to the database and displayed in the portal list.

**Priority:** Medium  
**Story Points:** 5  
**Notes:** Ensure email addresses are unique across doctor profiles.

---

## User Story 4: Delete Doctor Profile
**Title:**
_As an Admin, I want to delete a doctor's profile from the portal, so that outdated or inactive doctors are removed._

**Acceptance Criteria:**
1. Option to delete profile is available on doctor detail views.
2. Confirmation dialog appears prior to permanent deletion.
3. Doctor record is removed or marked inactive in the system.

**Priority:** Medium  
**Story Points:** 3  
**Notes:** Check for active appointments before allowing deletion.

---

## User Story 5: View Monthly Usage Statistics
**Title:**
_As an Admin, I want to run a stored procedure in MySQL CLI to get the number of appointments per month, so that I can track usage statistics._

**Acceptance Criteria:**
1. Stored procedure exists in MySQL database to query appointment counts per month.
2. Admin can execute the query via MySQL CLI.
3. Query returns accurate aggregate monthly appointment figures.

**Priority:** Low  
**Story Points:** 5  
**Notes:** Optimize query execution on large appointment datasets.


---

# Patient User Stories

## User Story 6: View Doctors Without Logging In
**Title:**
_As a Patient, I want to view a list of doctors without logging in, so that I can explore options before registering._

**Acceptance Criteria:**
1. Publicly accessible doctor directory page.
2. Displays doctor names, specializations, and qualifications.
3. Prompts user to sign up or log in when trying to initiate a booking.

**Priority:** High  
**Story Points:** 3  
**Notes:** Allows prospective users to browse before committing to an account.

---

## User Story 7: Patient Sign Up
**Title:**
_As a Patient, I want to sign up using my email and password, so that I can book appointments._

**Acceptance Criteria:**
1. Registration form accepts email and password inputs.
2. System validates email format and password strength requirements.
3. New patient profile is stored in the database.

**Priority:** High  
**Story Points:** 3  
**Notes:** Send a confirmation message upon successful registration.

---

## User Story 8: Patient Login
**Title:**
_As a Patient, I want to log into the portal, so that I can manage my bookings._

**Acceptance Criteria:**
1. Login interface accepts registered email and password.
2. Authentication verifies credentials and opens the patient dashboard.
3. Appropriate error messages appear for incorrect credentials.

**Priority:** High  
**Story Points:** 2  
**Notes:** Secure login sessions using tokens or cookies.

---

## User Story 9: Patient Logout
**Title:**
_As a Patient, I want to log out of the portal, so that I can secure my account._

**Acceptance Criteria:**
1. Logout option is clearly visible on the patient dashboard.
2. Selecting logout destroys the active session.
3. User is redirected to the public home page.

**Priority:** High  
**Story Points:** 1  
**Notes:** Ensure sensitive data is inaccessible via the back button after logging out.

---

## User Story 10: Book an Appointment
**Title:**
_As a Patient, I want to log in and book an hour-long appointment, so that I can consult with a doctor._

**Acceptance Criteria:**
1. Patient can view doctor availability calendars.
2. System allows selecting a 1-hour time slot for consultation.
3. Booking is successfully recorded and linked to the patient profile.

**Priority:** High  
**Story Points:** 5  
**Notes:** Prevent double-booking for the same doctor and time slot.

---

## User Story 11: View Upcoming Appointments
**Title:**
_As a Patient, I want to view my upcoming appointments, so that I can prepare accordingly._

**Acceptance Criteria:**
1. Dedicated section on the dashboard for scheduled appointments.
2. Displays date, time, and assigned doctor details.
3. Updates dynamically if an appointment is modified or cancelled.

**Priority:** Medium  
**Story Points:** 3  
**Notes:** Sort appointments chronologically by date and time.


---

# Doctor User Stories

## User Story 12: Doctor Login
**Title:**
_As a Doctor, I want to log into the portal, so that I can manage my appointments._

**Acceptance Criteria:**
1. Login screen accepts registered doctor credentials.
2. Successful login grants access to doctor-specific dashboard.
3. Appropriate error message appears on failure.

**Priority:** High  
**Story Points:** 2  
**Notes:** Ensure credentials match verified doctor accounts created by Admin.

---

## User Story 13: Doctor Logout
**Title:**
_As a Doctor, I want to log out of the portal, so that I can protect my data._

**Acceptance Criteria:**
1. Logout button is accessible on doctor dashboard.
2. Selecting logout destroys active session.
3. Redirects to public landing page.

**Priority:** High  
**Story Points:** 1  
**Notes:** End session securely to prevent unauthorized clinical access.

---

## User Story 14: View Appointment Calendar
**Title:**
_As a Doctor, I want to view my appointment calendar, so that I can stay organized._

**Acceptance Criteria:**
1. Calendar view displays booked, pending, and completed slots.
2. Filter or switch views between daily, weekly, and monthly views.
3. Selecting an appointment opens detailed view.

**Priority:** High  
**Story Points:** 3  
**Notes:** Real-time sync with patient booking schedules.

---

## User Story 15: Mark Unavailability
**Title:**
_As a Doctor, I want to mark my unavailability, so that patients only see available slots._

**Acceptance Criteria:**
1. Interface allows selecting specific dates or time ranges as unavailable.
2. System blocks patient bookings during marked unavailable slots.
3. Changes update availability calendar instantly.

**Priority:** Medium  
**Story Points:** 3  
**Notes:** Notify patients if existing bookings overlap with new unavailability blocks.

---

## User Story 16: Update Doctor Profile
**Title:**
_As a Doctor, I want to update my profile with specialization and contact information, so that patients have up-to-date information._

**Acceptance Criteria:**
1. Profile edit form allows updating phone, specialization, and bio.
2. Input validation ensures complete data before saving.
3. Updated details immediately reflect in the doctor directory.

**Priority:** Medium  
**Story Points:** 2  
**Notes:** Protect core identifying fields like medical license number from unauthorized edits.

---

## User Story 17: View Patient Details
**Title:**
_As a Doctor, I want to view patient details for upcoming appointments, so that I can be prepared._

**Acceptance Criteria:**
1. Clicking an upcoming appointment shows patient summary (name, age, contact).
2. Displays past appointment history or consultation notes if available.
3. Adheres to privacy standards restricting view to assigned patients only.

**Priority:** High  
**Story Points:** 3  
**Notes:** Restrict patient data access to authorized treating doctors only.
