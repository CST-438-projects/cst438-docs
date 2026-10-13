# Project 01
# Android based API app
# Description

For this project teams will work together to build an app that consumes information from a REST API and uses a **local database** for caching. The values from the API may be stored in the local database. 

**The app will be built using Android Studio and  Kotlin.**

# What we will do

* Design, plan, and implement a mobile application that consumes an API.   
* Use the agile process  
* Create use stories  
* Create github issues  
* Each issue must have a(n):  
  * assignee  
  * precondition  
  * TESTABLE postcondition/acceptance criteria  
  * passing test  
  * A unique branch  
* Learn to use Kotlin

# 

# Minimum Viable Product (MVP)

- [ ] Authenticate users  
      - [ ] OAuth is not required but will be for the next project… maybe?  
- [ ] Fetch data from an API  
      - [ ] DO NOT CREATE YOUR OWN API  
- [ ] Store information locally  
- [ ] Display persistent information  
- [ ] (optional ish) Create users

#  

# Must haves (non-negotiable)

* Allow users to log in and see something specific to them  
* Pull from a web based REST API  
  * See [here](https://github.com/public-apis/public-apis?tab=readme-ov-file) for a list though you aren't limited to these  
* Use Kotlin  
  * use [composeable UI](https://developer.android.com/develop/ui/compose/mental-model)  
  * DO NOT create the UI with XML  
* Use local storage  
  * [Link to Kotlin docs on Room](https://developer.android.com/training/data-storage/room/)  
  * 100% inflexible on this. I don't want data stored on Firebase.  
* Use Git and Github  
  * Each week I will run a script to check for a pull requests  
  * The individual contributions to the github repo will be a major part of the evaluation of this project.  
    * This means everyone MUST contribute.  I don't want to hear "I didn't do anything because…"

## 

## Example apps:

#### Job listings

User creates a login and selects a set of interests from a drop down. The app uses [a job API list](https://github.com/public-apis/public-apis#jobs) to list jobs based on the skills selected. Maybe let the user save the jobs to the phone (I'd say save the ID to the ROOM DB and load it when the app loads). Users should be able to modify their profile to change what jobs they are interested in.

#### Fitness App

Users create a login and can then select exercises provided by a [fitness API](https://wger.de/en/software/api). Username and password should be used to get an API token that will be stored locally. The app will allow the user to store exercises and workout plans.

#### [Sports](https://github.com/public-apis/public-apis?tab=readme-ov-file#sports--fitness) Win Predictor

Users create a login and select their favorite teams. The app then gives the user predicted outcomes of upcoming matches. It will also allow them to change which teams they want to follow. The basis of the win is that, across all sports, teams that play at home have a \> 50% chance of winning.  

#### 

 

# 

# Learning Outcomes Addressed

1. Apply, Analyze, and Integrate software engineering processes.   
   Including:  
   1. requirements analysis  
   2. Software design  
   3. test driven development  
   4. code review  
   5. continuous integration and deployment  
   6. agile planning and execution (i.e. user stories)  
   7. retrospectives  
   8. peer feedback.  
2. Practice and Evaluate Software Development lifecycles  
   1. Specifically: Continuous integration, Incremental development, waterfall development and others as time permits  
3. Build and Evaluate software using the agile development model as defined in the textbook used in this course.  
4. Evaluate, Explain, and Apply team management skills  
   1. Establish clear team roles and expectations  
   2. Set realistic milestones  
   3. Peer-review and evaluation  
   4. Effective communication  
   5. Project management  
5. Identify, Explain, and Apply proper source control  
   1. Manage commits to a shared repository  
   2. Use proper comments and style when adding code to git  
6. Critique, Prepare, and Evaluate Professional Communication  
   1. Prepare and present information about projects  
   2. Critique and assess other student work, including presentations.

# 

# Resources

* [Learn Android Kotlin](https://developer.android.com/kotlin/campaign/learn)  
* Fake API for mocks and testing: [jsonplaceholder.typicode.com/](http://jsonplaceholder.typicode.com/)  
* A list of free APIs: [https://github.com/public-apis/public-apis](https://github.com/public-apis/public-apis)  
  * Pixel Avatars: [https://avatars.dicebear.com/](https://avatars.dicebear.com/)

# 

# Updates Aug 20, 2026

* Minor formatting and requirements updates

## Aug 21, 2025 V2.5.2

* Minor formatting

## Jan 14, 2025 V 2.5.1

* Formatting and cleaning up language  
* Removed one requirement

## Sep 6, 2024 V 2.5.0.

* Updated the language to not focus on the android Room library and instead to focus on local (SQLite) storage.

## Aug 23, 2024 V 2.0.0.

* Added an update section  
* Added versions  
   

