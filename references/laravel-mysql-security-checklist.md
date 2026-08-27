# Laravel / MySQL Security Checklist

**Domain Name:** ______  **Project ID:** ______

| # | Security Aspect | Checklist Item | Verify | Status |
|---|---|---|---|---|
| 1 | Laravel Configuration | Set `APP_DEBUG=false` in production | coding | |
| 2 | | Set a strong `APP_KEY` | coding | |
| 3 | | Use `.env` file for sensitive configuration | coding | |
| 4 | Authentication & Authorization | Use Laravel's built-in authentication scaffolding | coding | |
| 5 | | Implement role-based access control (RBAC) | coding | |
| 6 | | Enforce password complexity and 2FA where possible | coding | |
| 7 | Input Validation & Sanitization | Use Laravel validation for all form inputs | coding | |
| 8 | | Sanitize data before output to avoid XSS | coding | |
| 9 | Database Security (MySQL) | Use strong, unique MySQL user credentials | server side | |
| 10 | | Limit MySQL user privileges (least-privilege principle) | server side | |
| 11 | | Regularly update MySQL to the latest stable version | server side | |
| 12 | CSRF Protection | Use Laravel's CSRF tokens on all forms | coding | |
| 13 | HTTPS / SSL | Enforce HTTPS with middleware and server configuration | coding/server | |
| 14 | Security Headers | Add headers like X-Frame-Options, X-Content-Type-Options, and Content-Security-Policy | coding | |
| 15 | File & Directory Permissions | Set correct permissions for `storage` and `bootstrap/cache` (e.g., 755, 644) | server side | |
| 16 | Error Handling | Hide detailed errors in production | coding | |
| 17 | Rate Limiting | Use Laravel rate-limiting middleware for APIs and logins | coding | |
| 18 | Session Security | Use secure, HTTP-only, and same-site cookies | coding | |
| 19 | Logging & Monitoring | Monitor logs for suspicious activity | server side | |
| 20 | Dependency Management | Regularly update Laravel and third-party packages (`composer update`) | coding/server | |
| 21 | Database Backups | Secure and automate backups; ensure backups are encrypted | server side | |
| 22 | Server Security | Disable unnecessary services and ports | server side | |
| 23 | | Use a firewall and intrusion detection systems | server side | |
| 24 | Robots.txt & .htaccess | Restrict sensitive routes and files from being indexed | server side | |
| 25 | Prevent SQL Injection | Always use Eloquent / Query Builder or prepared statements | coding side | |

---

| Internal Checking done by | Verified By |
|---|---|
| Name: | Name: |
| Date: | Date: |
