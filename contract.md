# Contract

## Goals

_At a high level, what do you most want to get out of this project, and why?_

In my time at Mudd, I've spent a lot of time learning hard CS skills, such as algorithms and data structures. However, more subjective qualities of a CS project can be just as impactful on the quality of the final product. By comparison, the Mudd curriculum has done a lot less with this side of the field. With this in mind, I really want to work on polishing the user experience through effective language design. To do this properly, I'll need a good sense for how people interact with my language in each iteration. As a result, in-class and outside interviews and user tests will be very useful for me. 

I also want to gain some experience taking the time to reflect and revise my work once it is functional. I feel that in computer science we're always rushing to some end goal without taking stock of what was accomplished and how it could be improved. And since this class focuses so heavily on language design, taking the time to consider and improve the final product is especially worthwhile. That is why I've scheduled my intermediate goals to have a complete implementation by week 3 (more on that in *Time management*) so I can do additional testing and revisions with the remainder of my time.

## Concepts / skills

_What concepts and / or skills from class would you like to work on, as part of your
project? Are there any concepts / skills that we haven't covered in class that you would
like to work on, as part of your project (for example, other things related to DSLs that
you have come across, or topics from other classes)? Why are you interested in working on
these things?_

As I want to build a syntactically lighweight DSL, my plan is to write it as an external DSL, as an internal DSL would be too limiting and syntactically complex for my vision. With this in mind, I'd like to work on my parsing and interpreting skills, specifically as it pertains to external DSLs. I'm interested in these skills because I see them as applicable across a wide variety of host programming languages, while internal DSL techniques can often be more specialized. 

I'd also like to get some experience designing a DSL in such a way that it could be expanded upon by a capable developer. In the readings for this class we saw different perspectives on how expandable a DSL should be by design. At this point, I've settled on designing my DSL to enable limited future expansion with the addition of new commands (control flow), but not new data structures. Similarly to the language design, I'll have to think carefully about how best to write my backend code with limited modularity in mind. This is a skill I want to develop because these kinds of design decisions come up in lots of CS projects, from hobbyist to professional-grade.

## Time management plan

_How do you plan to set aside time outside of class, to work on the project? Are there
intermediate milestones that you can create, to help you make consistent progress?_

My goal in scheduling work time for this project is to avoid crunch periods before notebook due dates on Sunday and before critique times on Monday. Working up against these deadlines would likely lead to work that is rushed and sub-optimal, and putting forth compromised work for critique is distracting and may make the critiques I receive more superficial instead of getting to the core of things. In addition, being tired from crunching Sunday and Monday may lead to poor critiques that negatively impact others in the class. My Friday afternoons are really open, so I plan to reserve a few hours then specifically to work on my project. This will work well for me because I'll have no imminent deadlines and can just focus on the project. Other times for project work will be found more variably throughout the week, depending on workload and availability.

As for intermediate goals, I'd like to start by getting the backend working in my host language. The top option right now is Python, because it's really flexible and I'm really familiar with it. I'll need to learn how to do parsing in Python, but [there are existing sources](https://www.niklas-semmler.net/dsl,/python/2015/05/13/dsls_in_python.html) for how to do that. If Python doesn't pan out, my next choice will be Scala, as I've already gotten some recent experience using it with this class. I really don't want to get bogged down in the implementation, as the focus of this project is on the language design. As a result, if I don't have a basic implementation working within a week from this Sunday (by 4/2) I will pivot to writing a new interface for the first existing text-based game engine discussed in the *Related Work* section of my project.md file (text-engine). Such a basic implementation includes backend support for a simple set of user commands (GO, LOOK, and TALK) as well as the needed data structures for handling this. If I can get this working, other commands like TAKE and USE shouldn't be too bad. I'd then like to take the next two weeks to implement any remaining implementation elements and develop a completely functional first draft of my external DSL. From there, I'll have the last two weeks to do user testing, refine my work, and add new features as desired.

## Teamwork plan

_If you plan to work with someone else on the project, what is your plan for
collaborating? What part(s) do you think you might do together? What part(s) are you
considering doing separately? How will you hold one another accountable to make regular
progress?_

## Critique plan

_What will you do to make sure that you can give consistent and actionable feedback to
other people in the class?_

First of all, I will always make sure to attend our classes on Monday so I can get that vital in-person time. It's hard to give good feedback if you're not there every time, being able to observe the full track for how their project has been developing. I will also make sure to get hands-on experience working with their language if they will let me. That direct interaction will be useful to me for my critiques and helpful as user testing to the person whose language I am using.

Finally, when it comes to the critiques, I will make sure that my feedback goes beyond surface-level suggestions and reflects thought on my part for how their language could improve. For example, I'd like to be able to offer some suggestions for how a syntactic element of their language could be improved instead of just saying that it's clunky. 



## Success

_At the end of the semester, what would you be proud to show or tell someone about your
project?_

Because my intended audience is people with little to no programming experience, I would be proud to show this project to someone new to programming and have them try and write something in it. My grandmother really likes to write, but she has never programmed before. I would if a language like this could get her into writing small games in her spare time.

I would also be proud to talk about my process for creating my final language design. My plan is for lots of critiques and user tests over the course of this project, so there should be lots of changes to talk about. Finally, my twin brother goes a different college and is pursuing a Game Development minor, so I'd bet he'd get a kick out of this project once it's complete.

## Assessment

_Looking over your responses to the previous questions, what would you consider to be an
"A-" for your project? What would you consider to be an "A"?_

To establish my grading system, I'd like to define some extra stretch goals on top of what I've already outlined: 

* Support for ASCII images on certain triggers (such as entering a space or picking up an object) - would be loaded in similarly to how images are handled in Markdown with parentheses around the file name.
* Adding support for more complex player commands like combining objects and having extended conversations with non-playable characters (asking them about places and objects).
* Exceptional examples in my provided documentation - a good example of this would be implementing a chunk of an actual text-based adventure game from back in the day, I'm partial to [*The Hitchhiker's Guide to the Galaxy*](https://en.wikipedia.org/wiki/The_Hitchhiker%27s_Guide_to_the_Galaxy_(video_game)).
* Exceptional error-catching and debugging approaches - I think that a custom debug mode that can print out all the objects in each room and their relevant interactions would be really cool.

In sticking to the grading system used in this course, an A- or an A should go above the typical standard (what I laid out in my project.md file). I think that an A- would achieve one or two of the stretch goals I've outlined above, while an A would achieve three or more of these.