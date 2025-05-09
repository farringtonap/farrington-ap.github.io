[![ci-nextjs-application-template](https://github.com/farringtonap/apcoursemanager/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/farringtonap/apcoursemanager/actions/workflows/ci.yml)

# Overview
At Farrington High School, they offer Advanced Placement (AP for short) courses that help prepare 9th-12th graders for college-level classes. At the end of the school year, students can take the AP exam and can earn college credit based on their score. However, it is hard to get students to apply for the various APs offered at Farrington due to the lack of marketing and promotion for them. Even though there are tools like Google Sites, it’s hard for teachers and staff to utilize them as they have to learn how to use it and also understand and apply core web design principles to market their class in a stylish, informative way; which takes away time that they could use for lesson plans, grading assignments, and preparing them for the exam. Using our tech stack, we can implement a web app that abstracts away the design aspect and allows the faculty and staff of the AP program to focus more on updating information for the AP Classes. The idea here is that trusted users can login to the app and then update class availability and information, while students can look at the website to see what classes will be offered for the upcoming school year and get a general idea of what the class is about.

# User Guide

Learn how to navigate our website here!

### Landing Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/landing-page.png)

The landing page provides general information about AP classes at Farrington HS like the benefits, purpose, no-drop policy, etc.

### AP Classes Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/ap-classes-page.png)

This page displays are the AP classes offered at Farrington HS. If it is offered that school year there will be a green checkmark image, if not it will show a red cross instead.

### Assessment Form Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/assessment-form-page.png)

This page leverages the power of AI by giving a student recommended after they fill out the form. This form asks a student their interests, previous courses taken, GPA, and current grade. 


#### Note: The next few pages can only be accessed by a trusted user like an admin.

### Add/Edit Classes Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/add-edit-classes-page1.png)
This section of the page allows trusted users to add AP classes and allows them to fill out fields like, class name, teacher email, description, etc.

![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/add-edit-classes-page2.png)
The section manages current AP classes by either editing a certain fields or deleting them entirely.

### Add/Edit Subjects Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/add-edit-subject-page.png)
This page allows an admin to add, edit or delete a current subject. Adding a subject is as simple as inputting the subject name and clicking the add subject button. As for editing, a user would need to click edit and modify the desired field. And the delete button wipes that subject from the database

### Add/Edit Prerequisites Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/add-edit-prerequisites-page.png)
This page allows an admin to a new prerequisite by adding the prerequisite name and including the subject its attached to. Editing a prerequisite changes its name and the subject its attached to. And deleting wipes it from the database 

### Admin Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/admin-page.png)
The admin page allows the admin only to add and edit current users in the database for example, they could change a teachers name or email address.

### Sign In Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/signin-page.png)
The sign in page allows a user who is currently in the database to sign in with their credentials in order to access their side of the site like and admin or teacher.

### Sign Up Page
![Screenshot of the Landing Page for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/user-guide-images/signup-page.png)
The sign up page is for users currently not in the database like a new teacher to get in the database and have the powers of a teacher on the site.

# Developer Guide

This codebase uses the following technologies:
- NextJs &rarr; Opinionated framework that handles routing, authentication, and much more. 
- React &rarr; Reusability for components across website
- Bootstrap &rarr; Styling framework 
- Prisma &rarr; ORM to easily manage and update the structure and schema of the database
- Postgres &rarr; Database to house data related to the AP Courses
- Playwright &rarr; Visual regression testing for websites

### Getting Started

1. Run `npm install` to install all dependencies for this project
2. Create a `.env` file in the root directory
3. Add in the secrets from the discord into the `.env` file
4. Modify the `DATABASE_URL` secret 
    - update username to your postgres account
    - update password to your postgres account
5. Create your db located in the `DATABASE_URL`
6. Run the following commands in the terminal
    - `npx prisma db migrate`
    - `npx prisma db seed`
7. Afterwards, run `npm run dev` and verify that local development works. 

### Getting the AI Working

1. Install python & pip (pip should come with python install)
2. `python -m venv venv` to create a virtual environment called `venv`
3. Activate the virtual environment 
    -  Mac / Linux: `source path/to/venv/Scripts/Activate`
    -  Windows: `path/to/venv/Scripts/Activate`
4. cd into python-backend
5. Run `pip install -r requirements.txt`
6. cd back into root directory and run `uvicorn main:app --reload --port 8000`

# Deployment

[https://apcoursemanager.vercel.app/](https://apcoursemanager.vercel.app/)

# Community Feedback
After getting community feedback from 5 Farrington HS community members who tested our application's functionality here are the main points they had to say about it

### User Friendly
The application was very user friendly for both students and school faculty as it enables students to quickly look for the currently offered AP classes for that semester, and allows faculty to swiftly make quick changes.

### User Interface
It was noted that the UI, especially the navbar, were both nice to look at and server their purpose. For the faculty, the use of dropdowns were very convenient. Along with the buttons such as, add and delete being green and red respectively adds to simplicity of using the application.

### One Background Image
Another thing of note was that while using the football field of Farrington HS was nice, it gets bland, especially when its on every page. One thing that could improve upon it would be to add different angles or different images of the school on each page. Also, possibly picking a images better suiting each page as some of the text needed a box shadow in order to be seen.

### Consistency
While the website design does its best to look consistent across the board there are still some inconsistency to be seen. For example, on the Add/Edit AP Courses page the two cards present are not the same width. 

# Relative Links

Github Organization: [https://github.com/orgs/farringtonap/repositories](https://github.com/orgs/farringtonap/repositories)

Team Contract: [https://docs.google.com/document/d/1ze4JMEOuv-2TEV-2IcM4VQ12fONRzIiYdRZjDBzn8aI/edit?usp=sharing](https://docs.google.com/document/d/1ze4JMEOuv-2TEV-2IcM4VQ12fONRzIiYdRZjDBzn8aI/edit?usp=sharing)

# Mockups Pages

## Landing Page
![Screenshot of the Landing Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/landing-page-mockup.png)
The landing page explains both the purpose and benefits of taking an Advanced Placement (AP) class.

## AP Classes Page
![Screenshot of the AP Classes Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/apclasses-page-mockup.png)
The AP classes page will display the current AP subjects that Farrington High School offers. This gives students and parents a general overview of the subjects that have an AP class.

## AP Classes(Expanded) Page 
![Screenshot of the AP Classes(Expanded) Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/apclasses-expanded-page-mockup.png)
When clicking on a AP subject it will expand to show all available AP classes for that subject. For example, AP Math contains the AP Statistics and AP Calculus classes. 

## AP Classes(Full) Page
![Screenshot of the AP Classes(Full) Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/apclasses-full-page-mockup.png)
Once choosing a class of interest it will show a full page of information regarding the chosen class. It will display information like, the teacher, teacher's email, credits provided, class schedule, and a description of the class.

## Login Page
![Screenshot of the Login Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/login-page-mockup.png)
The login page is meant for trusted users at Farrington High School like an AP Coordinator or AP Teacher to login and make changes to AP classes.

## AP Coordinator Page
![Screenshot of the AP Coordinator Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/ap-coordinator-page-mockup.png)
The AP Coordinator page is meant for the AP Coordinator is make AP classes by assigning the class's name, credits provided, teacher's name and email, and inital class schedule.

## AP Teacher Page 
![Screenshot of the AP Teacher Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/ap-teacher-page-mockup.png)
The AP Teacher page is similar as it is meant for the AP Teacher of the class to update information about the class like, the teacher's name and email, the class schedule, and provide a description for the class.

## Assessment Form Page 
![Screenshot of the Assessment Form Page Mockup for apcoursemanager](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-designmockup/assessment-form-page-mockup.png)
The Assessment Form page is meant for students to provide information on their strengths and weaknesses in certain subjects. After the form is filled out we will dynamically generate classes that would best fit the student based on their strengths.

# M1

Project Board Link: [https://github.com/orgs/farringtonap/projects/3](https://github.com/orgs/farringtonap/projects/3)

# Milestone 1 Progression

## Landing Page
![Screenshot of the current Landing Page for Milestone 1](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone1/landing-page-milestone1.png)

## Sign In Page
![Screenshot of the current Sign In Page for Milestone 1](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone1/sign-in-page-milestone1.png)

## Sign Up Page
![Screenshot of the current Sign Up Page for Milestone 1](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone1/sign-up-page-milestone1.png)

# M2

Project Board Link: [https://github.com/orgs/farringtonap/projects/4](https://github.com/orgs/farringtonap/projects/4)

# Milestone 2 Progression

## Landing Page
![Screenshot of the current Landing Page for Milestone 2](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone2/landing-page-milestone2.png)

## AP Classes Page
![Screenshot of the current AP Classes Page for Milestone 2](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone2/ap-classes-page-milestone2.png)

## AP Classes Detail Page
![Screenshot of the current AP Detail Classes Page for Milestone 2](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone2/ap-classes-detail-page-milestone2.png)

## Assessment Form Page
![Screenshot of the current AP Classes Page for Milestone 2](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone2/assessment-form-page-milestone2.png)

## Sign In Page
![Screenshot of the current AP Classes Page for Milestone 2](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone2/sign-in-page-milestone2.png)

## Sign Up Page
![Screenshot of the current AP Classes Page for Milestone 2](https://raw.githubusercontent.com/farringtonap/apcoursemanager/refs/heads/main/doc/apcoursemanager-current-state-milestone2/sign-up-page-milestone2.png)

# M3

Project Board Link: [https://github.com/orgs/farringtonap/projects/3](https://github.com/orgs/farringtonap/projects/5)
