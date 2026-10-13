# Finding: SQL Injection Assessment

## Summary

SQL injection occurs when an application places untrusted user input into a database query without appropriate safeguards. Depending on the implementation, an attacker may be able to alter query logic and access or modify information beyond the intended request.

## Test Environment

- Application: DVWA
- Environment: Local training lab
- Module: SQL Injection
- Test input: `1' OR '1' = '1`
- Date tested: 10-10-2026

## Testing Procedure

1. Open the local DVWA application.
2. Log in using the lab's configured credentials.
3. Navigate to the SQL Injection module.
4. Record the DVWA security level.
5. Enter the test input in the intended input field.
6. Submit the input and observe the response.
7. Compare the response with a normal input.
8. Save screenshots of the test and its result.

## Observed Result

During earlier testing, the response appeared to display multiple records, including names such as admin and other sample DVWA users.
## Security Impact

If the behavior confirms SQL injection, possible impacts may include:
- Unauthorized retrieval of database records
- Bypassing intended query conditions
- Exposure of sensitive information stored in the database
- Data modification or deletion, depending on database permissions and the vulnerable query

The actual impact depends on the vulnerable code, database privileges, and application configuration.

## Preliminary Severity

Security Level: Low

Do not assign a final severity solely because a test string was submitted. Confirm that the response demonstrates unintended query behavior.

## Mitigations

1. Use parameterized queries or prepared statements.
2. Avoid constructing SQL statements by concatenating user input.
3. Apply server-side input validation as a supporting control.
4. Use a database account with only the permissions required by the application.
5. Avoid returning detailed database errors to users.
6. Add security regression tests for the affected input.

## Conclusion

The assessment investigated whether user-controlled input could alter the intended database query in the local DVWA training environment. The final finding and severity must reflect the observed response and available evidence.
