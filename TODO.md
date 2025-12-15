# Splitwise Advanced - Project Roadmap

This document outlines the tasks and features for building an advanced MERN stack application similar to Splitwise.

## Phase 1: Project Setup & Configuration
- [ ] **Repository Initialization**
    - [ ] Initialize Git repository
    - [ ] Create `.gitignore` for MERN stack
- [ ] **Backend Setup**
    - [ ] Initialize Node.js project (`npm init`)
    - [ ] Install core dependencies (`express`, `mongoose`, `dotenv`, `cors`)
    - [ ] Set up basic server structure (`server.js`, `app.js`)
    - [ ] Configure ESLint and Prettier
- [ ] **Frontend Setup**
    - [ ] Initialize React app (Vite recommended for performance)
    - [ ] Install Tailwind CSS and configure
    - [ ] Install state management library (Redux Toolkit or Zustand)
    - [ ] Setup React Router for navigation

## Phase 2: User Authentication & Security
- [ ] **Backend Auth**
    - [ ] Design User Schema (Name, Email, PasswordHash, Avatar, etc.)
    - [ ] Implement Registration API (Hash passwords with bcrypt)
    - [ ] Implement Login API (Generate JWT)
    - [ ] Middleware for JWT verification
    - [ ] Password Reset functionality (via Email)
- [ ] **Frontend Auth**
    - [ ] Create Login Page
    - [ ] Create Registration Page
    - [ ] Implement Protected Routes
    - [ ] Persist auth state (Local storage/Cookies)

## Phase 3: Core Logic & Database Design
- [ ] **Database Schema Design**
    - [ ] **User Model**: Profile info, friends list
    - [ ] **Group Model**: Members, expenses, category
    - [ ] **Expense Model**: Payer, amount, split details (exact, percentage, equal), date, currency
    - [ ] **Settlement Model**: Record of payments between users
- [ ] **Expense Logic API**
    - [ ] Create Expense API (Calculate individual shares)
    - [ ] Feature: Support for "Equal", "Exact Amounts", and "Percentage" splits
    - [ ] Edit/Delete Expense API (Recalculate balances)
- [ ] **Group API**
    - [ ] Create Group
    - [ ] Add/Remove Members
    - [ ] Get Group details with balances

## Phase 4: Frontend Core Features
- [ ] **Dashboard**
    - [ ] Display "Total Balance", "You Owe", "You are Owed"
    - [ ] Recent Activity Stream
- [ ] **Group Management UI**
    - [ ] List of groups
    - [ ] Group details view
    - [ ] Add new expense modal
- [ ] **Friend Management**
    - [ ] Add friend by email
    - [ ] Non-group expenses (direct splits)

## Phase 5: Email Notification System (Key Feature)
- [ ] **Backend Email Service**
    - [ ] **Option A (Modern & Recommended)**: Setup [Resend](https://resend.com) (Great DX, allows writing emails in React)
    - [ ] **Option B (Classic)**: Setup Nodemailer with a provider like SendGrid, Mailgun, or Brevo
    - [ ] Create Email Templates (Welcome, New Expense, Monthly Summary, Reminder)
- [ ] **Triggers**
    - [ ] Send email when added to a group
    - [ ] Send email when added to an expense
    - [ ] **Feature**: "Remind Friend" button to send settlement reminder emails

## Phase 6: Advanced Features
- [ ] **Settlement Algorithm**
    - [ ] Minimize transactions logic (Simplify debts algorithm)
- [ ] **Visualization**
    - [ ] Charts/Graphs using Recharts or generic Chart.js
    - [ ] "Spending Habits" visualized by category
- [ ] **Recurring Expenses**
    - [ ] Scheduler for rent, subscription bills
- [ ] **Export Data**
    - [ ] Export group expenses to PDF or CSV
- [ ] **Multi-currency Support**
    - [ ] Integration with currency conversion API

## Phase 7: Deployment & Polish
- [ ] **Testing**
    - [ ] Unit tests for split logic (Jest)
    - [ ] Integration tests for API
- [ ] **Deployment**
    - [ ] Backend: Render/Heroku/AWS
    - [ ] Frontend: Vercel/Netlify
    - [ ] MongoDB Atlas setup
