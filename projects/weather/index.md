---
layout: default
title: Weather Database
---

<div class="container text-center">
  <h1>Weather Database</h1>
  <h2>A Continuing Project</h2>
</div>
<div class="container text-left">
  <h3>The Beginning</h3>
  <p>My dad is a weather geek. He started recording the weather back in the mid 1980s by hand, cataloging temperature, humidity, barometric pressure, wind speed and direction, and precipitation. Several years ago, I decided to save a few trees and convert his hand-written entries to an application where he could continue to add entries and easily look back on the data he had entered for amateur forecasting.</p>
  <h3>Inputting the Data</h3>
  <p>But where to start? My initial iteration was to manually enter all of his data (about nine thousand entries) into an Excel spreadsheet. It was a tedious and agonizing effort, but in a few days I had manually entered all of his data into an easy-to-read format to which he could add at his leisure.</p>
  <h3>Version 1</h3>
  <p>Within a few weeks, I realized that it would be handier to simply have an input form and a database backend that he could filter and organize how he saw fit. I put together a simple webserver and SQL database and began working on a basic webpage that would submit new entries and show the previous data on a separate page.</p>
  <p>The first version of this web app was not very pretty. It was a mostly-empty page with ugly rectangular input boxes and blocky grey buttons. The only styling came from minor HTML tweaks to center the input boxes and submission button. Upon clicking submit, the page would redirect temporarily to tell the user if there were any errors or if the submission had been successfully added to the database. It would then redirect to yet another anemic page with a featureless spreadsheet of all previous entries in descending order.</p>
  <p>Load times were fast, but this was clearly a long way from being a full-featured in-house application. My next step would be to add a bit of styling to the pages. I dug through mountains of documentation on different styling methods and stylesheets, trying to find one that would be both appealing and easy to implement for years to come. I eventually settled on Bootstrap 3, which began my love affair with the framework that still burns strongly today.</p>
  <h3>Version 2</h3>
  <p>Now for the fun part. I wanted this to be completely offline, so I had to essentially host my own CDN for Bootstrap to work flawlessly. After much frustration, I finally managed to get Bootstrap self-hosted, and began the work of editing my pages to implement the styles. Within a few days, the blank, featureless pages had become somewhat more appealing. I added a navy blue navbar at the top with links to the database and submission pages. I re-worked all of the input boxes to be evenly spaced and centered, and replaced the grey blocky buttons round-cornered, partially animated ones. At last, this was beginning to look like a professional effort.</p>
  <h4>Building a CRUD</h4>
  <p>Now, I needed a way to make the data easy to navigate, easy to edit, and fast-loading. That's when CodeIgniter came in.</p>
  <h2>UNDER CONSTRUCTION</h2>
  <p>Please stay tuned as I continue to update with page with more information, screenshots of my work, and hopefully a demonstration in the near future.</p>

</div>
