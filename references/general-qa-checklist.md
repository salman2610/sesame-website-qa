# General QA Checklist

**Domain Name:** ______  **Project ID:** ______

> Master checklist for front-end, back-end/admin, functionality, performance,
> security, mobile responsiveness, SEO, and design/accessibility QA. Not every
> item applies to every project — mark non-applicable items `N/A` with a
> reason instead of failing them.

## Front-End — General

1. Whether the "General standards & guidelines" document has been cross-checked against overall website design and functionality.
2. Whether a "Trial Show" was conducted and the changes noted after the trial have been included in the final website.
3. Whether menus, child menus, page contents, hyperlinks & page titles are developed as per the "Website Content" document approved by the client.
4. Whether mouse-over effects for hyperlinks are quickly noticeable by the visitor (color change, underlining, or any animated style).
5. Whether font & color tone are consistent throughout the website, and text in all specified fields uses the correct screen font.
6. Has the website content been spell-checked and content readability ensured?
7. Whether social media links are included on relevant pages and are connected properly.
8. Do all pages have a "Go to Top" button?
9. If the tab order on a screen moves in sequence from top-left to bottom-right.
10. When an error message occurs, does focus return to the field in error when the user cancels it?
11. Is there a testimonial section provided for relevant websites?
12. Is content placement consistent?
13. Is there a clear hierarchy of text and headlines?
14. Is there any duplicate data existing anywhere on the site?
15. Do image names match the images displayed (e.g., an image of a mickey mouse is named `mickeymouse.jpg`, not `image.jpg`)? Do all images have the `alt` tag defined properly?
16. Whether the name of the developing firm is given in the format "Site developed by **[Company Name]**", with a link to the company's website (at least on the home page).
17. Whether copyright, disclaimer, privacy policy, etc. are provided in the page footer area where applicable.
18. On sites with sub-menus, whether the current page position is shown as a breadcrumb.
19. Whether a favicon (shortcut icon) is assigned for the site and displayed in the address bar of every browser.
20. Whether file upload controls specify acceptable file formats, file size, and file dimensions — and whether the uploaded file name displays near the control once complete.
21. Whether file upload controls display warning messages when invalid input is submitted.
22. Whether a live map of the organization is added to the website, where valid address details exist.
23. Are there any broken links present on the site?
24. Do external links open in a separate window/tab?
25. Whether all mandatory fields are marked with a red asterisk and validated before form submission.
26. Whether field validation is shown via highlight options with customized warning labels.
27. Verify that when a page URL is shared on Facebook or other social platforms, an appropriate image and description show in the preview.

## Pages

28. Whether "Under Construction" is shown for pages with insufficient data — the space should not be left blank.
29. Whether a hotspot link for the logo is provided on all pages of the site (where applicable).
30. Does the live site have any dummy content present?
31. Whether media elements used across the page are aligned to the content structure.
32. Whether subpages have been developed distinctly from the home page, where applicable.

## Contact Forms

33. Whether a warning message is displayed for invalid input.
34. Whether an acknowledgement message is displayed after successful form submission.
35. Does admin receive a notification email once a user submits a contact form?
36. Whether email & mobile number validations are performed on all form submissions.
37. Does the notification email follow the pre-defined format in the "General standards & guidelines" document?

## Career

38. Whether the user can view the list of current vacancies.
39. Whether the user can apply for a job from the current vacancies page.
40. If the "Apply" button opens in a separate window/tab.
41. If a back button is provided to return to the job listing page.
42. Whether the user can go directly to the job application page.
43. If warning messages display for invalid input.
44. Whether an acknowledgement message displays after successful application submission.
45. Does admin receive a notification email after a user submits a job application?
46. Does the notification email follow the pre-defined format in the "General standards & guidelines" document?

## Gallery

47. If all images are mobile-responsive and of consistent dimensions.

## Back-End — General

48. Whether a login form is provided for admin.
49. Does the search function work properly?
50. Does the company logo appear in the top-left corner?
51. Whether a "Visit Site" option is provided to access the front-end site.
52. If a search option is provided on all pages with data listing.
53. Whether pagination is provided on all pages when there are more than 10 records to display.
54. Whether a favicon (shortcut icon) is assigned for the site backend and displayed in the address bar.
55. Whether ascending/descending sort is provided for relevant columns in lists.
56. If a dropdown list is provided to easily access user logs and users.
57. If admin can edit their user profile & company profile.
58. Whether admin can change their password (max length 20 characters).
59. If admin can successfully log out.
60. If a dashboard shows user info, the latest five enquiry details, FAQ, and company contact information (for relevant website backends).
61. Whether file upload controls specify acceptable file formats, file size, and file dimensions — and whether the uploaded file name displays near the control once complete.

