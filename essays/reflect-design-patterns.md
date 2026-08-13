---
layout: essay
type: essay
title: "My Crash Course to Understanding Design Patterns"
# All dates must be YYYY-MM-DD format!
date: 2026-07-30
published: true
labels:
  - Design Patterns
  - Reflection
---
<img width="200px" class="rounded float-start pe-4" src="../img/design-patterns.png">

## You Can Just Copy-And-Paste, Right?
As a whole, the idea of Software Engineering is still quite new to me. ICS 314 is my first experience with anything of the sort. Therefore, my understanding of design patterns is quite limited as well, much more so than other topics covered in the class so far. However, if there is one thing I am sure of, it is that design patterns are not something you just copy and paste into your code. It does not have a strict or precise format, but is instead more of an idea that can be executed in many ways to solve a problem.

## Plumbing Up With Analogies For Design Patterns
Now, if you are anything like me, then this will be a difficult concept to grasp, so perhaps it is better to think about it like plumbing for a house...

Suppose that you want flowing water to all your plumbing fixtures (sink, toilet, shower/bath, etc.). There is not just one set way to establish pipe lines to each fixture; lots of houses have different structures, interiors, and so on. Your local hardware store does not sell pre-built "one size fits all" pipe layouts, because they do not exist. More generally, a single-story house will more than likely not have the same pipe pattern as a two story house, or a three story apartment. And yet despite the differences in layout, the fundamental architectural challenges, and the best practices used to solve them remain the same.

The foremost problem of plumbing is even getting water to the fixtures. If you had an individual pipe for every fixture, you would be left with a tangled-up and heavily strained piping system. The best practice plumbers use in this case is a standardized structural pattern in which they establish a single, central main intake line. The idea remains the same, but the execution may be different depending on various factors such as location.

Another major problem in plumbing is water condition and pressure. Water coming straight from the main utility pipe is under extreme pressure and usually  contains harmful sediment or minerals. The best practice in this situation is to install a pressure regulator and water filter after the main utility pipe.

## From Plumbing to Programming
In terms of a central, main water supply entryway, it is an example of the Singleton Pattern. My team and I use a single Prisma connection to our database. Creating a connection for each page that needs to access some part of the database would eventually make too many for it to handle. Using Prisma, no matter how many pages or components request data, they all route through that exact same central instance, just like every faucet in a house drawing from one main intake pipe.

Meanwhile, the pressure regulator and water filter is a real-world example of the Data Mapper Pattern. In our database, we have raw "unfiltered" PostgreSQL data. Passing that data directly into frontend React components would cause many errors. Prisma acts as our Data Mapper: it sits between our raw database and our UI, translating raw database records into clean, safe, and usable TypeScript objects.

## Final Thoughts
Design patterns are nothing like UI frameworks despite initially thinking so. Design patterns are a lot more flexible, and I see that it is used for backend development such as databases, connections, etc. and not so much for the frontend compared to UI components.

*Use of Google Gemini 3.6 Flash Extended to create analogy*
