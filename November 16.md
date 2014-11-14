# Design notebook for week ending November 16, 2014

## Description

One of the first things I realized I needed to do was give specifics as to how the user will interact with the language, so I made my design idea more concrete on a blackboard, then in the design and implementation document.

Worked more on project, added some of the classes for the data structures. Doing so I realized I need to understand SpriteKit a bit more as I don't fully understand how I will be implementing this. I looked at the Pigs SpriteKit tutorial, which gave me a better understanding. I then wanted to make it to the user can make the images as I figured that would be a good start (be able to define images with some simple animations and say "Done!"). I watched the "Drawing with Swift in Playgrounds" tutorial, which while somewhat helpful, was also for OSX so it doesn't directly translate. Even so, most of the objects are pretty similar. It wasn't directly applicable to what I currently need, and watching it made me realize again (which I had thought earlier) that I should not focus on the drawing portion yet, and just assumed a define image to animate and do the drawing part secondary.


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

2 hours on critique (spent a fair bit of time looking up existing tools)

1.25 hours on design sketches on blackboard and critique feedback

1 hour on writing up design changes and implementation, and thinking more about the decisions.

1.5 hour looking more into how I would implement architecture in Swift project and looking at tutorials and playing around in Playground

## Post-critique summary

Overall, I am making good progress and it was good to be familiar with the tools and how Swift works. Professor Ben made a good point to use the tool that will most fit my IR for choosing between CoreAnimation and SpriteKit. Especially because my language is not text based, I need to make sure that I am very careful and specific in describing what my language will actually look like, and what is to be expected for a user to use the DSL. I should have an outline of how the interactions and interface will look, and really go into more detail on how that will occur. 

I have outlined the overall process, but I need to detail the specific things that occur at each step in the process. The high level design of my DSL makes sense, but these smaller details are what I need to focus on to really flesh out the DSL and allow me to implement it.

## Post-critique reflection

I definitely agree with everything Mauricio has mentioned, as I myself have not really fleshed out the details (I kinda thought about each thing disjointedly, but not how everything ought to work together). I have also decided to go with SpriteKit for now as I think that really does work better as a close representation to the IR, although that decision may change as I really dive into the implementation.

As a response to the critique, I have actually wrote out exactly what the interface will look like, and how the user can create something within this DSL. This will be a part of my stuff this week! Thank you Mauricio!
