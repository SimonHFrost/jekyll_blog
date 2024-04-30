---
layout: post
title: "We went to hackmexico!"
image: /assets/hackmexico.png
---
<img class="add-small-padding" alt='Hackmexico Hero Logo' src='/assets/hackmexico/hackmexico.png'/>

I like coding alone, but I also like coding with other people. Even if you’re not working on the same codebase, having everyone aligned towards a goal is great to keep you focused as well as keeping things interesting.

My home office setup in my apartment is great, but sometimes I need to remind myself to get out and explore the city, and interact with locals as well as other expats. When I heard about the hackathon, and after some quick convincing to my co-founder Jakub, we jumped at the chance!

## What the heck is a hackathon?

A hackathon is when you have a fixed amount of time to ‘hack’ or write code towards a specific goal under specific time constraints. No code is allowed to be written beforehand, but in this specific event preparation of UI wireframes and data training AI algorithms could be done ahead of time.

There are all sorts of hackathons: making a video game, using a new technology, or trying to address specific societal problems. hackmexico was the last, and presented three themes to address modern world needs: financial inclusion, social responsibility, and digital empowerment.

![Hackmexico Themes](/assets/hackmexico/themes.png)

## Brainstorming Ideas

I find visualising products easier when a clear user need has been identified. I broke down social responsibility and digital empowerment into smaller problems based on my experience, and afterwards came up with brief solution descriptions.

![Potential Solutions](/assets/hackmexico/solutions.jpg)

One stood out to me the most: better real-time transport updates. Using technology to improve the way you navigate around the city with cheap or free transport gives you more autonomy, and is a form of digital empowerment (theme check! ✅).

## Waze for Ecobici and public transport

![Waze for Ecobici and public transport](/assets/hackmexico/waze.png)

This was the first slide of the pitch to my partner

I’m a huge fan of biking and public transport. It's cheap, better for the environment, and also is used by the majority of the public. I made a quick presentation to pitch to my co-founder to see if I could get him on board.

I liked the catchiness of the concept, which had the following important points:
Quickly recognizable: Waze is an app that is (unfortunately) extremely common in Mexico. It helps drivers navigate Mexico’s crazy traffic with real time updates on events like accidents and roadworks.
Green! Biking isn’t just low cost, but it’s also good for you.
High potential for using AI in some novel, but useful ways: AI is so hyped at the moment, and there seemed to be some obvious use cases for our concept that would get us points with the judges.

## What the heck is Ecobici?

![Ecobici promo image](/assets/hackmexico/ecobici.jpg)

Ecobici is a bike sharing system in Mexico City. It’s extremely affordable at only around 30 USD (545 MXN) per year, and as long as you return the bike to a docking station in less than 45 minutes, it’s completely free. Usage is super simple, scan the QR code with your phone, adjust the seat, and ride. When you’re finished just return the bike back to a dock without having to touch your phone.

Ecobici started in 2010 and has been a huge success. In the month of January 2024, there were 1.5 million rides, and a record 70,000 in a single day on February 13th [Source]. Due to its success, the system was recently expanded in 2022 with hundreds of additional docking stations and bikes.

<img class="add-large-padding" alt='Hackmexico Hero Logo' src='/assets/hackmexico/map.png'/>

This is just a small section of Mexico City, each icon represents a docking station with 20 or more bikes!

If you can’t tell, I love biking and think Ecobici is amazingly executed, from the well engineered mobile app to the design of the bikes and the docking stations. If you plan to visit Mexico City, you can set up with the android and iOS super quickly.

## Ecobici Data

I knew in order to get attention from the judges we would have to incorporate AI into our product. We didn’t have a huge database of user submitted data like Waze, so we had to find an alternative.

It didn’t take long to find that Ecobici has a whole section dedicated to the open data protocol General Bikeshare Feed Specification (GBFS) where you can access data via a live api, as well as download historical data on a month by month basis.

## Station Information and Status (live)

The live API contains station data in the form of static station information as well as dynamic station status. Other routes and properties exist but have been omitted for the sake of simplicity.

Station Information

![Ecobici Data Station Information](/assets/hackmexico/station-information.png)

Station Status

![Ecobici Data Station Status](/assets/hackmexico/station-status.png)

This data is great, but we can’t infer trends over time if we only have a single snapshot in time. Therefore I wrote a small script to save snapshots every hour in Javascript via a Github Actions. It ran for some weeks so that we could infer trends not just based on the time of day, but also the day of the week.

If you want to see this script or access the resulting data for calendar week 14, you can access it on my Github here: https://github.com/SimonHFrost/ecobici-api-poll-and-save.

### Trip Information (historical)

As well as live data, Ecobici provided historical data about trips via a huge .csv file for each month (over a million rows for January!). This data is focused on bikes and trips, rather than stations themselves. Below is an example of the first 10 rows from January 2024.

![Ecobici Trip Information](/assets/hackmexico/trip-information.png)

We now have data! We weren’t sure what features we wanted to make with our app, but we were confident we could create something interesting with the data we now had. We were ready for the hackathon! Or so we thought…

## A wheely sticky situation…

<img class="add-large-padding" alt='Hackmexico Hero Logo' src='/assets/hackmexico/sticky.png'/>

A week before the event. We were notified that each theme now had additional requirements. The one we selected, now specified:

Digital Empowerment: Mexico has a rich cultural heritage and booming tourism sector. Create a digital platform that promotes accessible tourism in Mexico to ensure inclusive travel experiences.

Despite reading the hackathon format documents ahead of time, this change to the theme was significantly different to what we planned. We tried to pivot our Ecobici preparation but it didn’t seem to fit any of the themes well. We were pretty disappointed because we had become attached to our Ecobici idea.

## Dorado Dumpster (Golden Dumpster)

Ultimately, we decided the main thing we could salvage through pivoting was to reuse the technology preparation we had done with OpenStreetMap, Vite, and React. We decided to go for the new theme Social Responsibility : Mexico grapples with the dual challenge of food wastage and food scarcity.

<img class="add-large-padding" alt='Hackmexico Hero Logo' src='/assets/hackmexico/dorado-dumpster.png'/>

Dorado Dumpster is a dumpster diving app where you can track and share locations where perfectly good groceries have been thrown away that can still be used. It was silly and simple enough that we thought we could ‘hack’ out in short notice.

While it was quite different from what we originally planned, we still managed to hack together a basic Minimum Viable Product (MVP), learned some new tech, and learned how to work better with each other.

## Conclusion

Sourcing and normalising data sources is a practice that will become more common as the world becomes consumed by Artificial Intelligence. I was pleasantly surprised to see platforms I love like Ecobici openly publish their data. Going through the exercise of preparing and cleaning up practical data and seeing how it could apply to our project was an informative experience.

![Team Mosmos](/assets/hackmexico/team-mosmos.jpg)

Despite not being able to work on the idea we originally planned. Getting our hands dirty rapid prototyping from start to finish, alongside other motivated and smart coders was a memorable experience.

Thanks to AngelHack for having us!
