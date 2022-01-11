

# Project 3 - Airbnb experiences

![home page](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908227/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/Home_ulwgvd.png)




## Overview

**Group members:** Rhona Petersen, Talia Glantz, Anna Wilczynska, Jamie Joahill

This was my third general assembly project. We had one week to build a full stack MERN application. Using React on the front-end and a Django, Python back-end. We decided to build a clone of the Airbnb experiences section of the Airbnb site.

## Brief

* Build a full stack application. 
* Use an Express API to serve your data from a Mongo database.
* Consume your API with a separate front-end built with React.
* Be a complete product which most likely means multiple relationships and CRUD functionality. for at least a couple of models.
* Have a visually impressive design.
* Be deployed online.

## Deployment

[Deployed project link](https://sei-project-3-59.herokuapp.com/)
## Time frame

7 Days
## Tech Stack


| Front-end | Back-end | Other tools | Version Control | APIs used|
|:----------| :---- |:-----------| :-------------| :---|
| JavaScript (ES6) | Node.js | Google dev tools | Git| Mapbox |
| React | Express | Insomnia | GitHub | Cloudinary |
| React Router | MongoDB | VS Code live share |
| Axios | JSON web token| Figma |
| CSS | Bcrypt | Yarn | 
| Semantic UI | Mongoose | Slack 
|Font awesome| Nodemon||Zoom|
|Rsuite| Dotenv |

## Planning

As soon as we received the brief my team and I started brainstorming ideas about the type of application we wanted to create. Afterwards we each spoke about our ideas and we settled on creating a clone of the Airbnb experiences section from Airbnb. We wanted to take an agile methodology approach to our build so we set up a Trello board that would not only detail what features to include but it would help us track our project’s build throughout the week. We also decided to do daily stand-ups, where we could talk about any issues we were having and see where we could help each other out. Throughout the day we would also keep in touch using slack, this was great because we used this to organize our evening meeting on Zoom to speak about what we had done during the day.

We used a Trello board to map out the back-end and front-end features. This was a good planning tool to use as it allowed us to see what needed to be done to create the application. Breaking everything down into smaller, more manageable goals to achieve. 

![trello here](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908229/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/Trello_hd2ae9.png)

We set up our backend very quickly. Everyone was involved in the creation of our experience model. We thought it would be best if we were all involved in this process so we could all have an input in what data our main model should contain. This is our main experience modal schema: 

![exp schema here](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908226/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/expschema_hfapwq.png)

![review schema here](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908226/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/reviewschema_s3momu.png)

![date schema here](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908227/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/dateschema_bjvsyi.png)


**Work split**

Rhona Petersen - 
Back-end 
User profile page

Talia Glantz - 
List all events
Favourite events

Anna Wilczynska - 
Navigation bar
Login/Register model
Home page 

Jamie Joahill - 
Back-end
Show event page
Add experience form

**Application functionality**

* User can view events
* Register/Login
* Favourite event/events
* Create an event
* Delete an event
* Search for an event

## Visuals

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908229/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/showexp_xzgmnv.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908228/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/showexp2_ovt37o.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908228/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/showexp3_r61vik.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908228/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/showexp4_wktrtb.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908226/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/add_experience_page_dwaggy.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908226/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/add_experience_page_2_lmcooh.png)



## Build

If you are logged in and you are the owner of that experience you can choose to delete it from the application. I wrote this helper function to allow me to gain access to the payload that is stored within local storage.

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908227/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/helpers_e4duta.png)

After I created this helper function, I could use it anywhere within the application. I used it to check if there was a payload inside local storage and if there was I would then check if the currentHostId matches the payload.sub that was stored in local storage. If this was true then a delete button would appear on the experience page to indicate to the user that this was their experience and it could then be deleted.

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908229/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/userisowner_tuvkpu.png)

This is how I structured the JSX. I passed in the userIsOwner function then experience host id. If this was true then it would display the delete button onto the page. If the button was clicked it would then fire off the handleDelete function. Which would use the axios delete request to remove that experience from our database.

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908227/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/isDeleted_fbyjb7.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908229/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/yogawithgoats_zb0rar.png)


## Bugs

* On the show experience page. If there are no ‘things to know’ this should be hidden and should not be displayed on the screen. 
* Show experience page doesn't display as it should within the Safari browser. 
* Things to know are included if nothing is within that category. It should be hidden. 

## Blockers

When I was working on the add experience form I ran into one of the most difficult problems I have faced in my journey as a junior developer thus far. This issue led me down a path to learning about currying and curry functions. “A curried function is a function that takes multiple arguments one at a time. Given a function with 3 parameters, the curried version will take one argument and return a function that takes the next argument, which returns a function that takes the third argument. The last function returns the result of applying the function to all of its arguments.”

