# Project proposal

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Text-based adventure games live and die by the quality of their writing. This means that great writers have the ability to craft great games in this space. However, such games also require control flow and state management under the hood so they can function properly. Whether coding it up from scratch or using an existing, heavier implementation, this can be a lot of work for a writer, who likely has little, if any experience in programming. My idea is to make this medium more attractive and accessible via a lightweight DSL so that writers can focus on writing and not tedious programming tasks! 

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate here because of the super-focused domain. Compared to other video games, text-based adventure games are pretty simple, with a fixed number of actions that the player can take along with a series of rooms that the player can navigate through. This limited scope makes a DSL practical here. It's also appropriate because my intended audience of writers does not have any existing programming experience, and a DSL would give me enough room to design with this in mind.

### Why you?

_What excites you about this idea? How did you come up with it?_

I've loved choose-your-own-adventure books and text-based adventure games since I was a kid. As a project, it would give me a better appreciation for the medium while working on the skills we've covered so far in this course. I thought of it while considering the kinds of project that wouldn't be too implementation-heavy while giving lots of leeway on the language design. I was thinking about everything that can be accomplished within a terminal window, and I was reminded of these kinds of games.  

### Domain

_Describe the project's domain in five words._

Developing simple text-based adventure games!

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The overall philosophy with my design is to make it as lightweight as possible, so writers can focus on writing and not on juggling syntax. My plan is to take influence from Markdown and XML to make something that is not terribly intrusive yet powerful enough for the features I wish to implement (room, interaction, and inventory system on the backend along with related GO, LOOK, TALK, TAKE, USE, and INVENTORY commands for the player to use in the terminal). Tags and nesting from XML will allow for rooms to be established with different objects, people, and items within them, while certain symbols and parentheses around tags (like in Markdown) can define relationships between rooms and between objects. This is the right way to work in this domain because it implies the necessary relationships between all the things in the game while removing all the logic that would otherwise be necessary to implement yourself.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, the game as programmed will start on the command line. This will involve printing things to the terminal and waiting for user input, where the process repeats. Some common errors will likely be improperly closed tags, bad nesting, and relationship references to tags that do not exist. My DSL will need good error-catching to be able to diagnose these problems and return clear and relevant error messages to the user in the terminal. I'll need to describe the problem in clear terms and give a relevant suggestion for how to fix it! 

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to link rooms together, declare objects within them, and establish important relationships between these things (one room being to the north of another, a key opening a chest, and so on). It should be possible but difficult to rebind certain actions within the engine to different keywords. This could be useful depending on the theme of your game (ex. a game with a blind protagonist could rebind LOOK to TOUCH). It should be very difficult to add in new actions for the user. My intention for this engine is to support the vast majority of actions in existing text-based adventure games, and if you want more than that then a more complex and flexible DSL would be a better fit for your project!

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are quite a few DSLs within this domain. One example that I found is called [text-engine](https://github.com/okaybenji/text-engine). It is a text-based adventure game engine written as an internal DSL in JavaScript. I like a lot of the possible commands that a user can input into valid games - things like LOOK, TAKE, GO and TALK will be good to implement for my project. However, some things would be too much for me to implement (saving and loading the current game are two good examples). I also think that having to write JavaScript would be too complicated for my intended audience.   

One other example I found is called [Twine](https://twinery.org/reference/en/index.html). The source [found here](https://www-users.york.ac.uk/~tas509/TwineExampleProject/ExampleTwineProject.html) was especially helpful for learning more about it. This is a tool that allows for easy creation of text-based games and other forms of non-linear storytelling. Twine is interesting because it is predominately graphical, letting you place story blocks and connect them to form branching narratives. It also has support for variables, arrays and conditional logic within these blocks (along with selectable lists of options, images, sounds, and videos) so you can definitely implement a text-based adventure game with it. It takes a lot of inspiration from Markdown for its syntax. One issue with this language is that it requires you to manually manage objects in arrays, which is something I want to avoid having the user themselves. It also doesn't run in a terminal, which it loses some of the original magic of the medium.

Based on these two examples, there is definitely demand for simple tools to create these kinds of games! And Twine will definitely be worth considering in more detail as I develop my project.

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

My goal is to spend 20% of my time on systems and the other 80% of the time on language design. I think that this split allows me to pursue both areas while emphasizing the latter (as this is a programming languages class, after all).

### Scope

_How big an idea is this? How ambitious is this project?_

I think that this idea is reasonably sized, as it will provide some interesting implementation challenges while keeping the project focused on language design. I also think that this domain is well-suited for scaling the scope of the project up or down depending on unexpected successes or roadblocks. For example, if things are going swimmingly, I can tackle some of the extended goals outlined in the *Grading* section of my contract. On the other hand, if things go awry on the implementation I will switch to interfacing with an existing text-based game project (as also discussed in my contract).

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This project would be a good idea because it is well-sized, having reasonable implementation requirements and lots of leeway with designing the language. I also think it's a fun domain that would really benefit from such a language existing. 

This project might not be such a good idea because there are plenty of other existing DSLs that try to do the same things. However, based on my research I think I could deliver something new within this space.