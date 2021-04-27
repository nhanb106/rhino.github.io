## Table of Contents

* [Goal of this Project](#goal-of-this-project)
* [Deployment](#deployment)
* [User Guide](#user-guide)
* [Community Feedback](#community-feedback)
* [Developer Guide](#developer-guide)
* [Development History](#development-history)
* [Contact Us](#contact-us)

## Goal of the Project

The goal of this project is to address the many stray cats on UH Manoa's campus. "Meow Mapper" will allow users to track cats and see which have been fed/provided with veterinary care and which have not. 

![ci-badge](https://github.com/meow-mapper/meow-mapper-deploy/workflows/ci-meow-mapper-deploy/badge.svg)

## Deployment

A live deployment is available at [https://meowmapper.com/](https://meowmapper.com/)


## User Guide

### Landing Page

The landing page is the first page presented to users when they visit the URL to the site. A navbar with more options will be available on logging in. 

![](Images/landingNew.PNG)


### Cat Pictures Page

This page is where users can share pictures of the cats they see around campus. 

![](Images/cat-snaps-mockup.png)

### Login Page

This is the page a user sees directly after logging in. A personal feed that the user can change based on their specific goals for using the website.

### Spay-and-neuter Page

This is the page that is run in affiliation with the Humane Society with the end goal of less stray cats on campus. 
![](Images/Neuter.png)

### Snatch-a-cat Page

This is the page that where users can go to choose a cat to adopt. 
![](Images/Snatch.png)

## Donations

Users can provide donations to contribute to feral cat feeding stations around campus.
![](Images/Donate.png)

## Community Feedback

We would love to hear from our users! Please feel free to contact us with ideas for improvement. 


## Developer Guide

### Installing 

First, install [Meteor](https://www.meteor.com/developers/install).

Second, go to [https://github.com/meow-mapper/meow-mapper-deploy](https://github.com/meow-mapper/meow-mapper-deploy) and download the masters.

Third,  go to your newly created repository, and click the “Clone or download” button to download your new GitHub repo to your local file system. Using GitHub Desktop is a great choice if you use MacOS or Windows.

Fourth, cd into the app/ directory of your local copy of the repo, and install third party libraries with:
![](Images/installing.png)

### Running the system
Once the libraries are installed, you can run the application by invoking the “start” script in the package.json file:
![](Images/running1.png)
The first time you run the app, it will create some default users and data. Here is the output:
![](Images/running2.png)

### Note regarding “bcrypt warning”:
You will also get the following message when you run this application:
![](Images/bywarning.png)
On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

### Note regarding “MongoError: not master and slaveOk=false”:
Intermittently, you may see the following error message in the console when the system starts up:
![](Images/merror1.png)
While irritating, this message appears to be harmless and possibly related to a race condition between the development instance of Mongo and Meteor. By harmless, I mean that in most cases, the console goes on to display App running at: http://localhost:3000/ and no problems occur during run time.

### Viewing the running app
If all goes well, the template application will appear at [http://localhost:3000](http://localhost:3000). You can login using the credentials in settings.development.json, or else register a new account.

###ESLint
You can verify that the code obeys our coding standards by running ESLint over the code in the imports/ directory with:
![](Images/esl.png)

### Walkthrough
The following sections describe the major features of this template.

#### Directory structure
The top-level directory structure is:

## Development History

[Milestone 1:](https://github.com/meow-mapper/meow-mapper/projects/1) 4/15/2021
- Website functionality confirmed
- Mockups for pages finalized
- Landing page created

[Milestone 2:](https://github.com/meow-mapper/meow-mapper/projects/4) 4/27/2021
- Create working webpages
- Implement github actions
- Implement TestCafe "availability" tests for all pages

[Milestone 3:](https://github.com/meow-mapper/meow-mapper/projects/3) 5/4/2021
- Get community feedback on our webpage

## Contact Us

The developers of this project are Kha Bui, Nhan Bui, Germaine Juan, and Maegan Chow.


