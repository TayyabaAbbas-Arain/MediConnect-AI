MediConnect AI — Shared Frontend Kit
This shared frontend repository is designed for the frontend development team (Auth Module, Patient/Doctor Module, Admin Module). The core objective is to ensure that while different developers build separate modules, the final application maintains a unified, seamless user experience and consistent product identity.

📂 Repository Structure
Plaintext
TayyabaAbbasArain-Frontend-Intern/
├── design-system.css       <- Global design tokens: colors, typography, buttons, inputs, cards, 
│                              badges, tables, and layout styles. Import this; do not reinvent.
├── component-sheet.html    <- Live interactive style guide and preview of all UI components.
├── partials/
│   ├── header-public.html    <- Public/landing page header (Assigned to Member 1)
│   ├── sidebar-patient.html  <- Patient dashboard sidebar navigation (Assigned to Member 2)
│   ├── sidebar-doctor.html   <- Doctor dashboard sidebar navigation (Assigned to Member 2)
│   ├── sidebar-admin.html    <- Admin panel sidebar navigation (Assigned to Member 3)
│   └── footer.html           <- Shared footer component (Standardized across all modules)
└── *.html                  <- Various module view files (Login, Dashboards, Signups, etc.)
