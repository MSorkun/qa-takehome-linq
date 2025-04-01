# Notes and Findings from Postman

## Overview  
I used Postman to inspect key API endpoints related to Linq’s public profile contact exchange flow. This included testing both `GET` and `POST` methods for downloading contact information and submitting contact information.

---

## 1. Download Contact Info (Public API)

- **Endpoint:**  
  `GET https://api.linqapp.com/api/v1/cards/mert_sorkun7/download_contact`

- **Authentication Required:** No  
- **Status:** `200 OK`  
- **Response:**  
  Returns a `.vcf` file (VCARD format) with full contact info:
  text format
  BEGIN:VCARD
  VERSION:3.0
  N:Sorkun;Mert
  FN:Mert Sorkun
  TEL;type=CELL,VOICE:+13108105426
  EMAIL:sorkunmert2@gmail.com
  item1.URL: https://linqapp.com/xoiz0bau_c8k?source=vcard
  item1.X-ABLabel: Linq
  END:VCARD

### This endpoint works without login or authentication and exposes full personal data, including phone and email.
### This may expose user data publicly to anyone with the profile link.

---
 
## 2. Exchange Contact Info (Submit Data)

- **Endpoint:**  
  `POST https://api.linqapp.com/api/v2/user_contacts`

- **Authentication Required:** No  
- **Status:** `200 OK`  
- **Request Payload:**
  json format
  {
    "contact_id": 2263723,
    "user_id": 563098,
    "form_fields_attributes": [],
    "note": "Hi!",
    "created_from_card_id": 634775,
    "is_accept_marketing": false
  }
  
- **Response Summary:**
  json format
  {
    "data": {
      "user_contact": {
        "id": 3205134,
        "contact_id": 2263723,
        "note": "Hi!",
        "created_at": "2025-04-01T11:08:26.854-05:00",
        "contact": {
          "first_name": "Mert",
          "phone_number": "+13108105426",
          "email": "sorkun.mert@outlook.com"
        }
      }
    }
  }
 

### The API accepted the POST without any authentication and returned detailed contact data in the response.
### This endpoint allows modification of user data without verification.

---

## 3. Auth Enforcement on GET `/user_contacts`

- **Endpoint:**  
  `GET https://api.linqapp.com/api/v2/user_contacts`

- **Authentication Required:** Yes  
- **Status:** `401 Unauthorized`  
- **Response:**
  json format
  {
    "error": {
      "type": "unauthorized",
      "messages": ["You can't see that"]
    },
    "status": "unauthorized"
  }
  

### This is expected and confirms that access to user-specific data is appropriately restricted.

---

### Screenshots  
Supporting screenshots of each API call and payloads are saved in the `/screenshots` folder for reference.

---

