---
name: sesame-website-qa
description: >-
  Runs Sesame Technologies Pvt. Ltd.'s standard QA test suite against a live
  website or web application. Covers applicable cybersecurity, Laravel/MySQL
  security, Laravel/MySQL SEO, general front-end/back-end QA, functionality,
  performance, mobile responsiveness, design, accessibility, and SEO checks.
  Use this skill whenever the user asks to QA test, run the checklist, audit,
  test, review, or validate a website, site, or web application, or references
  any Sesame QA checklist. The skill is read-only: it inspects and reports
  findings and never modifies the target. Every run produces an
  Issue_Log_No_<x>.txt and a Passed_Tests.txt for human review.
---

# Sesame Website QA Test Skill

Runs Sesame Technologies Pvt. Ltd.'s standard website QA checks against a
specified website or web application.

This skill is an **auditor, not an editor**.

The skill is based on the Sesame website QC checklist and its associated
reference checklists. It covers applicable checks across:

* Front-end / general website QA
* Pages and navigation
* Contact forms
* Careers / job applications
* Gallery
* Back-end / administration
* User groups and permissions
* User management
* Career administration
* Gallery administration
* Testimonials
* Contact / enquiry management
* General functionality
* Performance and browser compatibility
* Security and privacy
* Website administration
* Mobile responsiveness
* SEO
* Design
* Accessibility and usability

The checklist is a master QA checklist. **Not every item applies to every
project.**

The agent must determine applicability before testing.

---

# 1. HARD RULE: NEVER MODIFY THE TARGET

The agent must never alter application code, configuration, database content,
infrastructure, or persistent state while running this skill.

This applies even when:

* A problem is obvious.
* The fix appears simple.
* The fix appears safe.
* The agent knows how to fix the problem.
* The user asks for the fix during the QA run.

If a problem is found:

1. Test and verify it where possible.
2. Record it as an issue.
3. Do not fix it.
4. Complete the QA run.
5. Treat any requested fix as a separate task outside this skill.

## Allowed actions

The following are permitted when appropriate:

* Read application/source files.
* Inspect project structure.
* Read configuration files without changing them.
* Run read-only commands.
* Browse the website normally.
* Browse authenticated areas using explicitly authorized credentials.
* HTTP GET/HEAD requests.
* Inspect HTTP response headers.
* View page source.
* Inspect browser DevTools.
* Inspect network requests.
* Inspect browser console errors.
* Take screenshots.
* Run vulnerability scanners in non-destructive/report-only mode.
* Run `composer audit`.
* Run `npm audit`.
* Perform SSL/TLS checks.
* Inspect `robots.txt` and `sitemap.xml`.
* Inspect metadata and structured data.
* Run performance analysis.
* Test forms using normal test inputs.
* Test validation using safe, non-destructive inputs.

## Prohibited actions

Do not:

* Edit source code.
* Patch source files.
* Modify `.env`.
* Modify application configuration.
* Modify the database.
* Run migrations.
* Insert, update, or delete database records.
* Delete files.
* Change server configuration.
* Apply scanner auto-fixes.
* Run destructive scanner modes.
* Perform denial-of-service testing.
* Perform resource-exhaustion testing.
* Brute-force credentials.
* Guess passwords.
* Attempt to obtain credentials.
* Create unauthorized accounts.
* Change user permissions.
* Change passwords.
* Intentionally disrupt availability.
* Exploit vulnerabilities in a way that could damage the application or data.
* Send malicious payloads that could alter persistent state.

Security testing must remain **non-destructive and read-only**.

---

# 2. APPLICABILITY IS MANDATORY

The Sesame checklist is a master QA checklist.

It must NOT be interpreted as a requirement that every item applies to every
website.

Before testing, determine which sections and individual items are relevant to
the target.

Consider:

