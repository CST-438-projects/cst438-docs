# CST 438 Project 3 Guide

# Overview

The major goal of this assignment is to **work in groups** to produce a **demo** of a high quality professional project.  Secondary goals are to allow students to practice the skills necessary to design and develop a fully featured project on a tight timeline. This is a student driven project meaning that you will be the expert.   
What you create is up to you; within some constraints.

## What you build

This is a little bit open. You will have a few days to think about this. It must be something that can be accomplished via a web app; a service or feature YOU WANT TO EXIST.    
You will have \~3 minutes as a team to sharktank your ideas to the faculty.  

# Assignments

* Pitch presentation  
  * You will present what you are building to the class along with goals and a timeline  
* Code review  
  * Review each others code  
  * Review the code from another team  
* Midpoint test  
  * Each team will use and review the work of a subset of other teams (probably 3\)  
* Final presentation  
  * Present your product and compare it to the original presentation  
* Forms  
  * Team evaluations

# 

# Project Components

## Front end

* Web  
  * Reactive front end  
  * Must be hosted on Render, AWS, Google Cloud Platform or similar  
* Mobile  
  * **One** of Android OR iOS  
  * You can DO both but **only one is required**  
* Consistent UI across platforms  
* OAuth2 \-\> Spring Security OAuth2  
  * AT LEAST TWO OAuth PROVIDERS  
  * Google and Github for example  
* Containerized with Docker

## Backend

* API with at least 8 endpoints  
  * MUST be done in Spring Boot  
    * So no Supabase or Firebase for endpoints.   
    * Supabase or Firebase for the Database is fine.  
  * Must be hosted SEPARATE from the front end  
