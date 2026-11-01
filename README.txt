DentaCare - Smart Dental Clinic Management System
=====================================================

A modern front-end web application prototype for outpatient dental clinics.
It features Role-Based Access Control (RBAC) ensuring patient medical privacy
while giving dentists and administrative staff a dedicated clinical console.

Getting Started:
----------------
Double-click `index.html` or open it in any modern browser (Chrome, Edge, Firefox, Safari).

Dual-Portal Architecture (Privacy & Security):
----------------------------------------------
1. Public / Patient Portal:
   - Online Appointment Booking: Public visitors can book an appointment on `appointment.html`.
     Upon confirmation, the system automatically assigns a unique sequential Patient ID (e.g. `DC1028`)
     and creates their patient health record in LocalStorage.
   - Immediate Portal Login: The booking confirmation slip features their Unique Patient ID with:
     * One-Click "Log In to Patient Portal Now" button.
     * "Copy Patient ID" button.
     * Direct link to `login.html?tab=patient&id=DC1028` with pre-filled credentials.
   - Privacy Guard: Patients can ONLY view their own personal medical timeline and appointments.
     All doctor dashboards, other patients' records, medical allergies, and clinical managers are blocked.
   - Login Credentials: Log in on `login.html` with your assigned Patient ID (e.g. `DC1024`, `DC1028`)
     or registered phone number.

2. Doctor & Clinical Staff Portal (Protected):
   - Navigation: Dashboard, Patients Directory, Appointments Roster, Treatment Plans, Timelines, Follow-Ups.
   - Access: Open `login.html`, select "Doctor / Staff", enter `doctor@dentacare.demo` and PIN `1234`.
   - Guarded Routes: Any attempt to access `dashboard.html`, `patients.html`, `treatments.html`, or `followups.html`
     without doctor credentials automatically redirects to `login.html` with a privacy notice.

Project Structure:
------------------
├── index.html          - Public clinic homepage & specialty highlights
├── login.html          - Dedicated dual-role login portal (Doctor vs Patient)
├── dashboard.html      - [Staff Only] Clinical operations console, KPIs & operatory status
├── patients.html       - [Staff Only] Patient directory with medical alerts & registrations
├── registration.html   - [Staff Only] Quick registration portal
├── appointment.html    - Interactive appointment desk with doctor cards & time chips
├── treatments.html     - [Doctor Only] Diagnosis, procedural stages & progress tracker
├── history.html        - Patient care timeline (locked to individual patient for privacy)
├── followups.html      - [Staff Only] Postoperative recall & review scheduler
├── services.html       - Public catalog of clinical dental specialties
├── about.html          - Public doctor roster, qualifications & clinic values
├── contact.html        - Clinic address, helpline, emergency notes & inquiry form
├── css/
│   └── style.css       - Plus Jakarta Sans typography, SaaS elevation & responsive styling
├── js/
│   └── script.js       - Role authentication, privacy guards, CRUD & LocalStorage
└── README.txt          - Project documentation

Default Evaluation Credentials:
-------------------------------
- Doctor Login:  `doctor@dentacare.demo`  |  PIN: `1234`
- Patient Login: Patient ID: `DC1024` (or any newly generated ID e.g. `DC1028`)  |  Phone: `+91 98765 11001`

Technology:
-----------
HTML5, CSS3 (CSS Variables, Flexbox, Grid), Modern JavaScript (ES6+), Browser LocalStorage.
