# Design notebook for week ending November 9, 2014

## Description

Started the week with thinking more about how I want to interface with the language, as well as looking deeply into how Swift/iOS does animation, as that would give me more ideas how I want to make the IR for the animations in order to make the implementing semantics easier. I so far have looked into ways of rotation, where I can essentially give my objects a certain number of degrees to rotate (start and end) and it will simply do so. Looking into doing translation/path, I learned how to drag an object around, as well as create (draw) lines. I will need to look into how to really put those two together, and allow the image to travel along the drawn path.


**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

1 hour on critique

0.5 hour on critique feedback, summary, and reflection

2.5 hours looking into Swift, SpriteKit, Animation framework in Swift, drawing tutorials, animation tutorials

0.5 hour on writing design and implementation

2.5 hours working on app, got to the point where I can rotate an image and also drag it around, leaving a path behind it

0.5 hour finishing critique and continuing work on design and implementation


## Post-critique summary

Domain of creating animations seems to be well-defined and useful. Lots of initial design considerations, including: audience, interaction/input, image input, and animation creation. An important design component will be designing the interface, as that is something that is novel and importannt to how a user can express themselves in this domain-specific language. Key difficulties will be how users should be able to express the animations they want easily, as well as the designing the environment for a user to express themselves. The primitives are well-defined for the animation space I am looking to allow users to be in. There are a number of existing libraries/frameworks for this domain, such as ActionScript, BannerZest, and pyglet, all of which can be useful in how I design my language.

My description was a bit confusing as I did not clearly define what the environment and inputs really are. I should think more about the concept of creating "living" images as that is a powerful idea. My discussion of errors was a bit sparse in terms of what type of issues I could expect. I did not consider the idea that there could be too much going on in the drawing, and could possibly crash the application, which would be an error. 

Again, along with my description, my plan is still not very concrete in terms of exactly how users can create animations, whether it is by text or user interface. User testing is a great idea, and I should definitely get input from experienced animators. I should be wary about implementing this in Swift, as there may not be much of a community, and I may find Objective-C to be a better choice because of that. My flexibility in my schedule is good as it is hard to plan exactly how long each portion will take.

## Post-critique reflection

Thank you so much for the feedback Paul! It was definitely very useful, and helped me think of stuff I wasn't thinking of before. I should have been more concrete in my description, but my plan is to make this DSL solely used through a user interface. I may first textually describe the DSL (as I need some way to implement it in Swift/Objective-C), but will have to spend more time on how the user interface will look. The existing animation stuff you referenced will be very useful as I had not heard of those before, so I will spend some time this week looking into those for help in designing the language. The errors of overloading the amount of animations was something I have not considered, so that was helpful for you to point that out. I'm still unsure as to what I will do for that case, but I am hesitant to limit number of animations as hardware will continue to improve, so it would seem odd to limit it for a specific device. I may just leave it up to the user not to crash the app, but that is something I will consider more. 

The point on Swift vs. Objective-C was helpful, and something that I have considered. Both can work together, although I havent specifically looked into it. As far as I can tell so far Swift is pretty good for my use case of at least getting a prototype, but I may look further into the interopability of the two if the need arises. I will also be sure to get user feedback as I go along with the iterations of the app!

Also, I appreciate the reinforcement that this is a good and interesting DSL! 

