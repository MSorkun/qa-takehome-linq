# Manual Test Cases – View the profile and attempt to save contact info as a visitor. - Linq

---

### Test Case 1
- **Test Case ID:** TC001
- **Description:** Visitor opens a profile link in incognito mode
- **Steps:**
  1. Copy a user profile link (e.g., https://linqapp.com/mert_sorkun7)
  2. Open it in an incognito/private browser
- **Expected Result:**
  - Profile loads correctly
  - "Exchange Contact" button is visible

---

### Test Case 2
- **Test Case ID:** TC002
- **Description:** Visitor clicks "Exchange Contact" and dismisses the pop-up without entering any data
- **Steps:**
  1. Click "Exchange Contact"
  2. Press the ESC key or click outside the pop-up window
- **Expected Result:**
  - The pop-up closes
  - No confirmation message appears

---

### Test Case 3
- **Test Case ID:** TC003
- **Description:** Visitor clicks "Download Contact" and cancels the save prompt
- **Steps:**
  1. Click "Exchange Contact"
  2. Click "Download Contact"
  3. Press ESC or cancel in the OS file dialog
- **Expected Result:**
  - No confirmation message appears
  - The download process is canceled, and the file is not saved

---

### Test Case 4
- **Test Case ID:** TC004
- **Description:** Visitor fills in name and email and clicks "Continue"
- **Steps:**
  1. Click "Exchange Contact"
  2. Fill in the name and email fields
  3. Click "Continue"
- **Expected Result:**
  - Contact is successfully saved
  - A confirmation message is shown
  - Visitor receives an email confirmation

---

### Test Case 5
- **Test Case ID:** TC005
- **Description:** Visitor clicks "Download Contact" and successfully downloads the contact card
- **Steps:**
  1. Click "Exchange Contact"
  2. Click "Download Contact"
  3. Save the contact card to the desktop
- **Expected Result:**
  - The contact card file (.vcf) is saved to the desktop
  - The contact card can be opened and imported to the contacts list successfully

---

### Test Case 6
- **Test Case ID:** TC006
- **Description:** Visitor opens the profile page on both desktop and mobile
- **Steps:**
  1. Visit the same profile on both desktop and mobile devices
- **Expected Result:**
  - Layout is responsive
  - Call-to-action buttons are visible and functional on both desktop and mobile

---