Our backend data structure for the experience model was so deep and nested it was extremely difficult to create a form which allowed a user to input their information. 

After a lot of trial and error, I had to write three separate curry functions which would handle our nested information they were:
* handleInputChanges
* handleDataChanges
* handleThingsToKnowChanges

As a junior developer this is one of the biggests challenges I faced, but I’m glad I persitited with it to finally get it to work in the end.


![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908227/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/handleInputChanges_kaylcm.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908227/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/handleDateChanges_ga8xvb.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641908227/ReadMe%20images/Project%203%20-%20Airbnb%20experiences/handleThingsToKnowChanges_wkbf4n.png)

**This is how our experience data looked :**

``{
   name: 'Yoga with Goats',
   location: 'London',
   locationCoord: {
     latitude: 51.490684,
     longitude: -0.147935
   },
   date: [
     {
       day: 12,
       month: 11,
       year: 2021
     },
     {
       day: 9,
       month: 12,
       year: 2021
     }
   ],
   duration: 90,
   description: 'Take a leisurely walk along a nature path (and meet our friendly critters) to our outdoor yoga studio. Stretch, relax, and center yourself as you prepare to practice yoga while our friendly goats wander around - or even on - you! Soak in the joy of simplicity and happiness that goats can bring! At the end of class, sit peacefully and snuggle one of our adorable baby goats! Other things to note. Please plan to arrive a little early; gates open 15 minutes before class. Please dress for the farm setting and the weather. Campfire will be provided in the colder weather.',
   category: 'Nature and outdoors',
   image: [
     'https://res.cloudinary.com/dulbdr0in/image/upload/v1636473288/Experience-Images/b0c5e4ef-c596-410f-b5d0-3ed4e1acaa52_ya4goc.jpg',
     'https://res.cloudinary.com/dulbdr0in/image/upload/v1636473288/Experience-Images/5b78fd86-b19f-4201-a184-d6c65a3d7e88_jlyagr.jpg',
     'https://res.cloudinary.com/dulbdr0in/image/upload/v1636473288/Experience-Images/facfdb41-fdfb-4495-8524-74413541f06f_gmccdr.jpg',
     'https://res.cloudinary.com/dulbdr0in/image/upload/v1636473288/Experience-Images/07329ec4-421b-4f0c-b1c6-6aab48459870_lvdwlj.jpg',
     'https://res.cloudinary.com/dulbdr0in/image/upload/v1636473288/Experience-Images/c714dbf0-c6c6-4c1c-8fad-77ecf9127247_p4asga.jpg',
     'https://res.cloudinary.com/dulbdr0in/image/upload/v1636473288/Experience-Images/77cfebbf-6d45-4a6b-a76f-dcef72dda0d2_a0e5tk.jpg'
   ],
   attendees: [],
   price: '£28',
   thingsToKnow: [
     {
       header: 'Guest requirements',
       text: [
         'You will need a photo that matches the one on your ID to confirm who is actually going on this experience.',
         'Guests ages 6 and up can attend, up to 10 guests in total.',
         'All participants must wear a protective face covering and practise social distancing.'
       ]
     },
     {
       header: 'What to bring',
       text: [
         'Yoga mat',
         'Water bottle',
         'Love of goats'
       ]
     },
     {
       header: 'Cancellation policy',
       text: [
         'Cancel within 24 hours of purchasing or at least 7 days before the experience'
       ]
     }
   ],
   languages: 'English',
   whatIsIncluded: ['tickets'],
   reviews: [
     {
       text: "What a fabulous experience!",
       rating: 5
     },
     {
       text: "What a fabulous experience!",
       rating: 5
     },
     {
       text: "Once in a lifetime!",
       rating: 5
     },
     {
       text: "Not every day you can say your yoga partner was a goat lol",
       rating: 4
     },
     {
       text: "A very different experience.... Haha",
       rating: 3
     },
     {
       text: "The goats are cute but can be distracting. Having said that what did we expect! Fun nevertheless",
       rating: 3
     },
   ]
 }``


## Wins

* Overall I am very happy with the outcome of this project. It really solidified my knowledge of React. 
* Worked well within our team to get the final product looking very slick. 

## Challenges

* Learning about currying and curried functions.
* I found semantic UI to be extremely challenging to use. 
* I felt really intimidated by the design of Airbnb and trying to create an application that matched their style was challenging. 
* As it was the first time using Git and GitHub within a team, and also using multiple branches this was quite challenging at times. But it was a great way to really build a solid foundation of why it’s used within software development. 

## Future features

* More CSS styling.
* A user could review the event once they have attended.

## Key Learnings

* Learning to read documentation.
* Working well within a group.
* A much better understanding of MongoDB and how a NoSQL database works.
