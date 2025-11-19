---
layout: post
title: "Disco Tray Week 10 Post"
categories: Disco Tray
author: Colten Berry
---

<p>This week I finished a few other issues that were brought up in our testing. Logging out returns the user to the list screen instead of the login screen. This makes sense with our new anonymous feature. Also, editing a blurb looked terrible because I forgot to include padding when I made the textfield outlines visible so I added padding.</p>
<p>Most of my effort this week went into trying to prevent a historical site from reloading when a user left a review. Because I know have a selector listening for changes in appstate.historicalsites, any changes to any historical site triggers the list to rebuild. This is not ideal, but with the smaller images hopefully the user will not notice it as much. I tried to alter this so that only the single site would rebuild and all the other sites would remain the same, but I was not getting the results I wanted with that. After banging my head against a wall for most of the week, I decided to just add in an ID field to the ListItem and had each historical site object generate a Uuid as its ID. If I am understanding the documentation correctly, this will allow flutter to reuse the old widget instead of completely rebuilding it if the historical site object is the same. Hopefully, this means it won't try to get new images from the firestore. But the images were already getting stored in the historical site object so you wouldn't expect that to be a problem anyway but it was. Maybe the futurebuilder was the one causing unnecessary loading now that I think about it. Since it was running GetImage as its future field. I will fix that during our meeting today</p>
