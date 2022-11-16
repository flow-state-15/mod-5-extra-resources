# Welcome to Module 5 Project

![React and Redux Logos](https://miro.medium.com/max/800/1*meCFnZ5MK_7Fu1ogYfBvNQ.png)
> Guidelines for competing this project week!

## Overview
The Mod 5 Project is meant to assess your abilities to complete a frontend utilizing React, Redux, your Mod 4 custom API as the backend, JSX/HTML, and CSS in a week's time. All of these brought together for your *first full-stack project*! 🎉
This project will be in your portfolio for showcasing your skills to future employers and recruiters. The aim is to have 4 features eventually (after graduation) but for this week the minimum to complete is **2 core features**.
> If you start extra features, keep them on a separate branch until they are completed with full functionality. Incomplete features will need to be commented out for presentation and grading.

Everyone will have a staff member as their project advisor. Project Advisors will be leading standups every day with their group during Week 16 Project Week, where they keep track of your progress. You will be added to a team Slack channel with your project advisor before EOD Friday.
Presentations with your team and grading will occur on Monday morning, Week 17. By completing this project, you will officially be a **full-stack developer**!

![Bill Nye happy computer gif](https://media0.giphy.com/media/l3nWqD4ViFej9REAw/giphy.gif?cid=ecf05e47igpzk6ql1l16cjebsutwhnpzsrfllbidrgvcjwg2&rid=giphy.gif&ct=g)
> Be aware that this is a living document and subject to updates and is not a comprehensive list--should be supplemented by reading the materials on aA Open.

# Phase 1 - Authenticate Me & Project Proposals
Friday's homework had you start working on Authenticate Me Frontend.
You will be continuing with the clone site you made in the Mod 4 backend project. Please read the **React Solo Project Expectations**, along with the other materials, on AAO.
Please fill out and submit this [Mod 5 Project Proposal | Google Form](https://forms.gle/uz93a7oghJDgeGJY7) by Monday.
The fields it requires is:
```md
1. Clone: AirBnb or MeetUp
2. Project Name: CloneBnB
3. Github Repo Link: http://github.com/your-github-user/your-project-repo/
4. Github Wiki Link: http://github.com/your-github-user/your-project-repo/wiki (with the wiki pages complete)
5. Live Link: https://name-of-app.herokuapp.com
6. Scorecard Link: https://docs.google.com/scorecard... (please see below for the link to create your scorecard)
```
### Scorecard Link
Please create a scorecard for your project to submit in the proposal!
#### [Mod 5 Scorecard](https://docs.google.com/spreadsheets/d/1f3zBqm5YVQt2hBFq7NwHCByDobCcCkg85poZsqfiHWU/edit?usp=sharing)
1.  *File* > *Make a Copy*.
2. Fill out the top right section, from *Developer* to *Live Link*, as you get the information!

By Monday, you are expected to have completed Authenticate Me Frontend. This needs to be approved by your project advisor before you are allowed to move on to your features.
# Phase 2: Project Time!
## Standups vs Question Asking
### Standups
Standups usually occur during the mornings and before lunch, but the exact times will be posted on your team's slack channel by your project advisor. This is a time for us to see where you are at currently in your project and to see if you are reaching the goals you give yourself. An important skill to learn is prioritization and pacing.

During your turn, share your screen (both code and the actual site) and discuss what you worked on the day before, what you will work on today, and any blockers you are currently having. On Monday, staff will want you to demonstrate that your authentication is all working correctly. Throughout the week, you may be asked to demonstrate CRUD functionality for your features, too.

**An important aspect of standups is that this is not a time for debugging.** We have a limited amount of time to make sure we get a read on everyone. Project advisors might have some quick advice about where a problem is most likely arising but you will be asked to formulate a good question to post on your online-questions channel.

### What is a good question?
> "The effectiveness of being a Software Engineer can be proportional to your ability to ask effective questions." -- AAO

This is probably the most important skill we try to teach you here at App Academy. Being able to articulate what is occurring, what you actually want to occur, and what you have narrowed down... will help you become a highly sought after programmer.

Functionally, here in Mod 5, there is a lot of interacting parts (Between React, JSX, CSS, Redux, your backend... etc.)  so debugging can be a lengthy process. For staff to be able to effectively assist everyone with problems, we need as much context given to us and groundwork already completed.
**By groundwork we mean:**
1. **Have you console.logged any variables/data you are dealing with?**
	- Is it what you expected it to be? The right type? The right content?
2. **Have you narrowed down where the problem is happening in code? (Follow the dataflow!)**
	- Example: you're not getting the right data in your thunk.
		- So, go check your dispatch and payload in your component.
		- *Console.log that you are getting the expected data in every step of the process.*
	- Also narrowing down by commenting out code until an error goes away. So now you know it must be occurring around that code somewhere!

When you are writing a good question, include all this context. And a good thing to follow is this good question format below ⤵
### Good Question Format:
- [ ]   **What you are working on?**
- [ ]   **A description of the problem.**
    -   _What is occurring right now?_
    -   _What are you trying to achieve?_
- [ ]   **What error messages are you getting?**
	- Check all the places! On the backend server, frontend/browser consoles.
- [ ]  **Relevant screenshots of code and error messages**
	-  Include explanations of these screenshots, especially if its a large screenshot.
	- Please follow Slack etiquette and include screenshots in the same message/thread.
		- If you accidentally submit before adding screenshots, please post them within the thread of your original message.
- [ ]  **The debugging process you’ve done so far**  (Follow your data flow!).
- [ ] **Push your code to a branch on Github**
	- Give us the link/name of the specific branch
	- Make sure to include component/function/file names in your question so we know where to look.

> Helpful Links:
> - [Format Your Slack Messages](https://slack.com/help/articles/202288908-Format-your-messages)
> - [How to Take Screenshots](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/resources/how-to-screenshots-and-formatting.md#how-to-take-screenshots-and-format-code-on-slack)
### Lecture Questions Emoji System

Because the staff are asked to answer questions asynchronously when possible, staff will use slack reaction emojis to communicate the status of your question.

## 👀
The eyeballs mean the TA's are aware of the question and are looking into it / discussing it in the Staff Room. There may be other questions ahead of yours and it may take time to resolve the question based on the complexity of the problem and how clear the question was, if screenshots or commits were provided etc.

## ✅
The green check means that a TA or the student has confirmed that the question has been resolved. If this isn't correct tag one of staff in the thread or re-post the question.

## ☑️
The gray or blue check means the question seems to have been resolved by a TA or other student but is awaiting some form of confirmation.

-------------------------

# Feature CRUD
### For your first feature:
> AirBnB first feature must be **Spots**. Meetup first feature must be **Groups**.
- [ ] Must be a place to CREATE!
- [ ] Must be a place to READ!
- [ ] Must be a place to UPDATE!
	- *Hint:* will be similar to your CREATE (in styling, validations, etc.)
	- *you don't need to let user's edit the photo(s)--you can leave that input out.*
- [ ] Must be a way to DELETE!

### For your second feature:
- [ ] Must be a place to CREATE!
- [ ] Must be a place to READ!
- [ ] UPDATE is not required for this feature
- [ ] Must be a way to DELETE!

# AirBnB
![Airbnb logo banner](https://storage.googleapis.com/kaggle-competitions/kaggle/4651/media/airbnb_banner.png)
> See AAO "React Project Assessment > Project List" for list of approved features for AirBnB.
### Basic Pages Needed
 - Home Page
 - Spot Details Page
 - Create Spot Page or Modal
 - Edit Spot Page or Modal
 ### Modals Needed
 - Sign Up Modal
 - Log In Modal

### Extra Pages & Modals
> Not required to pass but good to have eventually!
- Profile Page
	- User's Reviews
	- User's Spots
	- User's Bookings
- Create Review as Modal
- 404 Page

## Forms

Some advice on specific features:
#### Spots
- **Edit form doesn't need to include the option to edit the previewImage.**
 - **Longitude and Latitude don't need to be input fields**
	 - Regular users aren't going to know this information; its usually an external map API that would be able to calculate these from address input.
	 - For now, sending a hardcoded/default value to your backend will suffice the requirement.
	 - Later it would be great to refactor and implement something like Google Maps API into your project to replace the hardcoded data.

# Meetup
![meetup logo banner](https://img.freepik.com/vector-premium/concepto-meetup-colegas-empresarios-personajes-empleados-empresa-pausa-cafe-personas-que-comunican-charlan-pasan-tiempo-libre-juntos-discuten-cuestiones-laborales-ilustracion-vectorial-dibujos-animados_87771-14282.jpg)
> See AAO "React Project Assessment > Project List" for list of approved features for Meetup.
### Basic Pages Needed
 - Splash Page
 - Home Page
	 - Tab for viewing list of groups
	 - If events is your second feature, tab for viewing list of events
	 - *see actual Meetup site to visualize the tabs*
 - Group Details Page
 - Create Group Page or Modal
 - Edit Group Page or Modal
 - Event Details Page (if events is your second feature)
 - Create Event Page or Modal (if applicable)
 - Edit Event Page or Modal (if applicable)
 ### Modals Needed
  - Sign Up Modal
 - Log In Modal
 ### Extra Pages & Modals
 > Not required to pass but good to have eventually!
- Profile Page
	- User's Created Groups
	- User's Events
	- User's RSVPs
	- User's Joined Groups
- Create Modal for second feature
- 404 Page
## Forms
Some advice on specific features:
#### Groups
- **Edit form doesn't need to include the option to edit the previewImage.**
- **Meetup has a multi-step create form for groups. You do NOT need a multi-step form.** You are allowed to put all the input fields on one page.

------------------------------------

## General Advice
 - If you cannot view a part of your clone site because you would have to pay (like reviewing a spot or creating a group)
	 - It does not have to be accurate to the site! Please copy the styling and format from the forms and pages you can see.
- NPM packages must be approved by your project advisor.
- CSS frameworks are not allowed.
- NOTE: **Programatic hard refreshes are not allowed**. This includes manipulating the url through the `window` object. React provides all the tools necessary for dynamic rerendering or window relocation. If you have to have to refresh the page to see your data this is an indication that your reducer/selector code is bugged.

<hr />

## Helpful Links Resources for Mod 5 Project Week

- [GitHub README and Wiki Guidelines](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/project-week/github-README-and-wiki-guidelines.md)
- [Whit's CSS Tips](https://docs.google.com/document/d/1VkeCDf12jokoTdriQycheyfnlfdc-qypDXsxCO5tqNk/edit?usp=sharing)
- [Helpful Heroku Tips](https://github.com/whitnessme/helpful-heroku-tips)

### Grading and Presentation Requirements

- [React Project CSS Grading Specs][css-grading-specs]
- [React Project Grading and Presentation Process][grading-presentation]

### Project Resources

- [Question Asking Protocol][question-asking-protocol]
- [GitHub README and Wiki Guidelines][readme-wiki-guidelines]
- [Design and Styling Resources][design and styling]

### Database Schemas Examples

- [AirBnb][airbnb]
- [Meetup][meetup]
- [SoundCloud][soundcloud]

### Database Schema Creation Apps

- [dbdiagram.io][db-diagram]
- [drawSQL][draw-sql]
- [Quick DBD][quick-dbd]

### Redux Store Shape Examples

- [Redux Stores][redux-stores]

### Guides

- [AWS S3 for User Uploads][aws-s3-user-uploads]
- [AWS S3 Only for Storage][aws-s3-only-storage]
- [Cloudinary Basic Setup][cloudinary-basic-setup]
- [Fullstack DataFlow][fullstack-data-flow]
- [Google Maps API Walkthrough][google-maps-api-walkthrough]
- [Migration Updating in Sequelize][sequelize-migration-update]
- [Sequelize Cascade Delete][sequelize-cascade-delete]
- [Supplemental Authenticate Me Read Along][authenticate-me-read-along]

<p align="right" style="font-size:10px">
  <a href="../README.md">Back to main README.md</a>
</p>

<!-- grading information -->

[css-grading-specs]: ./css-grading-specs.md
[grading-presentation]: ./overview-of-react-project-grading-process.md.md

<!-- project links -->

[question-asking-protocol]: ./question-asking-protocol.md
[readme-wiki-guidelines]: ./github-README-and-wiki-guidelines.md
[design and styling]: ./project-week/design-and-styling.md

<!-- schema example links -->

<!-- These are not currently options for mod 5 but may return in the future -->
<!-- Move these links up when they are available again -->
<!-- - [bandcamp][bandcamp] -->
<!-- - [eventbrite][eventbrite] -->
<!-- - [evernote][evernote] -->
<!-- - [flickr][flickr] -->
<!-- - [medium][medium] -->
<!-- - [producthunt][producthunt] -->
<!-- - [quora][quora] -->
<!-- - [untappd][untappd] -->
<!-- - [yelp][yelp] -->

[airbnb]: ../assets/db-schemas/airbnb.jpg
[bandcamp]: ../assets/db-schemas/bandcamp.jpg
[eventbrite]: ../assets/db-schemas/eventbrite.jpg
[evernote]: ../assets/db-schemas/evernote.jpg
[flickr]: ../assets/db-schemas/flickr.jpg
[medium]: ../assets/db-schemas/medium.jpg
[meetup]: ../assets/db-schemas/meetup.jpg
[producthunt]: ../assets/db-schemas/producthunt.jpg
[quora]: ../assets/db-schemas/quora.jpg
[soundcloud]: ../assets/db-schemas/soundcloud.jpg
[untappd]: ../assets/db-schemas/untappd.jpg
[yelp]: ../assets/db-schemas/yelp.jpg

<!-- external db schema creation apps -->

[quick-dbd]: https://www.quickdatabasediagrams.com/
[draw-sql]: https://drawsql.app/
[db-diagram]: https://dbdiagram.io/home

<!-- redux stores -->

[redux-stores]: ../assets/react-redux-state-shape.md

<!-- guides links -->

[aws-s3-user-uploads]: https://github.com/jdrichardsappacad/aws-s3-pern-demo
[aws-s3-only-storage]: https://github.com/Lazytangent/aws-s3-just-storage
[authenticate-me-read-along]: https://github.com/Lazytangent/authenticate-me-read-along
[cloudinary-basic-setup]: https://github.com/Lazytangent/Cloudinary-BasicSetup.git
[fullstack-data-flow]: https://github.com/Lazytangent/DataFlow
[google-maps-api-walkthrough]: https://github.com/Lazytangent/Google-Maps-API-Walkthrough
[sequelize-cascade-delete]: https://github.com/Lazytangent/sequelize__migration_hooks
[sequelize-migration-update]: https://github.com/Lazytangent/migrations-demo-with-sequelize

<!-- - [Module 5 Project Week Resources][solo-project-resources] -->
<!-- [project-resources]: https://github.com/Lazytangent/Mod-5-Project-Week -->
