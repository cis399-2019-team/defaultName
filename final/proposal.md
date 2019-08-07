# Final Project Proposal: Creating User Email Accounts


### General Description

- Implement, manage, and create mail accounts for each individual user using chron and puppet jobs


### Goals

- Implement email services with IMAP and SMTP servers
- Inital test by creating dummy users and test if we can log into their emails
- Ensure that each person can log into their own email accounts
- Successfully create accounts for each user and this will be confirmed through a confirmation email sent to all users, who then will respond back to show that the emails are functioning properly.


### User Effect & Support

- User population will have an additional email account to setup and manage besides their user accounts within our system
- Users whom need assistance will be provided our emails in our documentation for contact if any issues or chnages are needed to be addressed.


### Security Issues

- Each account will be only accessible by user's personal public ssh key (or a new password theycreate for ease of access) to prevent unwanted third party user access.
- A possible security issue is if a client accidentally allows one or more third party access to their email account with/without their knowledge.


### Implementation

- We will use puppet and chron jobs to implement the email accounts, and build upon the previous account creation project


### Documentation

- Both user and system administration work involved with this project will be properly documented and posted on our defaultName GitHub repository for current and future references.

