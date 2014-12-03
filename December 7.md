# Design notebook for week ending December 7, 2014

## Description

***12/1***

Started working on the project this week by implementing speed sliders. I now have a rotation speed slider working, although there are changes I would like to make to it as right now it resets the position every time the slider changes, and I would rather it just update the old animation that existed. To do so cleanly may require some refactoring of the code.

***12/3***

Got the rotation speed slider to not reset each time the slider is moved, which looks a lot better now. Not perfect, but I am happy with it. Took a fair bit of trouble to get this to work with the issue of trying to edit existing animations, which exist within a layer. If I was just changing the layer it would be fine, but there are individual animations so I don't want to be working on that level. Also implemented the path speed slider, which currently works, but one issue is that as the path gets longer, the animation goes faster that the "animation" is the entire thing. I tried changing speed instead of duration, but no luck. At the moment it may be more trouble than it is worth to do a lot of math to calculate length of the path, so I may just let that be for now as there are other bigger things to work on, as it looks relatively smooth, just odd as you make the path super long. Also made it so that the animation immediately starts while you are drawing for better feedback. 

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

## Post-critique summary

## Post-critique reflection
