# PARTHBLOG

### Functional Requirements Specification

**Version 1.1**

---

## Project Information

| **Project Name** | ParthBlog |
|---|---|
| **Document Type** | Functional Requirements |
| **Version** | 1.1 |
| **Created By** | Piyush Dhyani |
| **Created On** | 01 October 2026 |
| **Last Updated** | 02 October 2026 |

---

## Document Status

**Status:** Active

**Scope:** User Registration, Authentication & Blog Management

> ParthBlog is a fictional blogging platform created as a QA & Business Analysis portfolio project, covering functional requirements and user-facing workflows.

---

## Contents

1. [Version History](#version-history)
2. [Scope](#scope)
3. [Requirements](#requirements)
   - [REQ-01 — User Registration](#req-01--user-registration)
   - [REQ-02 — User Login](#req-02--user-login)
   - [REQ-03 — Forgot Password](#req-03--forgot-password)
   - [REQ-04 — Create Blog](#req-04--create-blog)
   - [REQ-05 — Edit Blog](#req-05--edit-blog)
   - [REQ-06 — Delete Blog](#req-06--delete-blog)

---

# Version History

| Version Number | Date Updated | Changelog |
|---|---|---|
| 1.0 | 01-10-26 | Initial creation of the requirements |
| 1.1 | 02-10-26 | Added REQ-04 — Create Blog, REQ-05 — Edit Blog, and REQ-06 — Delete Blog. Scope update |

---

# Scope

This project is being made to create a website where the user can create, publish and update the blogs of their choosing. The user can register in the website and create and update the blog of their choosing.

---

# Requirements

## REQ-01 — User Registration

**Flow:** Fill details → Click Signup → Validate details → Send OTP → Show OTP verification screen → Enter OTP → Create/verify account

- The user will be able to register to the website so that they can publish the blogs of their own.
- The user needs to enter 4 things - email, username and password and confirm password.
- The email needs to be in format of `userid@domain.com/net etc`. If the requirement isn't met, the user won't be able to proceed further.
- The username needs to contain 1 lowercase, 1 uppercase, 1 special character and 1 numerical value at minimum. Max character limit is 8. Also, the username needs to be a unique value, otherwise it will be rejected.
- Same requirements for password and confirm password as username ones. The password and confirm password need to contain exactly the same values.
- If user is able to satisfy the requirement for all 4 fields, it will result in account verification screen being displayed next. After clicking the Signup button, the user will need to enter a one-time password sent to their email to verify the account. Once done, the user account will be created and verified.

---

## REQ-02 — User Login

**Flow:** Open Login → Enter username → Enter password → Click Login → Validate credentials → Authenticate user → Grant access to account

- The user can use a username and password to log into the website.
- The username shall contain minimum 1 lowercase, 1 uppercase, 1 special character and 1 numerical value. The character limit is 8.
- Same requirements for password as username.
- The user need not to enter their email for the login process. It's only useful for Signup, forgot password functionality and keeping up to date with their blog posting on their personal registered email.
- The user entering the username and password as per the requirement and click on Login will be able to login. If these requirements aren’t met or if the user isn’t registered, login will be denied.

---

## REQ-03 — Forgot Password

**Flow:** Open Login → Click Forgot Password → Enter registered email → Validate email → Send password reset link → Open reset link → Enter new password → Confirm password → Validate password → Reset password → Display success message → Navigate to Login

- The user will be able to reset their password in case they forgot it. They can navigate to this screen from the login screen.
- The user needs to enter their registered email when asked on the Forgot Password screen. If the user enters a non-registered email or if they don’t follow the defined email format, the system will throw an error.
- The user will get a link in their registered email inbox to reset the password. Clicking it will take them to a new screen to reset password.
- The user needs to enter the password and confirm password on this screen. The format for this will be the same as Signup/Login ones. If both password field values match, the user will be able to reset their password.
- If the user enters any one of their old passwords, the system shall throw a unique error: **"you're using an old password. Please enter a new one"**. If the user doesn't follow the formatting or if the password and confirm password fields don’t match, they will get the usual error message.
- On successfully resetting their password, the user shall get a success message and navigate to the login screen to try logging in again with the new password they created.

---

## REQ-04 — Create Blog

**Flow:** Open Home Page → Click Create Blog in Header → Enter Title → Enter Blog Description → Upload 1–5 Images → Click Publish Blog → Validate Details → Publish Blog → Display Published Blog

- The registered user can navigate to Publish Blog page from the home page header menu.
- On this new page, to publish a blog, the user needs to click on the Publish Blog button.
- This will bring them to the Create Blog section. Here, user can add 3 things - Title, Blog Description and Images. All these 3 items are mandatory to publish the blog; else the user will get an error and the blog will not be published.
- Title needs to be 100-characters limit maximum. This will show up as the topmost thing when the blog is posted.
- Description needs to be 5000-characters limit maximum. User can add any word content they want in this space. The description field will support a Rich Text Editor allowing basic formatting (bold, italics, bullet points etc). This will show up as the body of the blog.
- For the blog images, user can add up to 5 images max, with minimum being 1. The image(s) must be only of JPG or PNG format with 5 MB size maximum. When the blog is published, the user can see the images on the left-hand side on the individual blog page with a left or right button to cycle through the images. The first most image uploaded for the blog will become its thumbnail.
- Once the user is done writing the blog, they can click the Publish Blog button to publish the blog.

---

## REQ-05 — Edit Blog

**Flow:** Open Publish Blog page → Locate specific published blog → Click Pencil Icon → Open Edit Blog Section → Modify content → Click Update Content → Validate details → Apply changes immediately

- In the Publish Blog page itself, the registered user has the option to edit their published blog.
- The registered user shall only be able to edit their own published blog. Blogs posted by other users are not eligible to be edited by the current user.
- Once clicking the Pencil icon on the right-hand side of the published blog, the user will see the Edit Blog section.
- The same constraints and requirements defined for Create Blog shall apply to the Edit Blog section.
- User can edit everything about the blog they want, however any of the blog content fields cannot be empty.
- Once the user is done editing their blog content, they can click on the Update Content button and this will apply the changes to the specific blog right away.

---

## REQ-06 — Delete Blog

**Flow:** Open Publish Blog page → Click Trashcan Icon next to a specific blog → Display confirmation pop-up → Click Yes → Permanently delete blog → Remove blog from Publish Blog page view

- This functionality will allow the registered user to delete the blog they have created.
- Alongside the Pencil icon from the Edit Blog section, user can see the Trashcan icon. This signifies the Delete Blog functionality.
- Clicking it will show a pop-up saying **"Are you sure you want to delete this blog? Once deleted, this blog cannot be recovered"** with a Yes/No button prompt. Clicking Yes will permanently delete the blog. Clicking No will close the pop-up and leave the blog unchanged.
- The deleted blog will no longer be displayed on the Publish Blog page.
- The user can delete their own blog and no one else's.