## User Group

62. Check if admin can:
    - Add a new user group by entering a group name.
    - View the list of user groups.
    - Change user group status.
    - Edit a user group name.
    - Set user group permissions.
    - Delete a user group / groups.
63. Whether admin can disable a user group that has existing users (a warning message should display).
64. Whether a user group receives only the permissions assigned by admin.
65. Whether admin can delete a user group that has existing users (a warning message should display).
66. If admin can navigate between "Add/Edit" pages and the listing page.

## User

67. Check if admin can:
    - Add a new user with data such as user group, name, phone, email, login name, password & user icon.
    - Change user status.
    - Edit user details (group, name, phone, email, password, account icon).
    - Delete a user / users.
    - View a list of user logs (date/time of login/logout by different users).
    - Delete user log entries.
68. Whether a user gets only those permissions, over different modules, assigned to their user group.
69. If admin can navigate between "Add/Edit" pages and the listing page.

## Career — Administration

70. Check if admin can:
    - View the list of all job vacancies.
    - Add a new job vacancy (post name, experience, vacancy, place, description & priority).
    - Change the job vacancy status.
    - View the list of applicants for a job vacancy.
    - View individual applicant details.
    - Delete applicant(s) from the list.
    - Edit job vacancy details.
    - Delete job vacancy / vacancies from the list.
71. If the "Experience" field accepts alphanumeric and special characters.
72. If "Vacancy" & "Priority" fields accept only numbers.
73. Whether the maximum character limit for the "Description" field is 1000.
74. If admin can navigate between "Add/Edit" pages and the listing page.
75. If admin can navigate between the applicant listing page and individual candidate details.
76. If admin can navigate between the job listing page and applicant listing page.
77. Whether disabled job vacancies appear on the front end.
78. Whether job vacancies display on the front end according to priority.
79. Does admin receive a notification email once a front-end user submits a job application?
80. Does the notification email follow the pre-defined format in the "General standards & guidelines" document?

## Gallery — Administration

81. Check if admin can:
    - View the list of photos.
    - Add a new photo.
    - Change photo status.
    - Edit photo details (category, title, image).
    - Delete photo(s).
    - View the list of photo categories.
    - Add a new photo category (name, URL, description, image).
    - Change photo category status.
    - Edit photo category details.
    - Delete photo category / categories from the list.
82. Whether disabled photos appear on the front end.
83. If admin can navigate between the photo listing page and "Photo Add/Edit" pages.
84. If admin can navigate between the photo category listing page and "Photo category Add/Edit" pages.

## Testimonials

85. Check if admin can:
    - View the list of testimonials.
    - Add a new testimonial (name, designation, location, image, description).
    - Change testimonial status.
    - Edit testimonial details.
    - Delete a testimonial / testimonials.
86. If admin can navigate between the listing page and "Add/Edit" pages.

## Contact / Enquiry Details

87. Check if admin can:
    - View the list of all enquiries.
    - View enquiry details (name, email, phone, message title & message).
    - Delete a contact / enquiry.
88. Does admin receive a notification email once a front-end user submits a contact form?
89. Does the notification email follow the pre-defined format in the "General standards & guidelines" document?

## Functionality Checking

90. Whether hyperlinks are interconnected properly.
91. Buttons: whether each button takes the visitor to the required page.
92. Whether valid input is accepted and invalid input is rejected during form submission.
93. Whether related icons or graphics support the web page.
94. Whether maximum field lengths are enforced to prevent truncated characters.
95. Whether database queries — writing, retrieving, or editing — are performed correctly.
96. Is there a custom 404 page, or are 404 requests otherwise handled correctly?

## Performance & Compatibility

97. Whether the web page is compatible across major browsers (Chrome, Firefox, Edge, Safari, Opera, etc.) and all resolutions.
98. If the site displays within 8 seconds in the visitor's browser.
99. If the site sustains long periods of continuous use by users.
100. Whether the site or a given page can be used simultaneously by different users at the same time.
101. Whether page-load performance is acceptable over connections of different speeds.
102. Whether images display correctly in all standard browsers.
103. Whether fonts render correctly in all browsers.
104. If animated images appear properly across different browsers.
105. Does the website show above-average ratings when checked with Google PageSpeed Insights and GTmetrix?

## Security & Privacy

