# Design notebook for week ending December 12, 2014

## Description

Yay got drawing creation to work! Turns out CAShapeLayer does not actually change the bounds even when you add the path, and so it was always centered around (0,0). I did try to change this earlier, but the issue was that the position was in the same origin, which was an issue when rotation around despite having different bounds. I also tried messing with the anchor point as it seems like it would make sense to matter, but it does not currently seem to make a difference with position and bounds set, but something to keep in mind if there is some bug later. 

I also added the ability to clear the path. One issue is that if you are currently in path making mode, and clear, and then make another path, it will not trigger the immediate animation until you press finish or done. I would like to fix this, but realize it may take a bit longer to do as I would need to think of some refactoring in how triggers should work because right now I have the animation trigger be based on notifications from the animationView, but that view has no knowledge of the path drawn after clearing. I will work on some more crucial aspects to the project before the due date, but hopefully can get back to this later.

I now have the ability to change the color of what you draw with! It took waaay longer than expected as I didn't realize the issue that when I change the color, it changes the color of all previous parts of the paths that were already drawn. Tried multiple different methods of getting this to work, and I don't think it is possible. I ended up just having each Animatable keep track of each length of path, and drawing them individually as different CAShapeLayers in the sublayer (which had issues, but finally worked!). Cleaned up the UI a bit. One bug at the moment is that you can draw into the menu, and I think that is an issue from when I was doing Storyboard resizing, but not sure how to fix it as right now I'm just doing trial and error. And maybe for now that is okay since this is more a temporary UI for the long term as I would like to be able to hide the animation menu in a sliding view.


**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

1.25 presentation brainstorm and debugging drawing

3.5 hours debugging drawing creation, critique, and adding clear path option.

1.5 hours working on allow color changing and color picker

2 hours finishing color changing for drawing and moving UI elements

1.5 hours cleaning up code and finished final document


