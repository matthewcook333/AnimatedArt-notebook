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

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

## Post-critique summary

## Post-critique reflection