106. For image uploads, check that only the following file extensions are allowed: `.jpg`, `.gif`, `.swf`, `.png`; and for document uploads: `.doc`, `.xls`, `.pdf`.
     **NB:** `.exe`, `.txt`, `.ini`, `.html`, `.php`, `.bat`, `.cmd`, `.bsh`, `.sh` extensions should not be allowed.
107. Whether directory listing is disabled (e.g., `yourdomain.com/images`) — it should not show the list of files inside folders, but should return a warning or forbidden message.
108. Have the site files and database been backed up and stored in a safe place?
109. Whether the database password is secure.
110. Have weekly database backups been scheduled?

## Website Administration

111. Is it possible to log in to the control panel without a username and password?
112. Whether a "Forgot Password" link is provided on the login page — does admin receive an email with temporary password details?
113. Are credentials ready for admin users, with complete address and profile information?
114. Are the required modules activated and usable for the admin user?

## Mobile Responsiveness

115. Is the web page responsive and working correctly on iOS, Windows, and Android?
116. Does the website work well across standard screen resolutions (320×480, 360×640, 768×1024) and devices?
117. Does the website work correctly in responsive mode when subjected to orientation (landscape/portrait) changes?
118. Does the mobile view show "Click to Call" & "Send mail" buttons at the bottom of the homepage?

## Basic SEO Elements

119. Do all pages have valid, unique titles?
120. Have `sitemap.xml` and `robots.txt` been added to the domain root?
121. Whether all URLs are SEO-friendly and follow the general standard format.
122. Has Google Analytics tracking been installed and confirmed operational?
123. Set up canonicalization for all URLs.
124. Set up 301 redirects to the `www` URL (for revamped websites).
125. Add logo `alt` tag.
126. Add image `alt` tags.
127. Add social icons.
128. Add meta title.
129. Add meta description.
130. Include title tags on the left-side menu, product listing, top menu, and footer menu.
131. Place a geo tag in the header file.
132. Improve page-speed score — check with Google PageSpeed Insights.
133. Manage schema markup:
     - Website schema
     - Webpage schema
     - Organization schema
     - Postal address schema
     - Product, price & stock schema
     - Breadcrumb schema
134. Whether proper H1 and H2 headings are set for web pages.

## Design & Accessibility Guidelines

135. Be consistent in: use of icons, titles, labels, placement of page elements, buttons, and editorial style.
136. Show where the user is in the process:
     - Give screens meaningful titles so users remember where they are and what they're doing.
     - Show what will happen next (next step, who receives notification).
     - Use color cues.
     - Use icons with standard, understandable meanings.
     - Use the same format on each screen so users can predict where to find directions.
137. Field/form navigation:
     - Let the user tab from field to field.
     - Automatically place the cursor in the first field on a screen.
     - Provide confirmation and warning pop-ups/screens.
     - Design forms to be self-correcting so users can't proceed on error or skip an essential field.
     - Specify how data should be formatted (e.g., mm/dd/yyyy).
     - Indicate mandatory fields.
     - Design look-ups to populate fields with the desired data.
     - Build an intuitive format/process that reduces the need for directions or help text.
     - Stack fields vertically and restrict screen width to avoid horizontal scrolling.
     - Use a dark, sans-serif font against a light background.
138. Session & account UX:
     - Use Single Sign-On where the application should recognize the user.
     - Design for accessibility, including an option to change font size.
     - Include Save and Preview options on each screen where possible.
     - Indicate when users should print a screen for their records.
     - Give clear printing instructions so users don't have to print a screenshot.
     - Support social sign-in.
     - Show privacy & policy information.
     - Follow consistent graph/chart standards.
     - Use clear alert and notification messages, with sensible notification navigation.
139. Make sure users can navigate without a mouse, using tab keys and directional arrows; place any search window close to the top of the page.
140. Sound, animation, and video:
     - Provide text/transcripts for sound.
     - Use closed captioning on videos.
     - Provide alternate descriptions for animation files.
     - Give users a choice of versions (e.g., accessible with or without Flash, Shockwave, JavaScript, etc.).
141. Structure: use style sheets to control layout and presentation, but verify the page remains readable with style sheets turned off.
142. Use screen layouts that are consistent and uncomplicated.
143. Avoid using images to represent text, with the possible exception of navigation links.
144. To communicate the site's structure, provide a sitemap or table of contents with links to specific sections.

---

| Internal Checking done by | Verified By |
|---|---|
| Name: | Name: |
| Date: | Date: |

### Remarks after checking

If the above checks pass and the site is ready to host, confirm:

- The dummy text and pictures uploaded are relevant to the domain.
- Standard test cases were used for design-level checking.
- The developed site resembles the CRS or project description.
