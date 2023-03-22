# Project proposal

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

Text-based adventure games are defined by the quality of their writing. However, such games also require control flow and state management under the hood so they can function right. Whether coding it up from scratch or using an existing, heavier implementation, this can be a lot of work for a writer, who likely has little, if any experience in programming. Make this medium more accessible so that writers can focus on writing, not on control flow and managing state!

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate here because of the super-focused domain. Text-based adventure games are usually pretty simple with a fixed number of actions that the player can take. 

### Why you?

_What excites you about this idea? How did you come up with it?_

The implementation wouldn't be too bad and I'd have a lot of leeway with shaping my syntax. 

### Domain

_Describe the project's domain in five words._

Engine for text-based adventure games

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The overall philosophy with my design is to make it as lightweight as possible, so writers can focus on writing and not on juggling syntax. This is the right way to work in this domain 

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, the game as programmed will start on the command line. Some common errors will likely be improperly closed tags and bad nesting. 

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to link rooms together, declare objects within them It should be possible but difficult to rebind certain actions within the engine to different keywords. This could be useful depending on the theme of your game (ex. ). It should be very difficult to add in new actions for the user. My intention for this engine is to support the vast majority of actions in existing text-based adventure games, and if you want more than that then another more complex and flexible DSLs would be a better fit for your project!

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are quite a few DSLs within this domain. 

Because of this, there is a for a simpler language. 

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

My goal is to spend 20% of my time on systems and the other 80% of the time on language. 

### Scope

_How big an idea is this? How ambitious is this project?_

I also think that this domain is well-suited for scaling the scope of the engine up or down depending on roadblocks. 

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This project would be a good idea. I also think it's a fun domain that would really benefit from such a language existing. 

This project might not be such a good idea because there are plenty of other existing DSLs that try to do the same things. However, based on my research I think I could deliver something new within this space.