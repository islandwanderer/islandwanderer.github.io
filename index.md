<h1>Table of Contents</h1>
<h4><a href="#overview">Overview</a></h4>
<h4><a href="#userguide">User Guide</a></h4>
<ul>
 <li><a href="#landing">Landing Page</a></li>
 <li><a href="#profile">Profile Page</a></li>
 <li><a href="#home">Home Page</a></li>
  <li><a href="#createEvent">Create Event Page</a></li>
 <li><a href="#calendar">Calendar Page</a></li>
 <li><a href="#message">Message Page</a></li>
</ul>
<h4><a href="#developerguide">Development</a></h4>
<ul>
 <li><a href="#history">Development History</a></li>
 <ul>
  <li><a href="#m1">Milestone 1</a></li>
  <li><a href="#m2">Milestone 2</a></li>
 </ul>
 <li><a href="#guide">Developer Guide</a></li>
</ul>
<h4><a href="#feedback">Community Feedback</a></h4>

<h2 id="overview">Overview</h2>
<p><a href="https://github.com/islandwanderer/islandwanderer">Island Wanderer</a> is the perfect website for University of Hawaii students who want to explore the islands of Hawaii with other students. The Hawaiian Islands have a lot to offer, from hiking to snorkeling to luaus to relaxing at the beach. However, sometimes it can be hard to organize a group of people to go explore these places. Island Wanderer is here to solve this problem. Students can form groups to go on adventures together, creating countless unforgettable memories while meeting new people along the way.</p>
 
<p>The developers of this website are current University of Hawaii students who are passionate about exploring the Hawaiian Islands and love to connect with people through adventuring. If you have any comments or questions, you can contact the developers through creating an issue on the GitHub site.</p>

<h2 id="userguide">User Guide</h2>

<p>Students are able to log into the website and are immediately taken to the home page, which shows postings from other students, starting with the most recent posting. Users can then filter the postings by tags - locations, dates, people, etc. Students will have the option to save posts, message the poster, or post something themselves. They can also comment on a post. Students will also have access to a personal calendar, which will hold all the events the student wants to attend. Two ways to add events to the calendar is through manually entering an event, or directly addiing an event from a post. Furthermore, students can start private messages with other students, should they have any specific questions about a post or activity. Because students don't have to "friend" other students to see their posts/directly message them, there will be the option to block certain students, should there be any issues. </p>





<h4 id="landing">Landing Page</h4>
The <a href="http://islandwanderer.meteorapp.com/">landing page</a> of the website has a small bit of information about the website and allows UH students to log in.<br>

![landing page](https://user-images.githubusercontent.com/31399883/33113157-fedcc01a-cefa-11e7-992c-01a8a5570fc8.png)<br>


<h4 id="profile">Profile Page</h4>

![profile_page](/images/profile.png)<br>

Students are then taken to their <a href="http://islandwanderer.meteorapp.com/nmeinzen/profile">profile page</a> where they can enter their information. Students must enter their name and their email address. They can add other contact info such as facebook, slack, twitter, etc. to their account if they would like.


<h4 id="home">Home Page</h4>
Next students can go to their <a href="http://islandwanderer.meteorapp.com/nmeinzen/home">home page</a>, which will show all new posts/events created, and if they are interetsed, they can join an event, or add a new event. 

![user_homepage](https://user-images.githubusercontent.com/31559898/33109275-c485dd9a-cee4-11e7-84f5-e752a1cb7797.png)


<h4 id="createEvent">Create Event Page</h4>


<h4 id="calendar">Calendar Page</h4>

![calendar page](./images/calendar.png)<br>

Students can also check their personal calendar. If the student is signed chooses to attend an event, it will show up on their calendar.


<h4 id="message">Message Page</h4>

![message_page](./images/message.png)<br>

Students can then check theirmessages, which will show all messages from groups they are apart of.


<h2 id="developerguide">Development</h2>
<h4 id="history">Development History</h4>
<h5 id="m1">Milestone 1</h5>
<h5 id="m2">Milestone 2</h5>
<h4 id="guide">Developer Guide</h4>


The website was then deployed to <a href="https://galaxy.meteor.com/app/islandwanderer.meteorapp.com">galaxy</a>.</p>
><a href="https://github.com/islandwanderer/islandwanderer/projects/2">Milestone 2</a> 

<h2 id="feedback">Community Feedback</h2>



![profile_page](/images/profile.png)<br>

Profile page is similar to bowfolio app. The only difference is email of the newly signed up user is auto-populated. 

![message_page](./images/message.png)<br>

Message is a simple chat app where a user can choose any of the event they are subscribed to and enter the message board for the event. The event selection field is set a a reactiveDict. As any modern chat app, users message is aligned to the right and everyone else message is aligned to the left. The app further distinguishes different users with different background color on their message. A simple hash of username has been used to classify users into 7 different colors. Base collection has additional method called filter() which does filters message documents by events. As expected from any chat app, upon submition of message, messages field clears but event field does not. Clearing message was straight-forward task. However, reactive flag had to be set to the selected event after each message is entered.

Future enhancement could include a sophisticated hash function that minimizes collision. Other enhancements could count number of unread messages on each of the event user is subscribed to.

![calendar page](./images/calendar.png)<br>

Calendar is built on fullcalendar package. Calendar page also required sub-tempate to render as expected. The event collection of the app did not meet the requirement of events constructor of the package. A function to convert relevant documents from event collection into an array of objects enabled fullcalendar events constructor to display events in the calendar. 

Future enhancements could include routing event creator to event message page when the event is clicked on the calendar. Other enhancements to the calendar page could be routing to create event page when user clicks on the calendar space with no events.




