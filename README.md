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

Fortis Bank is a desktop banking system built with a clean **3-layer architecture** (Business / Data / UI). It supports core banking operations — deposits, withdrawals, transfers, and transaction history — with persistence handled through **DAO and Repository patterns** over Oracle SQL, keeping data access logic fully decoupled from the business layer.

The Swing GUI connects directly to the JDBC backend through typed repository classes that centralize all queries, eliminating boilerplate across the application.

---

## ⚙️ Tech Stack

| Layer | Technology |
|:------|:-----------|
| **Language** | Java |
| **Database** | Oracle SQL |
| **Connectivity** | JDBC |
| **UI** | Swing |
| **Architecture** | 3-Layer (Business / Data / UI) |
| **Patterns** | DAO, Repository |

---

## 🏗️ Architecture

```
┌─────────────────────────────────┐
│           UI Layer              │
│         (Swing GUI)             │
├─────────────────────────────────┤
│        Business Layer           │
│    (Services, Validation)       │
├─────────────────────────────────┤
│          Data Layer             │
│   (DAO / Repository / JDBC)     │
├─────────────────────────────────┤
│         Oracle SQL DB           │
└─────────────────────────────────┘
```

---

## 🚀 Features

- **Deposits** — Add funds to any account
- **Withdrawals** — Withdraw with balance validation
- **Transfers** — Move funds between accounts
- **Transaction History** — Full audit trail of all operations
- **DAO Pattern** — Decoupled persistence logic across 5+ entity types
- **Repository Pattern** — Centralized, typed query classes reducing boilerplate
- **JDBC Integration** — Direct database connectivity with parameterized queries

---

## 📦 Getting Started

### Prerequisites

- Java JDK 8+
- Oracle SQL Database
- IDE (IntelliJ IDEA / Eclipse)

### Setup

1. Clone the repo
   ```bash
   git clone https://github.com/safwan-islam/Fortis-Bank.git
   ```
2. Import the project into your IDE
3. Configure the Oracle SQL connection in the data layer
4. Run the application

---

## 👤 Author

**Safwan-Ahmed Islam** — [GitHub](https://github.com/safwan-islam) · [LinkedIn](https://linkedin.com/in/safwan-islam)