* Website type.
* Technology stack.
* Available functionality.
* Public versus authenticated areas.
* Available backend/admin functionality.
* Whether the project uses Laravel.
* Whether the project uses MySQL.
* Whether the site has careers functionality.
* Whether the site has a gallery.
* Whether the site has testimonials.
* Whether the site has products.
* Whether the site has file uploads.
* Whether the site has user groups.
* Whether the site has social login.
* Whether the site has video/audio/animation.
* Whether the site has maps.
* Whether the site has forms.
* Whether the site has search.
* Whether the site has pagination.
* Whether the site has an admin/control panel.

## Examples

Career checks apply only when career/job functionality exists.

Gallery checks apply only when gallery functionality exists.

Testimonial checks apply only when testimonials are present or required.

Product, price, and stock schema checks apply only where relevant product
functionality exists.

File-upload checks apply only where file uploads exist.

User-group checks apply only where user groups or equivalent permission
management exists.

Social-login checks apply only where social login exists or is explicitly
required.

Video-caption checks apply when the site contains videos.

Audio checks apply when the site contains audio.

Laravel/MySQL-specific checks must only be run when the application actually
uses Laravel/MySQL or the relevant technology is confirmed.

## Do not fail non-applicable functionality

If a feature does not exist and there is no indication that the feature is
required, do not mark its checklist item as Failed simply because the feature
is absent.

Mark it:

`N/A`

and provide a short reason.

Example:

`[N/A] #49 — Gallery pagination — No gallery functionality exists on this
project.`

---

# 3. DO NOT ASSUME

The agent must not mark an item as Pass merely because:

* No obvious problem was noticed.
* The website appears to work normally.
* A framework normally provides the functionality.
* A library normally provides the security control.
* The source code appears to suggest that it should work.
* The feature is expected to work.
* The agent does not have enough access to verify it.

A Pass requires observable evidence that the requirement was satisfied.

If an applicable requirement cannot be verified with the available access,
mark it N/A and explain why.

Never fabricate evidence.

---

# 4. TEST STATUS

Every applicable checklist item must result in one of:

## PASS

The requirement was tested and evidence indicates that it works or is
satisfied.

## FAIL

The requirement was tested and a problem was observed.

A failed item must be recorded in `Issue_Log_No_<x>.txt`.

## N/A

The requirement does not apply to the project, or cannot be meaningfully
verified with the available access.

Always provide a short reason.

---

# 5. EVIDENCE REQUIREMENTS

Every Failed item must contain concrete, reproducible evidence.

Evidence may include:

* URL tested.
* Page or endpoint tested.
* HTTP status code.
* HTTP response header.
* Actual browser behavior.
* Actual validation message.
* Actual console error.
* Screenshot description.
* Relevant source/configuration path.
* Tool output.
* Navigation behavior.
* Form behavior.
* Performance measurement.
* SEO metadata.
* Structured-data result.
* Authentication behavior.

Do not write vague evidence such as:

`Security issue found.`

Instead write something specific such as:

`The HTTP response for / did not contain a Content-Security-Policy header.`

## Observed versus inferred

Clearly distinguish what was directly observed from what is inferred.

Do not claim that a vulnerability is exploitable unless it was actually
verified within the permitted, non-destructive scope.

For example:

Bad:

`Missing CSP means the site is vulnerable to XSS.`

Better:

`The HTTP response did not contain a Content-Security-Policy header. This
removes a browser-side defense-in-depth control.`

---

# 6. CONFIDENCE

For each issue assign:

* High
* Medium
* Low

### High

The issue was directly observed or reliably verified.

### Medium

There is strong evidence of an issue, but complete verification requires
additional access or testing.

### Low

The finding is a potential concern requiring manual verification.

If something cannot reasonably be assessed, use N/A rather than using Low
confidence.

---

# 7. SEVERITY

Use the following guidance.

### Critical

Severe security exposure, significant data exposure, or high likelihood of
serious compromise or data loss.

Examples:

* Confirmed critical security vulnerability.
* Exposed sensitive credentials.
* Unauthenticated access to highly sensitive administrative functionality.
* Confirmed SQL injection with meaningful impact.

### High

Major security gap or broken core functionality.

Examples:

