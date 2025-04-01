# QA Analyst Take Home Assessment
This repository contains my submission for the QA Analyst Take-Home Assessment.

## Overview
The goal of this project is to manually test the Linq profile feature from a visitor’s perspective — specifically, viewing a profile and attempting to save contact information. This includes analyzing behavior using browser dev tools and Postman.

---

## Files Included
- `test-cases.md`: Manual test cases executed to validate the contact exchange flow.
- `bugs.md`: Reported bugs and unexpected behaviors found during testing.
- `postman-notes.md`: API request/response details and insights using Chrome DevTools and Postman.
- `bonus.md`: Optional section with process improvement suggestions and testing approach notes.
- `screenshots/`: Captured screenshots to support findings.

---

## Highlights
- Tested visitor flow: viewing and exchanging contact info on a public Linq profile.
- Identified potential data exposure via unauthenticated API requests.
- Simulated key backend requests using Postman (`GET /download_contact`, `GET /user_contacts`, and `POST /user_contacts`).
- Suggested enhancements for security and user awareness.

---

## Tools Used
- Google Chrome DevTools
- Postman
- Git + GitHub

---

## Notes
To complete the assessment, I first created a user profile on Linq.
Then, I conducted testing from the perspective of a visitor (not logged in) by:
- Accessing the user's public profile link
- Exchanging and downloading contact information
- Inspecting API calls primarily via Google Chrome DevTools, and later verified some endpoints in Postman

