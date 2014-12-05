# Design notebook for week ending December 7, 2014

## Description

***12/1***

Started working on the project this week by implementing speed sliders. I now have a rotation speed slider working, although there are changes I would like to make to it as right now it resets the position every time the slider changes, and I would rather it just update the old animation that existed. To do so cleanly may require some refactoring of the code.

***12/3***

Got the rotation speed slider to not reset each time the slider is moved, which looks a lot better now. Not perfect, but I am happy with it. Took a fair bit of trouble to get this to work with the issue of trying to edit existing animations, which exist within a layer. If I was just changing the layer it would be fine, but there are individual animations so I don't want to be working on that level. Also implemented the path speed slider, which currently works, but one issue is that as the path gets longer, the animation goes faster that the "animation" is the entire thing. I tried changing speed instead of duration, but no luck. At the moment it may be more trouble than it is worth to do a lot of math to calculate length of the path, so I may just let that be for now as there are other bigger things to work on, as it looks relatively smooth, just odd as you make the path super long. Also made it so that the animation immediately starts while you are drawing for better feedback. 

***12/4***

The path now hides on "Done", which is good. One issue is that I am removing the layer by checking if it is a CAShapeLayer, which is fine for now, but once I add the ability to draw it will be an issue. Currently looking into how I can make drawn pictures animated. It seems like it will not be too bad, as I can simply make the CGPath drawn into a CAShapeLayer and make that the "CurrentAnimatable". I need to see if there is some way to add keys possibly to each sublayer, or when removing paths, I could first check to make sure it is not "Animatable" type so that I do not remove those.

***12/5***

Having a fair bit of trouble understanding the ImageContexts correctly to try to get an image as the contents of the Animatable. I finally got it so that I could make a UIImage out of the ImageContext I make using the drawn path, but setting that to the contents of the Animatable is not doing anything, even when forcing the layer to redisplay. Still investigating this issue, currently trying to override the display function for Animatable but having issues with contents being nil for some reason.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

1.25 hours on critique

1 hour working on speed sliders

1.5 hour working on smoothing out rotation speed slider and implementing path speed slider and instant feedback of animation after drawing

0.5 hours on path hiding and thinking about drawn images and critique feedback

1.25 hours working on image drawing

1 hour continuing work on image drawing

## Post-critique summary

Overall, my interface and what I have so far is pretty good, but is not complete given a prototype. As I cannot easily has sample applications, I need to make sure that it is easy for a user to know how to make something. One way to do this is to guide them through what they should be doing next. One important feature for me to add is the speed sliders. Also, what would be nice is to allow for user-drawn images, as that would more closely express what I want to allow the user to do. Also, adding more animations rather than allow for chaining is a fair goal to have done by the end of the semester.

## Post-critique reflection

Thank you for the feedback! I definitely agree that the prototype does not show exactly the power of the language, as I think I need to allow for user drawn images to really show that, as well as more animation types and relationships (e.g. nesting, chaining, etc.). One of the things I am currently working on is the speed sliders, and will be working on allowing for drawing the pictures after that.