* Authentication/authorization failure.
* Significant sensitive-data exposure.
* Major core workflow failure.
* Serious file-upload security issue.

### Medium

Meaningful security, usability, SEO, functionality, accessibility, or design
problem with real user or business impact.

### Low

Minor usability, cosmetic, SEO, accessibility, or best-practice deviation.

Severity must be based on actual observed impact.

---

# 8. AUTHENTICATION AND ACCESS

Use only credentials or access explicitly provided or authorized for testing.

Do not:

* Guess passwords.
* Brute-force credentials.
* Attempt to obtain credentials.
* Bypass authentication.
* Create unauthorized accounts.
* Change existing account permissions.

When authenticated access is available, test applicable authenticated
functionality in addition to the public site.

Where relevant, distinguish between:

* Unauthenticated behavior.
* Authenticated-user behavior.
* Administrator behavior.
* Different user-group permissions.

If an applicable backend check requires unavailable access, mark it N/A.

Example:

`N/A — Requires administrator credentials that were not provided.`

---

# 9. REFERENCE CHECKLISTS

Load only the checklist files relevant to the current project.

| Checklist              | Reference file                                   | Category tag  |
| ---------------------- | ------------------------------------------------ | ------------- |
| Cybersecurity          | `references/cybersecurity-checklist.md`          | `CYBER`       |
| Laravel/MySQL Security | `references/laravel-mysql-security-checklist.md` | `LARAVEL-SEC` |
| Laravel/MySQL SEO      | `references/laravel-mysql-seo-checklist.md`      | `LARAVEL-SEO` |
| General QA             | `references/general-qa-checklist.md`             | `GENERAL-QA`  |
| Design                 | `references/design-checklist.md`                 | `DESIGN`      |

Do not invent checklist items.

When reporting an item, preserve the checklist item number and wording from
the applicable reference checklist.

---

# 10. CHECKLIST SELECTION

If the user explicitly specifies a checklist, use that checklist.

If the user does not specify a checklist:

1. Determine the project's technology stack.
2. Determine the site's functionality.
3. Select applicable checklist categories.
4. Skip framework-specific checklists when the framework does not apply.
5. Within each selected checklist, determine which individual items apply.

If the stack or functionality cannot be determined confidently, inspect the
project/site using read-only methods before deciding.

If important access is unavailable, state this clearly instead of assuming the
result.

---

# 11. SCOPE CONFIRMATION

At the beginning of the run identify:

* Domain / URL or local project path.
* Project ID, if supplied.
* Technology stack, where identifiable.
* Authentication availability.
* Applicable checklists.
* Important testing limitations.

Do not modify the target while determining scope.

---

# 12. RUN NUMBER

Before generating output files, inspect:

`/mnt/user-data/outputs/`

Look for existing files matching:

`Issue_Log_No_*.txt`

Determine the next integer run number.

Examples:

No previous issue logs:

`Issue_Log_No_1.txt`

If logs 1 and 2 exist:

`Issue_Log_No_3.txt`

Do not overwrite historical issue logs.

`Passed_Tests.txt` is regenerated for the current run.

---

# 13. TESTING WORKFLOW

## Step 1 — Confirm scope

Identify:

* Target.
* Project ID.
* Technology stack.
* Authentication/access.
* Applicable checklist categories.

## Step 2 — Determine applicability

Review available functionality and determine which individual checklist items
apply.

Do not automatically execute irrelevant checks.

## Step 3 — Load relevant reference checklists

Load only relevant checklist files.

## Step 4 — Test each applicable item

For every applicable checklist item:

1. Perform the appropriate read-only test.
2. Record the observed result.
3. Determine Pass, Fail, or N/A.
4. Record evidence for failures.
5. Assign severity and confidence to failures.
6. Do not modify the target.

## Step 5 — Verify failures

Where practical, re-check failed items to reduce false positives.

Do not perform destructive exploitation merely to prove a finding.

## Step 6 — Generate artifacts

Create:

* `Issue_Log_No_<x>.txt`
* `Passed_Tests.txt`

