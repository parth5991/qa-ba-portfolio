# ParthBlog — Functional Requirements

## Document Information

| Field | Details |
|---|---|
| **Website Name** | ParthBlog |
| **Version** | 1.0 |
| **Created By** | Piyush Dhyani |
| **Created On** | 01-10-2026 |
| **Updated On** | 01-10-2026 |

---

## Contents

1. [Version Record](#version-record)
2. [Scope](#scope)
3. [Requirements](#requirements)
   - [REQ-01 — User Registration](#req-01--user-registration)
   - [REQ-02 — User Login](#req-02--user-login)
   - [REQ-03 — Forgot Password](#req-03--forgot-password)

---

## Version Record

| Version Number | Date Updated | Changelog |
|---|---|---|
| 1.0 | 01-10-2026 | Initial creation of the requirements |

---

## Scope

This project is being made to create a website where the user can create, publish, and update the blogs of their choosing.

---

# Requirements

## REQ-01 — User Registration

**Flow:** Fill details → Click Signup → Validate details → Send OTP → Show OTP verification screen → Enter OTP → Create/verify account

- The user will be able to register to the website so that they can publish the blogs of their own.
- The user needs to enter 4 things: email, username, password, and confirm password.
- The email needs to be in the format of `userid@domain.com/net`, etc. If the requirement isn't met, the user won't be able to proceed further.
- The username needs to contain 1 lowercase, 1 uppercase, 1 special character, and 1 numerical value at minimum. Maximum character limit is 8. The username also needs to be a unique value; otherwise, it will be rejected.
- Same requirements for password and confirm password as username ones. The password and confirm password need to contain exactly the same values.
- If the user is able to satisfy the requirement for all 4 fields, it will result in the account verification screen being displayed next. After clicking the Signup button, the user will need to enter a one-time password sent to their email to verify the account. Once done, the user account will be created and verified.

---

## REQ-02 — User Login

**Flow:** Open Login → Enter username → Enter password → Click Login → Validate credentials → Authenticate user → Grant access to account

- The user can use a username and password to log into the website.
- The username shall contain minimum 1 lowercase, 1 uppercase, 1 special character, and 1 numerical value. The character limit is 8.
- Same requirements for password as username.
- The user need not to enter their email for the login process. It's only useful for Signup, forgot password functionality, and keeping up to date with their blog posting on their personal registered email.
- The user entering the username and password as per the requirement and clicking on Login will be able to login. If these requirements aren't met or if the user isn't registered, login will be denied.

---

## REQ-03 — Forgot Password

**Flow:** Open Login → Click Forgot Password → Enter registered email → Validate email → Send password reset link → Open reset link → Enter new password → Confirm password → Validate password → Reset password → Display success message → Navigate to Login

- The user will be able to reset their password in case they forgot it. They can navigate to this screen from the login screen.
- The user needs to enter their registered email when asked on the Forgot Password screen. If the user enters a non-registered email or if they don't follow the defined email format, the system will throw an error.
- The user will get a link in their registered email inbox to reset the password. Clicking it will take them to a new screen to reset password.
- The user needs to enter the password and confirm password on this screen. The format for this will be the same as Signup/Login ones. If both password field values match, the user will be able to reset their password.
- If the user enters any one of their old passwords, the system shall throw a unique error: **"You're using an old password. Please enter a new one."** If the user doesn't follow the formatting or if the password and confirm password fields don't match, they will get the usual error message.
- On successfully resetting their password, the user shall get a success message and navigate to the login screen to try logging in again with the new password they created.
