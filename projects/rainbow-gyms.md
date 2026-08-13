---
layout: project
type: project
image: img/vacay/vacay-square.png
title: "Rainbow Gyms"
date: 2026
published: false
labels:
  - TypeScript
  - Nextjs
  - NextAuth.js
  - React Bootstrap
  - PostgreSQL
  - GitHub
  - Prisma
  - Vercel
summary: "A responsive web application for UH Manoa students that some of my classmates and I developed for ICS 314."
---

<img class="img-fluid" src="../img/vacay/vacay-home-page.png">

Rainbow Gyms is a responsive web application designed to allow UH Manoa students to create and participate in scheduled workout sessions that I helped create as a team project in ICS 314, Summer 2026. The main goal of Rainbow Gyms is to give students more opportunities to stay healthy and connected by making it easy to find workouts and interact with other students.

The main feature of the web app are:
  - Browse and filter session based on `workout type`, `gym location`, `min. open spots`, and `date`
  - Create sessions
  - View and delete created sessions and view joined sessions
  - View more info about a session (participants, description)
  - View other participants' profiles
  - View calendar with sessions appearing on scheduled days

We used Issue Drive Project Management via the GitHub Issues tab, and created issues within three different projects&mdash;Milestone 1, 2, and 3.
Each Milestone had different requirements to be fulfilled. For example, M2 required at least one page to read from, and one to write into the PostgreSQL database. We created issues and divided up the work for each milestone accordingly.

My contributions to the project include the following: 
  - The creation of the initial mockups pages for the website including a very simple mockup profile card which read from our PostgreSQL database via Prisma functions
  - Assisted in creating the Milestone 1 documentation for our [projects's home page](https://rainbow-gyms.github.io/)
  - Implementation of a consistent style throughout all pages of our web application
  - Mobile scaling and responsiveness
  - Addition of a delete button that uses Prisma functions to remove a user's session from the PostgreSQL database
  - Additional various style features such as adding an underline to the Navbar link matching the page the user is currently visiting

The project helped me learn how to design and implement a responsive web site using ReactBootstrap, HTML, CSS, and Prisma.

Vacay is implemented using [Meteor](http://meteor.com), a JavaScript application platform. Within two weeks, we created a website that implements several types of reservations including flights, hotels, and car rentals.

In this project I gained experience with full-stack web application design and associated technologies, including [PostgreSQL](https://www.postgresql.org/) for database storage, the [React Bootstrap](http://getbootstrap.com/) Front-End Framework for the user interface, and TypeScript for both client and server-side programming. 

Here is some example code to illustrate Simple Schema use:

{% gist 9defa1fb3f4eb593ba5fa9eacedca960 %}
 
Source: <a href="https://github.com/theVacay/vacay">theVacay/vacay</a>