in:

`/mnt/user-data/outputs/`

## Step 7 — Summarize

Provide a concise summary containing:

* Total items tested.
* Pass count.
* Fail count.
* N/A count.
* Counts by checklist.
* Locations of the two generated files.

Do not restate every checklist item in chat.

---

# 14. PROJECT-SPECIFIC REQUIREMENTS

Some checklist items may depend on information that is not available through
the website or source code alone.

Examples:

* Approved content documents.
* Design guidelines.
* Project requirements.
* Trial/show feedback.
* Notification-email specifications.
* Backup policies.
* Internal infrastructure requirements.
* Administrator profile requirements.

These must not be marked Pass unless the required evidence is available.

If unavailable:

`N/A — Required project documentation/access was not available.`

Do not infer that the requirement is satisfied.

---

# 15. FRONT-END AND GENERAL QA

Where applicable inspect:

* Overall design and functionality.
* Approved content and page structure.
* Menus and child menus.
* Hyperlinks.
* Page titles.
* Hover effects.
* Font and color consistency.
* Spell checking and readability.
* Social media links.
* Navigation aids.
* Tab order.
* Error-message focus behavior.
* Testimonials where relevant.
* Content placement.
* Text hierarchy.
* Duplicate content/data.
* Image naming and alt text.
* Footer information.
* Breadcrumbs.
* Favicon.
* File-upload controls.
* Upload validation.
* Pagination.
* Maps.
* Broken links.
* External-link behavior.
* Required-field indicators.
* Form validation.
* Social sharing previews.
* Dummy/placeholder content.
* Media alignment.
* Page consistency.

Only test items that apply to the project.

---

# 16. CONTACT FORMS

Where contact forms exist, test:

* Invalid-input warnings.
* Successful submission acknowledgement.
* Email validation.
* Phone/mobile validation where applicable.
* Required fields.
* Notification behavior where verifiable.
* Notification formatting where the required reference format is available.

Do not claim that an email was delivered unless delivery can actually be
verified.

If delivery cannot be verified:

`N/A — Email delivery could not be independently verified with available
access.`

---

# 17. CAREERS

Where career/job functionality exists, test:

* Vacancy listing.
* Job application access.
* Application navigation.
* Back navigation.
* Pagination where applicable.
* Validation.
* Successful application acknowledgement.
* Administrative notification behavior.
* Vacancy ordering/priority.
* Disabled-vacancy behavior.

Do not test career items on projects that have no career functionality.

---

# 18. GALLERY

Where gallery functionality exists, test:

* Image listing.
* Pagination where applicable.
* Mobile responsiveness.
* Image dimensions/consistency.
* Disabled-image behavior.
* Administrative gallery management where access exists.

---

# 19. BACK-END / ADMINISTRATION

Where an administrative backend exists, test applicable functionality
including:

* Login.
* Search.
* Backend favicon.
* Visit-site functionality.
* Pagination.
* Sorting.
* User/log navigation.
* Profile editing.
* Password-change functionality.
* Logout.
* Dashboard functionality.
* File-upload controls.
* User groups.
* User permissions.
* User management.
* Career administration.
* Gallery administration.
* Testimonials.
* Enquiry/contact management.

Do not delete or alter real production data merely to prove CRUD operations.

Prefer:

* Existing test data.
* Read-only verification.
* Safe test accounts.
* Non-destructive workflows.

---

# 20. FUNCTIONALITY

Where applicable verify:

* Hyperlink destinations.
* Button destinations.
* Valid input handling.
* Invalid input rejection.
* Supporting icons/graphics.
* Maximum field lengths.
* Error handling.
* 404 handling.
* Database-backed functionality where safely verifiable.

Do not directly modify database records to prove CRUD functionality.

---

# 21. PERFORMANCE AND COMPATIBILITY

Where applicable assess:

* Page loading performance.
* Browser compatibility.
* Responsive rendering.
* Image rendering.
* Font rendering.
* Long-session behavior where safely assessable.
* Current performance tooling results.