* Handle CORS using backend features  
  * [Spring](https://spring.io/guides/gs/rest-service-cors)  
* Database  
  * [Supabase](https://supabase.com/) PostgreSQL it is the easiest.  
* Docker  
  * Backend containerized

## Testing

* Front end  
  * JEST unit tests  
  * Playwrite for automation tests  
* JUnit for Spring Boot  
* Postman testing for routes

## Deployment

* Connect your app from GitHub to render and automatically pull a branch when it is updated  
  * Probably a good idea to make sure whatever is merged doesn't break anything…  
    * Meaning you need unit tests to pass before deploying  
* Make GitHub run all your tests when something is pushed  
  * Each developer needs to test their own work  
  * [Red/Green/Refactor for the win](https://www.codecademy.com/article/tdd-red-green-refactor)

# Documentation

Your team will be responsible for the creation and submission of:

* Proposal document  
* [Product Requirement Document](https://www.atlassian.com/agile/product-management/requirements)  
  * Include what is required for the Minimum Viable Product  
* In code documentation  
  * Each Class/object needs to have robust documentation  
  * Other teams will be looking for this.  
* GitHub Issues  
  * Issues should not be user specific.  
  * Issues should contain enough detail that an outsider can accomplish it  
    * That sounds like a good assignment  
* Pull Requests  
  * Have a branch protection rule  
  * NO MERGES TO MAIN  
* Midpoint evaluation  
  * Each team will evaluate their progress in the middle.  
* Post mortem evaluation  
  * Each team will evaluate their progress at the end  
* Final Presentation  
  * Each team will present their work

# 

# Team requirements

Each team member is responsible for an entire vertical slice of the project. Meaning you can not just work on the front end or back end. You will be responsible for the entirety of a feature from the DB table to the View the user interacts with. 

Have at least 1 issue for each of:

* Entity creation  
  * Java file that results in a database table  
* Route  
  * If it exists in the DB there needs to be a get route  
* Page/view   
  * There needs to be a front end page that displays it

# 

# MVP and Vertical Slice

## MVP

A minimum viable product is the minimum set of features needed to show off a completed application.  

* Sign up /onboarding  
  * Account creation and setup  
* Update user information  
* Delete account

## Vertical Slice

A FULLY POLISHED activity from the MVP.  It should demo the feeling and goal of the application. 

## Appendix I: OAuth2 Flow with Spring Security

**Resource Owner**: The user (person logging in)  
**Client**: Your Spring Boot application  
**Authorization Server**: OAuth2 provider (Google, GitHub, etc.)  
**Resource Server**: Where user data lives (often same as Auth Server)

### The Authorization Code Flow 

Step-by-Step Process:  
**1\. User Initiates Login**  
User clicks "Login with Google" in React Native app  
React Native redirects to:   
https\://your-springboot-api.com/oauth2/authorization/google

**2\. Spring Boot Redirects to Google**

Spring Security redirects user to Google:  
https\://accounts.google.com/o/oauth2/auth?  
  client\_id=YOUR\_CLIENT\_ID  
  \&redirect\_uri=https\://your-springboot-api.com/login/oauth2/code/google  
  \&response\_type=code  
  \&scope=openid email profile

**3\. User Authenticates with Google**  
\- User logs into Google (if not already)  
\- Google shows consent screen: "App X wants access to your profile"  
\- User clicks "Allow"

**4\. Google Redirects Back with Authorization Code**

Google redirects to:  
https\://your-springboot-api.com/login/oauth2/code/google?code=AUTH\_CODE\_HERE

**5\. Spring Boot Exchanges Code for Tokens**  
\`\`\`  
Spring Security makes POST request to Google:  
POST https\://oauth2.googleapis.com/token  
Body:  
  code=AUTH\_CODE\_HERE  
  client\_id=YOUR\_CLIENT\_ID  
  client\_secret=YOUR\_CLIENT\_SECRET  
  redirect\_uri=https\://your-springboot-api.com/login/oauth2/code/google  
  grant\_type=authorization\_code

Google responds with:  
{  
  "access\_token": "ya29.a0...",  
  "refresh\_token": "1//0g...",  
  "id\_token": "eyJhbG...",  
  "expires\_in": 3600  
}  
\`\`\`

**6\. Spring Boot Gets User Info**  
\`\`\`  
Spring Security uses access\_token to call:  
GET https\://www\.googleapis.com/oauth2/v3/userinfo  
Authorization: Bearer ya29.a0...

Response:  
{  
  "sub": "123456789",  
  "email": "user@gmail.com",  
  "name": "John Doe",  
  "picture": "https\://..."  
}

**7\. Spring Boot Creates Session**

Spring Security creates a user in your app  
Stores user in database (via Supabase PostgreSQL)  
Creates session/JWT token for your app  
Redirects user back to React Native with your app's token

## Appendix II: Testing Resources (Thank you Ahmed\!)

**GitHub repo containing the example code and notebook Ahmed used:**  
[https\://github.com/AhmedTurkiii/software-testing/blob/main/Software-Testing.ipynb](https://github.com/AhmedTurkiii/software-testing/blob/main/Software-Testing.ipynb)

**PRD (Product Requirement Document)** – \~*20 mins*  
[https\://www\.atlassian.com/agile/product-management/requirements](https://www.atlassian.com/agile/product-management/requirements)

**AAA’s Software Pattern (Arrange, Act, Assert)** – \~*10 mins*  
[https\://semaphore.io/blog/aaa-pattern-test-automation](https://semaphore.io/blog/aaa-pattern-test-automation)

**Setup and Teardown in Testing** – \~*15 mins*  
[https\://jestjs.io/docs/setup-teardown](https://jestjs.io/docs/setup-teardown)

## Appendix III: Sample Project

## Campus Resource Booking System

A mobile-first platform where students can browse, reserve, and manage campus resources like study rooms, lab equipment, tutoring sessions, and meeting spaces.

**Team Member 1: Authentication & User Management**

* OAuth2 login (Google/GitHub for "university SSO" simulation)  
* User profiles (student, staff, admin roles)  
* Role-based access control  
* Account settings and preferences  
* **Unit Tests**: Auth service, user repository, JWT utilities  
* **E2E Tests**: Login flow, profile updates

**Team Member 2: Resource Management & Search**

* CRUD operations for resources (rooms, equipment, tutors)  
* Search and filter resources (by type, availability, location, features)  
* Resource details with photos, capacity, amenities  
* Admin dashboard to add/edit resources  
* **Unit Tests**: Resource service, search algorithms, filter logic  
* **E2E Tests**: Browse resources, search functionality, admin CRUD

**Team Member 3: Booking & Scheduling**

* Create/cancel bookings  
* Check availability (prevent double-booking)  
* Calendar view of bookings  
* Booking history  
* Waitlist functionality for popular resources  
* **Unit Tests**: Booking validation, conflict detection, time slot logic  
* **E2E Tests**: Complete booking flow, cancellation, conflict scenarios

**Team Member 4: Notifications & Analytics**

* Email/push notifications (booking confirmations, reminders, cancellations)  
* Dashboard analytics (most popular resources, peak times, utilization rates)  
* Booking reports for admins  
* User statistics (no-show tracking, usage patterns)  
* **Unit Tests**: Notification service, analytics calculations  
* **E2E Tests**: Notification triggers, dashboard displays