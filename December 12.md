# Design notebook for week ending December 12, 2014

## Description

Yay got drawing creation to work! Turns out CAShapeLayer does not actually change the bounds even when you add the path, and so it was always centered around (0,0). I did try to change this earlier, but the issue was that the position was in the same origin, which was an issue when rotation around despite having different bounds. I also tried messing with the anchor point as it seems like it would make sense to matter, but it does not currently seem to make a difference with position and bounds set, but something to keep in mind if there is some bug later. 

I also added the ability to clear the path. One issue is that if you are currently in path making mode, and clear, and then make another path, it will not trigger the immediate animation until you press finish or done. I would like to fix this, but realize it may take a bit longer to do as I would need to think of some refactoring in how triggers should work because right now I have the animation trigger be based on notifications from the animationView, but that view has no knowledge of the path drawn after clearing. I will work on some more crucial aspects to the project before the due date, but hopefully can get back to this later.


**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

1.25 presentation brainstorm and debugging drawing

3.5 hours debugging drawing creation, critique, and adding clear path option.

## Post-critique summary


## Post-critique reflection


