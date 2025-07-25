# JINHE
# GPT Agent Appointment & Staff Management System

This repository is designed for use with GPT Agents (Gemini, ChatGPT Code Interpreter, etc.) to collaboratively build a responsive appointment, staff, and customer management system. The system supports multiple user roles and integrates scheduling, check-in, and financial reports.

## 🧱 Tech Stack

- React + Tailwind CSS (frontend)
- Firebase (Firestore + Auth)
- React Big Calendar
- Recharts (for pie chart analytics)
- React Hook Form + Yup/Zod (for validation)
- Drag & drop: react-beautiful-dnd or dnd-kit

## 🔐 Features Overview

- Role-based permissions: Admin, Manager, Receptionist, Sales, Employee
- Customer form builder (drag-and-drop)
- Appointment booking with conflict detection and shift matching
- Shift scheduler + appointment calendar integration
- Check-in, payment lock and audit trail
- Financial report with Pie Chart + detail view
- Client attribution to Sales for performance tracking

## 🧠 GPT Agent Instructions

Please infer the architecture from this README.

- All data must sync with Firestore in real-time
- Each page must split logic layers (fetch, state, render)
- Show only work hours in calendar: 09:00–21:00
- Appointment slots must be 15-minute intervals
- After payment, lock all data from edit/delete (set `locked: true`)
- Log all actions (create/update/delete) for later audit
- UI must always show friendly loading and error state
- Do not rely on frontend cache alone — Firestore is the single source of truth

## 📄 Full Spec (中文規格文件)

Please refer to [`docs/spec.zh.md`](./docs/spec.zh.md) for full requirements in Traditional Chinese.
