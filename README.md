# Bankingsystem

1.Key Concepts and Tools

Spring Boot: To build REST APIs.
Spring Security: For authentication and authorization (role-based access control).
JPA (Hibernate): For ORM and database interaction.
MySQL: As the relational database.
PDFBox/Apache POI: For generating account statements in PDF format.
JWT: For secure user authentication.
Validation: For input validation using annotations like @NotNull, @Email.
Internationalization (i18n): Support for multiple currencies.

2.Features Implementation
a.User Registration and Login (Role-Based Access)
Users Table: Stores user information with roles (USER, ADMIN).
Implement Spring Security with JWT for token-based authentication.

b.CRUD Operations for Accounts
Accounts Table: Store account information (account number, type, balance).
APIs for:
Create a new account.
Fetch account details.
Update account information.
Delete account (soft delete).

c.Money Transfers
Transactions Table: Logs all transactions (debit/credit).
Implement business logic for:
Verifying sufficient balance.
Transferring money between accounts (same/different users).
Deducting fees for international transactions.

d.Monthly Account Statements
Use Apache PDFBox to generate statements.
Include transaction details filtered by date and type.

e.OTP Authentication
Use a utility class to generate random OTPs.
Send OTP via email or SMS (can use Twilio or SMTP).

f.International Transactions
Add a Currency Conversion API (e.g., from an external service like Forex API).
Handle conversion rates dynamically before transferring amounts.
