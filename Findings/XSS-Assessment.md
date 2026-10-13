# Finding: Cross-Site Scripting (XSS) Assessment

## Summary

Cross-Site Scripting (XSS) is a web application vulnerability in which untrusted content is handled in a way that allows unintended script execution in a user's browser.

Common categories include:
- Reflected XSS
- Stored XSS

The category depends on how the input reaches the browser and how it is processed.

## Test Environment

- Application: DVWA
- Environment: Local training lab
- Module tested: Reflected XSS and Stored xss
- DVWA security level: Low

## Testing Procedure

1. Open the local DVWA application and log in.
2. Navigate to the selected XSS module.
3. Record the security level and normal behavior.
4. Use a harmless test payload in the lab.
5. Observe whether the browser displays the input as text or executes it.
6. For stored XSS, inspect whether the result remains visible after reloading the page.
7. Save screenshots showing the test input and observed result.

## Observed Result

Choose the description that matches your evidence:
- The input was displayed as ordinary text.
- The input was rejected or modified.
- The browser executed the harmless test script.
- The result could not be confirmed.

Do not claim XSS was found unless script execution or other convincing evidence demonstrates the vulnerability.

## Security Impact

If XSS is confirmed, potential consequences may include:
- Performing actions in a user's browser under the application's origin
- Displaying misleading content
- Accessing page data available to the injected script
- Interfering with user interactions

Actual impact depends on the application, browser protections, session controls, and the type of XSS.

## Mitigations

1. Apply context-aware output encoding.
2. Use safe templating features and avoid unsafe DOM manipulation.
3. Sanitize HTML when the application intentionally accepts HTML content.
4. Validate input on the server where appropriate.
5. Use Content Security Policy as an additional defense, not as a replacement for safe output handling.
6. Review cookie settings, including `HttpOnly`, `Secure`, and `SameSite`, where appropriate.


## Conclusion

This assessment examined how DVWA handled user-controlled content in the selected module. The conclusion must be based on the actual browser result and retained evidence.
