# Design notebook for week ending November 2, 2014

## Description

Much of the work this week is brainstorming a DSL idea and really solidifying what it means for it to be a DSL. Much of the design decisions is really, "how can I make sure this is language-y, and allow the user to easily express their intention?". At the moment, I don't have many specific open questions, but I am curious what people think of the idea, whether they would find it useful/fun, concerns for the project, or ideas that would be really neat for me to include.

I don't really have any cool things to share so far. I have brainstormed a lot and filled out the design and plan. I have also learned a bit of Swift and went through tutorials to make a tip calculator app. Swift is really cool so far, although I do know that tutorials and the like are more prone to show off the strengths of Swift, rather than the limitations, so I will be wary of that. The Playground environment in XCode for developing in Swift is AWESOME! It allows for instant debug/implied print messages, as well as instant UI feedback. This means that you can describe a UI element, and it will automatically display. This is useful when you are hardcoding pixel values, and find it hard to picture/know exactly how it will look. The Playground does still have occasional bugs, such as saying there is an error when there actually isn't, but for the most part it has been very useful.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

How to design the Intermediate Representation (IR). Prof. Ben emphasized that this should be something I should focus on, and I do agree that it can be very interesting. I am trying to allow a dynamic image to be easily described in a static representation, which is doable, but to be effective I need to carefully think about how I express it. One design decision I am concern about is the idea of having nested animations, where one animation image can be part of a whole different animated image, and so it would have attributes of both. I haven't quite thought about exactly how I will represent that, or maybe even if I should (maybe there is a way to get around the issue? I could just make it so that instead of nest, you simply allow for each image to have identical animation attributes). 

**What questions do you have for your critique partners? How can they best help
you?**

If you were to use this DSL (i.e. if you wanted to make a quick animation just for fun), what would you like to be able to express? Are there other aspects of this domain that you can think of that might be neat to incorporate? 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

About 3 to 4 hours brainstorming and researching existing ideas (I went through many iterations of projects that ranged from completely different to very similar to the current idea).

2 hours learning Swift and doing Tutorials.

0.5 hours looking over all the projects overview stuff for the rest of the semester.

2 hours both writing up the project plan, description, and notebook, as well as more designing and thinking while doing it.

1.5 hours more on learning Swift from Apple's Swift book.

## Post-critique summary

Domain of creating animations seems to be well-defined and useful. Lots of initial design considerations, including: audience, interaction/input, image input, and animation creation. An important design component will be designing the interface, as that is something that is novel and importannt to how a user can express themselves in this domain-specific language. Key difficulties will be how users should be able to express the animations they want easily, as well as the designing the environment for a user to express themselves. The primitives are well-defined for the animation space I am looking to allow users to be in. There are a number of existing libraries/frameworks for this domain, such as ActionScript, BannerZest, and pyglet, all of which can be useful in how I design my language.

My description was a bit confusing as I did not clearly define what the environment and inputs really are. I should think more about the concept of creating "living" images as that is a powerful idea. My discussion of errors was a bit sparse in terms of what type of issues I could expect. I did not consider the idea that there could be too much going on in the drawing, and could possibly crash the application, which would be an error. 

Again, along with my description, my plan is still not very concrete in terms of exactly how users can create animations, whether it is by text or user interface. User testing is a great idea, and I should definitely get input from experienced animators. I should be wary about implementing this in Swift, as there may not be much of a community, and I may find Objective-C to be a better choice because of that. My flexibility in my schedule is good as it is hard to plan exactly how long each portion will take.

## Post-critique reflection

Thank you so much for the feedback Paul! It was definitely very useful, and helped me think of stuff I wasn't thinking of before. I should have been more concrete in my description, but my plan is to make this DSL solely used through a user interface. I may first textually describe the DSL (as I need some way to implement it in Swift/Objective-C), but will have to spend more time on how the user interface will look. The existing animation stuff you referenced will be very useful as I had not heard of those before, so I will spend some time this week looking into those for help in designing the language. The errors of overloading the amount of animations was something I have not considered, so that was helpful for you to point that out. I'm still unsure as to what I will do for that case, but I am hesitant to limit number of animations as hardware will continue to improve, so it would seem odd to limit it for a specific device. I may just leave it up to the user not to crash the app, but that is something I will consider more. 

The point on Swift vs. Objective-C was helpful, and something that I have considered. Both can work together (TO BE CONTINUED

Also, I appreciate the reinforcement that this is a good and interesting DSL! 
