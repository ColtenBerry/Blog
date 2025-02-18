---
layout: post
title: "Disco Tray Week 3 Post"
categories: Disco Tray
author: Colten Berry
---

<p>It has been a couple of weeks since I last updated, I will try to be better in the future about keeping my blog updated. This past week, I mainly put finishing touches on the Faulkner Footsteps project. I overhauled how images are loaded. I previously had them stored in a Google Drive folder and had their urls on Firestore, however loading these images took an extremely long time. I changed this so that the images were stored as strings and were then converted to images within flutter. Images now load almost immediately. While I am pleased with how quickly they load, the strings are very long and I imagine that if there are too many images, then Firestore may have problems pulling all of them. In that case, we can revert to the Google Drive folder method. Additionally, if there is an error loading an image, then the basic Faulkner Footsteps thumbnail will display instead. This helps safeguard the app from looking incredibly ugly if an error occurs<p>
<p> Another thing I did this week was changing the achievements page so that it generates achievements based on the historical sites within the Firebase. Previously this achievement list was hardcoded into the achievements page, so this allows sites to be added easier. I also tested adding a new historical site to ensure that everything works properly and it does.</p>
<p>I also changed the way that user reviews work. Instead of clicking on a button that allows you to review it, the star review widget is directly on the site and it is colored to match how the user rated the site. Directly after the widget is a text widget that displays the average score of the site. I think that this UI change gives the user much more information in a much more concise way. </p>
<p>I think that this project is starting to wrap up. I feel like we have addressed all of the major issues the previous group left us. I know my partners are still working on some of their issues and I have offered my help if they need it. </p>