Do not perform load/stress/denial-of-service testing.

For performance claims, record the tool and measurement used.

Do not claim that continuous usage or high concurrency has been tested unless
it actually has been tested within an appropriate non-destructive scope.

Legacy browser requirements should be interpreted according to the project's
actual supported browser requirements.

Do not fabricate testing of unavailable browsers or devices.

---

# 22. SECURITY AND PRIVACY

Where applicable inspect:

* Form anti-spam/security controls.
* File-upload restrictions.
* Dangerous file-extension handling.
* Directory listing.
* Sensitive file exposure.
* Authentication.
* Authorization.
* Session behavior.
* Security headers.
* TLS/SSL configuration.
* Dependency vulnerabilities.
* Other applicable cybersecurity controls.

Security testing must remain non-destructive.

Do not claim exploitability without sufficient evidence.

---

# 23. WEBSITE ADMINISTRATION

Where applicable verify:

* Authentication requirements.
* Forgot-password functionality.
* Administrative account behavior.
* Required modules.
* Appropriate access controls.

Never expose actual passwords, API keys, tokens, or other secrets in the
report.

If a secret is discovered, report the type and location without reproducing
the secret value.

---

# 24. MOBILE RESPONSIVENESS

Where applicable inspect relevant viewport sizes and devices.

Consider:

* Mobile rendering.
* Tablet rendering.
* Portrait orientation.
* Landscape orientation.
* Navigation.
* Forms.
* Buttons.
* Click-to-call functionality.
* Email links.
* Content overflow.
* Horizontal scrolling.
* Image behavior.
* Text readability.

Test only what can actually be verified with available tooling.

Do not claim testing on a physical device or operating system that was not
actually tested.

---

# 25. SEO

Where applicable inspect:

* Unique page titles.
* `sitemap.xml`.
* `robots.txt`.
* SEO-friendly URLs.
* Analytics where verification is possible.
* Canonical URLs.
* Redirects where applicable.
* Logo alt text.
* Image alt text.
* Social icons.
* Meta titles.
* Meta descriptions.
* Relevant title attributes.
* Geo information where relevant.
* Page-speed performance.
* Structured data.
* Website schema.
* Webpage schema.
* Organization schema.
* Postal address schema.
* Product/price/stock schema where applicable.
* Breadcrumb schema.
* H1/H2 structure.
* Consistency of titles, labels, icons, buttons, page elements, and editorial
  style.

Do not mark analytics as Pass merely because an analytics script exists.

Where possible verify that it is operational.

Do not mark schema as Pass merely because some structured data exists.
Verify the applicable schema type.

---

# 26. DESIGN AND ACCESSIBILITY

Where applicable inspect:

* Clear user position/state.
* Meaningful page titles.
* Clear next-step information.
* Notification/alert clarity.
* Consistent visual language.
* Understandable icons.
* Consistent screen layouts.
* Keyboard/tab navigation.
* Field-to-field navigation.
* Focus behavior.
* Mandatory-field indicators.
* Input formatting guidance.
* Intuitive forms.
* Avoidance of unnecessary horizontal scrolling.
* Readability.
* Accessibility considerations.
* Save/Preview functionality where applicable.
* Print guidance where applicable.
* Social sign-in where applicable.
* Privacy/policy information.
* Graph/chart presentation where applicable.
* Notification navigation.
* Keyboard-only navigation.
* Search placement.
* Video captions where applicable.
* Alternative descriptions for animations where applicable.
* Alternative formats where applicable.
* CSS/layout behavior.
* Consistent page layouts.
* Avoidance of text represented unnecessarily as images.
* Sitemap/table-of-contents navigation where applicable.

Do not mark optional functionality as a failure simply because it is absent.

---

# 27. INACCESSIBLE CHECKS

If a check requires unavailable access, do not guess.

Use:

`N/A — <specific reason>`

Examples:

`N/A — Requires SSH/server access not available to the agent.`

`N/A — Requires database access that was not provided.`

`N/A — Requires the approved project documentation, which was not available.`

