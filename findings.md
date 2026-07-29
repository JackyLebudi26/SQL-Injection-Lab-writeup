# Security Findings

## Summary

The lab demonstrated how insecure handling of user input can expose a web application to SQL Injection. The vulnerability occurred because user-controlled input could influence the database query without adequate input handling or parameterisation.

## Finding 1: Insufficient Input Validation

User input was accepted without sufficient validation. This increased the risk of unexpected input affecting the application's database query.

### Potential Impact

An attacker could attempt to:

- Bypass application controls.
- Access information without authorisation.
- Manipulate database queries.
- Expose sensitive information.
- Affect the confidentiality and integrity of stored data.

### Evidence

Relevant evidence is available in the `screenshots` folders and the full report in the `writeup` folder.

## Finding 2: Insecure Database Query Handling

The application appeared to construct database queries using user-controlled input instead of safely separating the SQL command from the supplied data.

### Potential Impact

If exploited in a real environment, this weakness could lead to:

- Unauthorised data access.
- Authentication bypass.
- Modification or deletion of data.
- Disclosure of database information.
- Further compromise of the application.

## Finding 3: Information Disclosure

Application responses or error messages may reveal information about the database or query structure.

### Potential Impact

Detailed error messages can assist an attacker in understanding the underlying application and database configuration.

## Overall Risk

SQL Injection is a serious web application vulnerability because it may allow unauthorised interaction with the database. The actual level of risk depends on the affected functionality, the sensitivity of the information, and the permissions assigned to the application's database account.
