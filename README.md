# GPT Agent Appointment & Staff Management System

This project is designed for GPT Agents (Gemini, ChatGPT Code Interpreter, etc.) to collaboratively build a cross-device internal web application for appointment, staff, and customer management. It supports customisable roles, permission control, calendar scheduling, payment locking, and report analytics.

## 🧱 Tech Stack

- React + Tailwind CSS (frontend)
- Firebase Firestore + Firebase Auth (data layer)
- React Big Calendar (appointment and shift views)
- Recharts (pie chart and performance reports)
- Yup or Zod + React Hook Form (form validation)
- Drag-and-drop: react-beautiful-dnd or dnd-kit

## 🧠 GPT Agent Instructions

Please infer the architecture and implement features based on this README and the linked spec file.

- Use React functional components, modular by page
- Sync all state and data with Firestore in real time
- Calendar only displays **09:00 to 21:00**, with **15-minute intervals**
- All changes (create/edit/delete) must write a log entry
- Prevent double-booking by checking real-time shift and appointment data
- After payment is completed, set `locked: true` and disable all UI edits
- User roles and permissions must be enforced both in UI and Firestore rules
- Client form fields are fully customisable and sortable by drag-and-drop
- Reports must match Firestore and support Excel export
- Deletion must refresh the UI; stale state is not allowed

## 👥 User Roles

Custom roles are supported. The `administrator` can add, edit or delete any role and assign permissions.

### Default roles (can be edited or removed):
- Administrator: full access
- Manager: appointments and scheduling
- Receptionist: create clients and appointments
- Employee: view personal schedule
- Business Manager: view report based on referrals

Each permission is assigned using granular keys like:
- `appointment:create`
- `client:form_design`
- `report:read_referrer`

## 📁 File Structure Suggestion