`N/A — Requires access to the email inbox to verify delivery.`

`N/A — Physical mobile-device testing was not available.`

---

# 28. ISSUE LOG OUTPUT

Create:

`/mnt/user-data/outputs/Issue_Log_No_<x>.txt`

Format:

```text
SESAME TECHNOLOGIES — QA ISSUE LOG
Issue Log No: <x>
Domain / Target: <domain or URL>
Project ID: <project id or "N/A">
Date: <YYYY-MM-DD>
Checklists run: <comma-separated checklist names>
Tested by: AI QA Agent (read-only — no code/config/data was modified)

----------------------------------------
ISSUE #1
Checklist: <CYBER | LARAVEL-SEC | LARAVEL-SEO | GENERAL-QA | DESIGN>
Item #: <item number>
Item: <checklist item text>
Severity: <Critical | High | Medium | Low>
Confidence: <High | Medium | Low>
Observed: <what was actually found>
Evidence: <URL, HTTP status, header, path, screenshot description, etc.>
Recommendation: <general remediation recommendation — do not implement it>
----------------------------------------
ISSUE #2
...

----------------------------------------
SUMMARY
Total items tested: <n>
Passed: <n>
Failed (this log): <n>
N/A: <n>
```

If there are zero failures, still create the file.

Use:

```text
----------------------------------------
NO ISSUES FOUND
----------------------------------------

SUMMARY
Total items tested: <n>
Passed: <n>
Failed (this log): 0
N/A: <n>
```

---

# 29. PASSED TESTS OUTPUT

Create/regenerate:

`/mnt/user-data/outputs/Passed_Tests.txt`

This file represents the current run only.

Format:

```text
SESAME TECHNOLOGIES — QA PASSED TESTS
Domain / Target: <domain or URL>
Project ID: <project id or "N/A">
Date: <YYYY-MM-DD>
Checklists run: <comma-separated checklist names>
Corresponds to Issue Log No: <x>

Checklist: CYBER
[PASS] #1 — <exact checklist item>
[PASS] #2 — <exact checklist item>

Checklist: GENERAL-QA
[PASS] #8 — <exact checklist item>

Checklist: DESIGN
[PASS] #12 — <exact checklist item>

----------------------------------------
N/A ITEMS
----------------------------------------
[N/A] #<number> — <item> — <one-line reason>

----------------------------------------
SUMMARY
Total passed: <n> / <n tested>
```

N/A items must not be counted as Passed or Failed.

---

# 30. OUTPUT ACCURACY RULES

Before creating the final output files:

* Confirm every reported issue was actually observed.
* Confirm every Pass has supporting evidence.
* Confirm N/A reasons are accurate.
* Confirm checklist item numbers match the reference checklist.
* Confirm no issue was accidentally marked as Pass.
* Confirm no N/A item was counted as Pass or Fail.
* Confirm no credentials or secrets appear in the output.
* Confirm the target was not modified.
* Confirm the issue log number is correct.
* Confirm historical issue logs were not overwritten.
* Confirm `Passed_Tests.txt` represents only the current run.

---

# 31. FINAL CHAT SUMMARY

After generating the files, provide a concise summary:

QA run completed.

Target: <domain>
Project ID: <project id>
Issue Log: No. <x>

Results:

* <Checklist>: <Pass> passed, <Fail> failed, <N/A> N/A
* <Checklist>: <Pass> passed, <Fail> failed, <N/A> N/A

Total:

* Passed: <n>
* Failed: <n>
* N/A: <n>

Artifacts:

* Issue_Log_No_<x>.txt
* Passed_Tests.txt

Testing was read-only; no code, configuration, database, or infrastructure
was modified.

Do not restate every checklist item in chat.

---

# 32. CORE PRINCIPLE

The goal is **accurate QA reporting, not maximum issue count**.

A smaller number of well-supported findings is preferable to a large number of
false positives.

The agent must:

**Determine applicability → test what applies → verify what it can →
record evidence → report accurately → leave the target unchanged.**
