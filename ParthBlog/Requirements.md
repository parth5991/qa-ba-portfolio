# PARTHBLOG

### Functional Requirements Specification

**Version 1.2**

---

## Project Information

| **Project Name** | ParthBlog |
|---|---|
| **Document Type** | Functional Requirements |
| **Version** | 1.2 |
| **Created By** | Piyush Dhyani |
| **Created On** | 01 October 2026 |
| **Last Updated** | 05 October 2026 |

---

## Document Status

**Status:** Active

**Scope:** User Registration, Authentication & Blog Management

> ParthBlog is a fictional blogging platform created as a QA & Business Analysis portfolio project, covering functional requirements and user-facing workflows.

---

# Contents

1. [Version History](#version-history)
2. [Scope](#scope)
3. [Requirements](#requirements)
   - [REQ-01 — User Registration](#req-01--user-registration)
   - [REQ-02 — User Login](#req-02--user-login)
   - [REQ-03 — Forgot Password](#req-03--forgot-password)
   - [REQ-04 — Home Page](#req-04--home-page)
   - [REQ-05 — Blogs](#req-05--blogs)
   - [REQ-06 — Create Blog](#req-06--create-blog)
   - [REQ-07 — Edit Blog](#req-07--edit-blog)
   - [REQ-08 — Delete Blog](#req-08--delete-blog)
   - [REQ-09 — Customize Profile](#req-09--customize-profile)
   - [REQ-10 — Contact Us](#req-10--contact-us)
   - [REQ-11 — FAQs](#req-11--faqs)

---

# Version History

| Version Number | Date Updated | Changelog |
|---|---|---|
| 1.0 | 01-10-26 | Initial creation of the requirements |
| 1.1 | 02-10-26 | Added REQ-04 — Create Blog, REQ-05 — Edit Blog, and REQ-06 — Delete Blog. Scope update |
| 1.2 | 05-10-26 | Added Home Page, Blogs, Customize Profile, Contact Us, and FAQs requirements. Expanded blog viewing, interaction, user profile, and website functionality. Updated project scope. |

---

# Scope

ParthBlog is a fictional blogging platform created as a QA & Business Analysis portfolio project. The scope encompasses the end-to-end functional requirements and user workflows required to build, manage, and test the platform.

The core modules of this project include:

- User Registration & Authentication (Login, Forgot Password)
- User Profiles & Account Management
- Global Feed & Home Page Dynamics
- Blog Content Management (Create, Edit, Delete)
- User Interactions (Commenting, Likes/Dislikes)
- General Website Functionality (Contact Us, FAQs)

---

# Requirements

## REQ-01 — User Registration

**Flow:**  
Fill details → Click Signup → Validate details → Send OTP → Show OTP verification screen → Enter OTP → Create/verify account

- The user will be able to register to the website so that they can publish the blogs of their own.
- The user needs to enter 4 things - email, username, password and confirm password.
- The email needs to be in format of `userid@domain.com/net etc`. If the requirement isn't met, the user won't be able to proceed further.
- The username needs to contain 1 lowercase, 1 uppercase, 1 special character and 1 numerical value at minimum. Max character limit is 8. Also, the username needs to be a unique value, otherwise it will be rejected.
- Same requirements for password and confirm password as username ones. The password and confirm password need to contain exactly the same values.
- If user is able to satisfy the requirement for all 4 fields, it will result in account verification screen being displayed next. After clicking the Signup button, the user will need to enter a one-time password sent to their email to verify the account. Once done, the user account will be created and verified.

---

## REQ-02 — User Login

**Flow:**  
Open Login → Enter username → Enter password → Click Login → Validate credentials → Authenticate user → Grant access to account

- The user can use a username and password to log into the website.
- The username shall contain minimum 1 lowercase, 1 uppercase, 1 special character and 1 numerical value. The character limit is 8.
- Same requirements for password as username.
- The user need not to enter their email for the login process. It's only useful for Signup, forgot password functionality and keeping up to date with their blog posting on their personal registered email.
- The user entering the username and password as per the requirement and click on Login will be able to login. If these requirements aren't met or if the user isn't registered, login will be denied.

---

## REQ-03 — Forgot Password

**Flow:**  
Open Login → Click Forgot Password → Enter registered email → Validate email → Send password reset link → Open reset link → Enter new password → Confirm password → Validate password → Reset password → Display success message → Navigate to Login

- The user will be able to reset their password in case they forgot it. They can navigate to this screen from the login screen.
- The user needs to enter their registered email when asked on the forgot password screen. If the user enters a non-registered email or if they don't follow the defined email format, the system will throw an error.
- The user will get a link in their registered email inbox to reset the password. Clicking it will take them to a new screen to reset password.
- The user needs to enter the password and confirm password on this screen. The format for this will be the same as Signup/Login ones. If both password field values match, the user will be able to reset their password.
- If the user enters any one of their old passwords, the system shall throw a unique error: `"you're using an old password. Please enter a new one"`. If the user doesn't follow the formatting or if the password and confirm password fields don't match, they will get the usual error message.
- On successfully resetting their password, the user shall get a success message and navigate to the login screen to try logging in again with the new password they created.

---

## REQ-04 — Home Page

**Flow:**  
Navigate to URL → Evaluate login status → Display appropriate Header (Login/Signup vs. Profile/Publish) → Display All-Time Top 5 Featured Blogs → Display Mission Statement → Display Testimonials → Display Footer

- The user will see the home page as the front page of the website.
- On the top, user can see the branding of the blog as well as info to login/Signup to the blog website (if not registered) or customize profile section (if registered and logged-in).
- The header navigation includes - Home, Blogs, Publish Blog (for logged in users only), Contact Us and FAQ page.
- Below that, a section of most featured blogs will contain the blogs that have the top 5 most likes on the blog post of all time.
- Below this, user can see a mission statement where user can see what the website is about.
- Below this, user can see testimonials and/or ratings left by other users based of their personal experience.
- On the footer, user can see social media links of the blog company, a section to subscribe to the blog website (by entering your email, like a newsletter for non-registered users who do not want to create their own blogs) and branding and policy details.

---

## REQ-05 — Blogs

### Flow — Main Feed

**Flow:**  
Navigate to Blogs Page → Fetch up to 50 blogs → Display Blog Snippets → Apply Sort/Filter (optional) → Click Next Page for pagination

### Flow — Individual Blog

**Flow:**  
Click Blog Snippet → Open Individual Blog Page → Read Content → Click Like/Dislike (if logged in) → Type Comment (if logged in) → Submit → Display Comment → Change/Delete Interaction (if authorized)

### Flow — Public Profile

**Flow:**  
Click Publisher Profile → Open Publisher Page → View User Info (Picture, Username, Bio, Join Date) → View User's Blog Feed → Apply Sort/Filter/Pagination

- The user can navigate to the Blogs page from the home page. They will be able to see the blog posts made by the registered users on the website.
- Blogs displayed on the Blogs page can only be viewed. Users cannot update or delete blogs from this page.
- Each blog snippet will include the image of the blog, the title and a partial description (taken from the full description from the beginning up until 100 characters and then `...`). Clicking on the blog capsule will take user to that individual blog page.
- On this individual blog page, the logged-in user can leave a like or dislike on the blog and leave a comment as well (all of it being optional). As the comment being posted, the user will see their username, profile image and comment as it is posted. Comment character limit is 300 characters maximum. A user who has left a comment can delete their comment, and a user who has liked or disliked a blog can remove their selection or change their selection from like to dislike and vice versa. Non-logged-in user can only read the blog.
- Back on the main blog page, the page itself will show 50 blogs at most with user being able to navigate through rest of the navigation via pagination.
- Any logged in or non-logged-in user can click on the profile of the blog publisher which will show the information of the blog publisher – username, profile picture, description and account created on. Below this, the user can see the blogs published by this user only looking exactly the same as the Blogs page itself with sort, pagination and filter present.
- The user can sort and filter the blogs.
- Sorting for the blogs will be by date published descending by default and can be configured by Date Published, Blog Title, Like Count, Dislike Count, Category Name. Supports both ascending and descending sorting.
- Filtering can be done by blog category and date published range by date, month or year.

---

## REQ-06 — Create Blog

**Flow:**  
Open Home Page → Click Publish Blog in header → Click Publish button → Open Create Blog section → Enter Title → Select Category → Enter Blog Description → Upload 1–5 Images → Click Publish Blog → Validate details → Publish Blog

- The registered user can navigate to Publish Blog page from the home page header menu.
- On this new page, to publish a blog, the user needs to click on the Publish button.
- This will bring them to the Create Blog section. Here, user can add 4 things - Title, Blog Description, Category and Images. All these 4 items are mandatory to publish the blog; else the user will get an error and the blog will not be published.
- Title needs to be 100-characters limit maximum. This will show up as the topmost thing when the blog is posted.
- Category can be any one of these 5 predefined categories – Technology, Lifestyle, Gaming, Travel Experience and Entertainment.
- Description needs to be 5,000-characters limit maximum. User can add any word content they want in this space. The description field will support a Rich Text Editor allowing basic formatting (bold, italics, bullet points etc). This will show up as the body of the blog.
- For the blog images, user can add up to 5 images max, with minimum being 1. The image(s) must be only of JPG or PNG format with 5 MB size maximum. When the blog is published, the user can see the images on the left-hand side on the individual blog page with a left or right button to cycle through the images. The first most image uploaded for the blog will become its thumbnail.
- Once the user is done writing the blog, they can click the Publish Blog button to publish the blog.

---

## REQ-07 — Edit Blog

**Flow:**  
Open Publish Blog page → Locate specific published blog → Click Pencil Icon → Open Edit Blog Section → Modify content → Click Update Content → Validate details → Apply changes immediately

- In the Publish Blog page itself, the registered user has the option to edit their published blog.
- The registered user shall only be able to edit their own published blog. Blogs posted by other users are not eligible to be edited by the current user.
- Once clicking the Pencil icon on the right-hand side of the published blog, the user will see the edit blog section.
- The same constraints and requirements defined for Create Blog shall apply to the Edit Blog section.
- User can edit everything about the blog they want, however any of the blog content fields cannot be empty.
- Once the user is done editing their blog content, they can click on the Update Content button and this will apply the changes to the specific blog right away.

---

## REQ-08 — Delete Blog

**Flow:**  
Open Publish Blog page → Click Trashcan Icon next to a specific blog → Display confirmation pop-up → Click Yes → Permanently delete blog → Remove blog from Publish Blog page view

- This functionality will allow the registered user to delete the blog they have created.
- Alongside the Pencil icon from the Edit Blog section, user can see the Trashcan icon. This signifies the delete blog functionality.
- Clicking it will show a pop-up saying `"Are you sure you want to delete this blog? Once deleted, this blog cannot be recovered"` with a Yes/No button prompt. Clicking Yes will permanently delete the blog. Clicking No will close the pop-up and leave the blog unchanged.
- Deleted blog will no longer show in the Publish Blog page.
- The user can delete their own blog and no one else's.

---

## REQ-09 — Customize Profile

### Flow — Edit

**Flow:**  
Click Profile Icon (top right) → Click Customize Profile → View Profile → Click Edit Profile → Modify fields → Enter Current Password (if changing email/password) → Click Update Profile → Validate → Apply changes

### Flow — Delete

**Flow:**  
Click Delete Account → Click Yes on confirmation prompt → Open verification email → Click deletion link → Delete user data & anonymize blogs

- The logged in user can customize their profile by navigating to it from the top right of their website. Clicking on their profile icon will open a pop-up where they can select Customize Profile.
- On this Customize Profile page, the user can see the following items - profile picture, account created date, username, email, bio.
- They can also see 2 buttons also - Edit Profile and Delete Account.
- Clicking Edit Profile will open a form to edit the profile.
- On this form, user can add/update an image for their profile (JPG, PNG only. 5MB maximum size).
- User can update their username. The user can update their username only once every 30 days from the date of the previous update. Same requirements for this as create account.
- User can update their email. The user can update their email only once every 30 days from the date of the previous update. Same requirements for this as create account.
- User can update their password. Enter new password and confirm new password. Same requirement as create account. The new password cannot be the same as the old one.
- User can add a description for their profile. 1000-character limit maximum.
- Any new updates to the profile will be saved once the user clicks Update Profile on this form. Any error in formatting will not allow user to update their information. Any information not updated in any field will not update the information. User cannot delete their predefined email, username and password.
- Back on the Customize Profile page, clicking the Delete Account button will show a confirmation pop-up `"Are you sure you want to delete your profile? If clicked Yes, you will receive a delete account link in your email which you can click to fully delete your details"`.
- Clicking the delete account link in the email will delete the account data, however the blog data itself will not be deleted from the website. In the place of deleted user's information in front of their published blog, it will show a generic image and `"Deleted User"` as username. This is non clickable.
- Clicking No on the Delete Account prompt will result in no change.

---

## REQ-10 — Contact Us

**Flow:**  
Navigate to Contact Us Page → View Form → Enter Email (auto-populated if logged in) → Enter Subject → Enter Message → Click Send → Validate Fields → Trigger Email to Admin → Display Confirmation Alert

- On the Contact Us page, the user can contact the website admin for any changes or issues they are facing.
- The user can add their email, subject and their message in the fields and click on send to send their message.
- Email address formatting is same as create account one. This field cannot be empty at the time of clicking Send. For logged-in user, the email field will be typed out pre-emptively.
- Subject field can contain 50 characters maximum. This field cannot be empty at the time of clicking Send.
- Message field can contain 1000 characters maximum. This field cannot be empty at the time of clicking Send.
- Clicking send and sending details will send an email to the admin of the website and user will see a confirmation alert on this page itself. Further correspondence can be possible on the user's email between user and admin.
- Any user can send the message through this page. Registered or not.

---

## REQ-11 — FAQs

**Flow:**  
Navigate to FAQ Page → View Categorized Questions → Click Question to Expand → Read Answer → Click Question to Collapse (optional)

- On the FAQ page, the user can see various question entries of questions asked on this page.
- The entries are categorized as per their content. User can collapse to hide the content and expand the question section to see the answer given in full. Default state is collapsed for a question.
- This question section will contain 2 things - question asked and answer given.
- This page is read only as the questions and answers are pre-populated.
