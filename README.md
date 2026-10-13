# MediConnect AI — Shared Frontend Kit

Yeh folder teeno frontend developers (Auth Module, Patient/Doctor Module, Admin Module)
ke liye hai. Maqsad: sab modules alag banda banaye, phir bhi pura app EK hi product
jaisa dikhe.

## Is folder mein kya hai

```
design-system.css        <- Sab colors, fonts, buttons, inputs, cards, badges, table,
                             header/sidebar/footer styles. IMPORT KARO, DOBARA MAT LIKHO.
component-sheet.html     <- Live preview of every component. Isay browser mein khol kar dekho.
partials/
  header-public.html     <- Landing/Auth pages ke liye header (Member 1 use karega)
  sidebar-patient.html   <- Patient dashboard sidebar (Member 2 use karega)
  sidebar-doctor.html    <- Doctor dashboard sidebar (Member 2 use karega)
  sidebar-admin.html     <- Admin panel sidebar (Member 3 use karega)
  footer.html            <- Footer — TEENO modules mein bilkul same, copy-paste karo
```

## Rules (sab devs ke liye)

1. **Har HTML page ke `<head>` mein yeh line hona zaroori hai:**
   ```html
   <link rel="stylesheet" href="design-system.css">
   ```

2. **Naya button/input/card banane se pehle `component-sheet.html` check karo.**
   Agar wahan class maujood hai (`.btn-primary`, `.input`, `.card`, `.badge-success` waghera)
   to usay use karo — apna naya CSS mat likho.

3. **Colors sirf variables se use karo, hex code hardcode mat karo.**
   Galat: `background: #0A1B33;`
   Sahi: `background: var(--color-navy-900);`

4. **Header aur Footer teeno modules mein EXACT same honge** (sirf logged-in state
   mein header ke right-side buttons change honge). `partials/footer.html` ko
   copy-paste karo, khud se mat banao.

5. **Sidebar structure same rahega, sirf menu items alag** — `.app-sidebar`,
   `.menu-item`, `.menu-item.active` classes teeno modules mein identical.

6. **Naya color/font chahiye ho to pehle project lead (Shakir) se confirm karo**,
   khud se decide na karein — warna consistency toot jayegi.

## Module Assignment

| Member | Module | Pages |
|---|---|---|
| 1 | Landing + Auth | Home, Login, Signup, Patient Signup, Doctor Signup, Verification Pending, Forgot/Reset Password, Contact Us |
| 2 | Patient + Doctor Dashboards | Patient: Dashboard, Appointments, Find Doctor, Book Appointment, AI Assistant, Reports, Help & Support, Profile, BMI Calculator. Doctor: Dashboard, Schedule Manager, Appointments, Patients/Queue, Reports, Feedback, Profile |
| 3 | Admin Panel | Admin Login, Dashboard, Manage Doctors, Manage Patients, Manage Appointments, Pending Doctor Queue, Open Complaints, Reports, Site Settings |

## Har 2-3 din mein

Teeno apne screens ka screenshot Shakir ko bhejein taake side-by-side compare ho sake
ke sab ka button/color/spacing match kar raha hai ya nahi.
