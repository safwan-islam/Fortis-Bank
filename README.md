<h1 align="center">🏦 Fortis Bank</h1>

<p align="center">
  <strong>Banking Management System</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/JDBC-007396?style=flat-square&logo=java&logoColor=white" />
  <img src="https://img.shields.io/badge/Oracle_SQL-F80000?style=flat-square&logo=oracle&logoColor=white" />
  <img src="https://img.shields.io/badge/Swing-007396?style=flat-square&logo=java&logoColor=white" />
</p>

---

## 📌 About

Fortis Bank is a desktop banking system built with a clean **3-layer architecture** (Business / Data / UI). It supports 5 account types, 3 transaction types, and a notification system — all persisted through **DAO and Repository patterns** over Oracle SQL with JDBC.

The app has two Swing interfaces: a **client portal** (login with PIN, manage accounts, view transactions) and a **manager dashboard** (create/remove clients, open/close accounts).

---

## ⚙️ Tech Stack

| Layer | Technology |
|:------|:-----------|
| **Language** | Java |
| **Database** | Oracle SQL (10 tables) |
| **Connectivity** | JDBC |
| **UI** | Swing (Login + Client + Manager views) |
| **Architecture** | 3-Layer (Business / Data / UI) |
| **Patterns** | DAO, Repository, Interface-based contracts |

---

## 🏗️ Architecture

```
┌──────────────────────────────────────────────┐
│                  UI Layer                     │
│  BankAppLoginSwing → BankAppClientSwing       │
│                    → BankAppGestionnaireSwing  │
├──────────────────────────────────────────────┤
│               Business Layer                  │
│  BankAccount (abstract)                       │
│  ├── CheckingAccount                          │
│  ├── SavingsAccount                           │
│  ├── CreditAccount                            │
│  ├── LineOfCredit                             │
│  └── ForeignCurrencyAccount                   │
│  BankClient (IBankClient)                     │
│  BankManager (IBankManager)                   │
│  Transaction (abstract)                       │
│  ├── Deposit                                  │
│  ├── Withdrawal                               │
│  └── Transfer                                 │
│  Notification (INotification)                 │
├──────────────────────────────────────────────┤
│                Data Layer                     │
│  DatabaseConnection                           │
│  BankAccountDAO  (IBankAccountRepository)     │
│  BankClientDAO   (IBankClientRepository)      │
│  BankManagerDAO  (IBankManagerRepository)     │
│  TransactionDAO  (ITransactionRepository)     │
│  NotificationDAO (INotificationRepository)    │
├──────────────────────────────────────────────┤
│              Oracle SQL Database              │
└──────────────────────────────────────────────┘
```

---

## 🗄️ Database Schema

**10 tables** on Oracle SQL:

| Table | Description |
|:------|:------------|
| `BankClient` | Clients (name, PIN, address, email, phone) |
| `BankManager` | Managers with role |
| `BankAccount` | Base account (balance, creation date, client FK) |
| `CheckingAccount` | Extends BankAccount — free transactions limit |
| `SavingsAccount` | Extends BankAccount — interest rate |
| `CreditAccount` | Extends BankAccount — credit limit + interest |
| `LineOfCredit` | Extends BankAccount — credit limit + interest |
| `ForeignCurrencyAccount` | Extends BankAccount — currency + exchange rate |
| `Transaction` | Deposit / Withdrawal / Transfer with destination account |
| `Notification` | Messages tied to accounts and clients |

---

## 🚀 Features

- **5 Account Types** — Checking, Savings, Credit, Line of Credit, Foreign Currency
- **3 Transaction Types** — Deposit, Withdrawal, Transfer (with destination account)
- **Client Portal** — Login with firstname + PIN, view accounts, perform transactions, view history
- **Manager Dashboard** — Create/remove clients, open/close accounts, view all clients
- **Notification System** — Alerts for deposits, negative balances, and more
- **Interface Contracts** — `IBankClient`, `IBankManager`, `INotification`, `IBankAccountRepository`, `IBankClientRepository`, `IBankManagerRepository`, `ITransactionRepository`, `INotificationRepository`
- **PIN Validation** — 4-digit PIN enforced via `CHECK` constraint with regex

---

## 📦 Getting Started

### Prerequisites

- Java JDK 8+
- Oracle SQL Database
- Eclipse / IntelliJ IDEA

### Setup

1. Clone the repo
   ```bash
   git clone https://github.com/safwan-islam/Fortis-Bank.git
   ```
2. Run `fortisbankdb.sql` in Oracle SQL to create all tables and seed data
3. Import the project into your IDE
4. Update `DatabaseConnection.java` with your Oracle credentials
5. Run `BankAppLoginSwing.java`

### Default Credentials

| User | Login | PIN/Role |
|:-----|:------|:---------|
| Client 1 | Safwan | `1234` |
| Client 2 | Houria | `5678` |
| Manager | Admin Fortis | Gestionnaire |

---

## 👤 Author

**Safwan-Ahmed Islam** — [GitHub](https://github.com/safwan-islam) · [LinkedIn](https://linkedin.com/in/safwan-islam)
