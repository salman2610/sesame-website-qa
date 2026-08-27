# Cybersecurity Checklist

**Domain Name:** ______  **Project ID:** ______

| # | Activity (Cybersecurity) | Status |
|---|---|---|
| 1 | Internal and external **vulnerability scanning** using tools like Nikto, Nuclei, WPScan | |
| 2 | **Security header audit**: HSTS, CSP, X-Frame-Options, X-Content-Type-Options, etc. | |
| 3 | **Dependency review**: analyze `npm audit` / `composer audit`; track and assess CVEs | |
| 4 | Perform **penetration testing / manual review** for OWASP Top 10 issues | |
| 5 | Conduct **subdomain and exposure scan** for leaked dev/staging URLs, admin panels, etc. | |
| 6 | Use **SSL Labs / TLS test** to verify an A+ grade and confirm weak ciphers are removed | |
| 7 | Check for **credential/file exposure**: `.env`, `.git/`, `.sql`, `.zip`, `backup.bak`, etc. | |
| 8 | Provide **final security sign-off** after verifying all checklists and risk closure | |
| 9 | Conduct **threat modeling and risk mapping** to identify high-risk components | |
| 10 | Validate **Content-Security-Policy (CSP)** using `report-uri` or `report-to` endpoints | |
| 11 | Ensure a **`security.txt`** file is present to support coordinated vulnerability disclosure | |
| 12 | Confirm **rate-limiting / anti-automation** protections on login, contact forms, etc. | |
| 13 | Test **logout / session expiration** behavior across devices and tabs | |
| 14 | Review **third-party JS/CDN** includes for SRI (Subresource Integrity) and trustworthiness | |
| 15 | Check **API responses** for overexposure (excess user info, debug fields, etc.) | |
| 16 | Ensure **no secrets or credentials** exist in client-side code or source maps | |

---

| Internal Checking done by | Verified By |
|---|---|
| Name: | Name: |
| Date: | Date: |
