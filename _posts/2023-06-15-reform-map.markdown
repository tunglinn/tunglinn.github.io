---
layout: default
modal-id: 0
date: 2023-06-15
img: parking-reform-map.jpg
alt: image-alt
project-date: June 2023
type: main
client: Parking Reform Network
category: Web Development
description: From rookie to savvy, I worked on a full-stack map migration project.
---
**[The Project][reform-map]** 

A map migration from Shiny(R) to JavaScript. Here's a comprehensive list of everything I learned:
- JavaScript, HTML, CSS
- GitHub
- CI/CD
- WebDev pipeline/infrastructure
- Testing

This was planned to be about a six month migration, with me as the main contributor and Eric as my supervisor. I spent 5-15 hours a week on the project, while I worked part-time as an EMT and moved from Los Angeles back to my home town near San Francisco. 

**The Details.**
Like I mentioned, I did not know much about web development. We needed this migration done because the Shiny server costs $40/month, in which we don't take advantage of most of the computing power and features of it. Also, efforts to revamp the map fell short due to the restraints with Shiny/R. Overall, we had a deadline before the Shiny server would shutdown.

The first piece I set up is a blank page instead of the Shiny app. We used Parcel to run the local development server and eventually bundle and build the `/dist` file for staging and production.

Next up is the actual map, in which we opted for LeafletJS. I worked with HTML and CSS to structure the site to resemble the Shiny app as closely as possible. Creating button icons and popups helped me get familiar with GitHub, CI/CD, and testing standards. 

After wading in the swamps of HTML and CSS, I returned to the map by finally loading in our data (compiled by our volunteers!). Our data includes fields like city name, coordinates, and type of reform. I started with just the coordinates and created a CircleMarker for each entry.

To use the rest of our data, we have popup details when users click on a CircleMarker. I had already successfully made a popup, so this ticket was smooth-sailing.

Now, it's time for the filters, which includes multi-select inputs, a population slider, a toggle, and a search bar. We decided on checkboxes for multi-select options. Since we wanted to keep the project small and clean, we did not use libraries like Bootstrap or React. Instead, I found ways to create a double-headed slider and toggle through basic HTML elements. Eric implemented the search bar, using Choice.js.

One month before we expected the Shiny server to shutdown, ___ sent a notice of an early shutdown. Thankfully, the most important components have already been migrated, so it was just a matter of fixing some bugs and pushing the staging site to production!

Once the migration was complete, we turned back to the design changes we wanted to do, but couldn't with the Shiny app. 

There were two problems with the old map. 

1) You are immedietely hit with thousands of data points.

2) The core cities that removed parking minimums were not explicitly obvious.

However, both views have their advantages. Lots of data shows that parking reform is happening more and more, while showing the core cities is much cleaner and easier to digest.

To address both of these problems, we decided to change the view to filter for just core cities, but include a counter on the page. Therefore, the counter would indicate that there are thousands more cities with some type of parking reform.

**Takeaways.** While I learned so many technical aspects of web development, UX, and data visualization, my biggest takeaway is how to truly understand the process, which required me to develop the skill of self-learning effectively. It's also about the habits I build, like writing documentation, industry standard programming, and acheiving broader understanding.

**What is parking reform?**

Parking is mundane, inevitable, and rage-inducing. However, to many communities, it is a vehicle for change in affordable housing, climate change, and safer streets. 

One of the most common ways cities and states have changed their parking codes is by removing them all together. Across the United States and the world, there are parking minimums required for new and/or re-use developments. While some safety codes and building codes are often written in blood, parking code cannot claim the same. Resources that were used to develop parking codes have poor data and is based on peak hours, which leaves many parking lots empty most of the time. Additionally, there is the argument of letting supply, demand, and the free market to dictate how many parking spaces a developer allocates. 

The Parking Reform Network is a dedicated, advocacy organization for parking reform. Amongst its tools, resources, and advocacy, is a parking reform map, which tracks parking reform across the country (and eventually around the world, too).

[reform-map]: https://parkingreform.org/mandates-map
