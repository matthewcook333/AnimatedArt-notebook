# Design notebook for week ending November 16, 2014

## Description

One of the first things I realized I needed to do was give specifics as to how the user will interact with the language, so I made my design idea more concrete on a blackboard, then in the design and implementation document.

Worked more on project, added some of the classes for the data structures. Doing so I realized I need to understand SpriteKit a bit more as I don't fully understand how I will be implementing this. I looked at the Pigs SpriteKit tutorial, which gave me a better understanding. I then wanted to make it to the user can make the images as I figured that would be a good start (be able to define images with some simple animations and say "Done!"). I watched the "Drawing with Swift in Playgrounds" tutorial, which while somewhat helpful, was also for OSX so it doesn't directly translate. Even so, most of the objects are pretty similar. It wasn't directly applicable to what I currently need, and watching it made me realize again (which I had thought earlier) that I should not focus on the drawing portion yet, and just assumed a define image to animate and do the drawing part secondary.

Finished the design and implementation document. I added some sketches that I did in class to the github as I felt that would be better than spending the time to draw sketches on the computer. The link to them is [here](https://github.com/matthewcook333/AnimatedArt/tree/master/design). I will also add the more relevant pictures below:

Sketch of the interface: 
![alt text](https://github.com/matthewcook333/AnimatedArt/blob/master/design/interface.jpg "Interface")

In the interface, you can see that above I have the idea of allowing the user to change previously made images/animations, although currently I do not plan on implementing that for my first iteration (unless I find it to be natural to add quickly). The drawing tools I plan to have a simple version of with multiple colors/thicknesses, which obviously that can be enhanced to allow for more sophisticated drawings.

Sketch of the drop down menus for animations: 
![alt text](https://github.com/matthewcook333/AnimatedArt/blob/master/design/animationdetails.jpg "Details")

Sketch of the steps of interactions, including description of commands:
![alt text](https://github.com/matthewcook333/AnimatedArt/blob/master/design/interactionsteps.jpg "Steps")

Worked a good bit more on the code itself. Going through it, I realized it makes much more sense to simply use Core Animation vs. SpriteKit (my documents might not reflect this as I did not have enough time to go back to the documents as I coded this close to this week's deadline. This will be reflected in later documents). I can use UIImageView in the same way as SKSpriteNode, and have the same capabilities of whether things are animation, and specifics of each animation. There is also more extensibility from a UIImageView vs SKSpriteNode. The downside is that SKSpriteNode has more built-in things like physics, collisions, textures (for 3D effects and such), etc. All of which I am not currently planning on using, nor plan to be a part of this DSL.


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I would say the biggest issue right now moving forward will be how to implement this. I have a general idea of how the animations work in SpriteKit, and have it where I can have the user click a button to rotate, as well as draw a path (though still not moving along the path), so I will have to do a lot more implementation work. Design-wise, I would say overall I am content with what I have, though I would be happy to hear suggestions/criticisms/concerns for what I have in mind!

**What questions do you have for your critique partners? How can they best help
you?**

Do the current set of animations/commands seem interesting enough to you? Is there something you see missing that you would love to have if you were making your own creation? If you have experience in iOS development, do you have particular suggestions for design choices/things to use for my project?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

2 hours on critique (spent a fair bit of time looking up existing tools)

1.25 hours on design sketches on blackboard and critique feedback

1 hour on writing up design changes and implementation, and thinking more about the decisions.

1.5 hour looking more into how I would implement architecture in Swift project and looking at tutorials and playing around in Playground

1.75 hours finishing up design and implementation document, organizing pictures, and talking to my brother about design choices and overall architecture.

1.5 hour on coding project, lots of figuring out how to have architecture implemented in code and Swift/iOS specific things (like init, storyboard stuff, etc.)

## Post-critique summary

Overall, I am making good progress and it was good to be familiar with the tools and how Swift works. Professor Ben made a good point to use the tool that will most fit my IR for choosing between CoreAnimation and SpriteKit. Especially because my language is not text based, I need to make sure that I am very careful and specific in describing what my language will actually look like, and what is to be expected for a user to use the DSL. I should have an outline of how the interactions and interface will look, and really go into more detail on how that will occur. 

I have outlined the overall process, but I need to detail the specific things that occur at each step in the process. The high level design of my DSL makes sense, but these smaller details are what I need to focus on to really flesh out the DSL and allow me to implement it.

## Post-critique reflection

I definitely agree with everything Mauricio has mentioned, as I myself have not really fleshed out the details (I kinda thought about each thing disjointedly, but not how everything ought to work together). I have also decided to go with SpriteKit for now as I think that really does work better as a close representation to the IR, although that decision may change as I really dive into the implementation.

As a response to the critique, I have actually wrote out exactly what the interface will look like, and how the user can create something within this DSL. This will be a part of my stuff this week! Thank you Mauricio!
