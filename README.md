# Bank-System-Frontend

# Frontend Banking App

This is a **mock frontend application** for a simple banking system. It allows users to manage accounts, transfer funds, view transaction history, and simulate authentication. It uses **React**, **React Router**, **Axios**, and **Socket.io-client**.

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Folder Structure](#folder-structure)
- [Installation](#installation)
- [Available Scripts](#available-scripts)
- [Component Overview](#component-overview)
- [Service Details](#service-details)
- [Notes](#notes)

---

## Features
- **Authentication** (Mock login/register)
- **Account Management** (Create/Delete/Transfer between accounts)
- **Transaction History** (View past transactions)
- **Real-time Notifications** (Simulated via mock Socket.io)

## Folder Structure
```
/src
  |-- components/
      |-- AccountFormModal.jsx
      |-- AccountList.jsx
      |-- Button.jsx
      |-- Input.jsx
      |-- TransactionForm.jsx
  |-- pages/
      |-- Accounts.jsx
      |-- Transactions.jsx
      |-- Home.jsx
      |-- Auth.jsx
      |-- Login.jsx
      |-- Register.jsx
      |-- Requirements.jsx
  |-- services/
      |-- accountService.js
      |-- transactionService.js
      |-- notificationService.js
      |-- authService.js
```

## Installation

1. Clone the repository:
    ```bash
    git clone
    cd frontend
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Start the application:
    ```bash
    npm start
    ```

   The app will be available at `http://localhost:3000/`.


## Available Scripts

- `npm start`: Runs the app in development mode.
- `npm run build`: Builds the app for production.
- `npm test`: Launches the test runner.
- `npm run eject`: Exposes configuration files (not reversible).


## Component Overview

### `/components/`
- **AccountFormModal.jsx**: Modal form for creating a new account.
- **AccountList.jsx**: Displays a list of all user accounts with delete options.
- **TransactionForm.jsx**: Form to create new transactions.
- **Button.jsx**: Reusable button component.
- **Input.jsx**: Reusable input field component.

### `/pages/`
- **Accounts.jsx**: Account management page.
- **Transactions.jsx**: Transactions history page.
- **Home.jsx**: Landing page after login.
- **Auth.jsx**: Authentication layout.
- **Login.jsx**: Login form.
- **Register.jsx**: Registration form.
- **Requirements.jsx**: Displays basic requirements/instructions.


## Service Details

### `/services/accountService.js`
- Handles all **account operations**:
  - `getAccounts()`: Retrieve list of accounts.
  - `createAccount({ name, type })`: Create a new account.
  - `deleteAccount(accountId)`: Delete an account by ID.
  - `transferFunds(fromAccountId, toAccountId, amount)`: Transfer funds between accounts.
  - `updateAccountBalance(accountName, amount, isDebit)`: Update balance.
  - `getTransactionHistory(accountId)`: Get account's transaction history.

### `/services/transactionService.js`
- Handles **transactions**:
  - `getTransactions()`: Fetch all transactions.
  - `createTransaction({...})`: Create a new transaction.

### `/services/notificationService.js`
- Handles **mock notifications**:
  - `subscribeToNotifications(callback)`: Simulates receiving a notification after 2 seconds.

### `/services/authService.js`
- Handles **mock authentication**:
  - `login(email, password)`: Mock login.
  - `register(email, password)`: Mock register.


## Notes
- This frontend currently **uses mocked services only**. There is **no real backend** integration yet.
- `socket.io-client` connection is set to `http://localhost:3000` but is mocked for now.
- All accounts and transactions **reset upon page reload** (no persistent storage).

---

**Future Improvements**
- Connect to a real backend API.
- Add user-specific data persistence.
- Implement proper authentication flow with JWTs.
- Improve error handling and input validation.
- Add form validation and loading states.

---

> 🔗 Developed for learning/demo purposes. Not production-ready.

