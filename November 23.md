# Design notebook for week ending November 23, 2014

## Description

I need to really dive into the coding/implementation this week, so I begun by trying to get rotation to work. Currently, I have a pretty good implementation of it. I am realizing that I may not actually need all the "Animation" classes as I can store the animations in UIImageViews with specific keys, which I can remove the animations simply with that. I may still have to figure out how to pause a given animation, but keep it stored.

I also went much further into how I want the overall controller/view architecture to look. At one point I scrapped my project and went for a master detail view, but realized that the master table view was really far more than I needed, and would also require much more work to really customize it the way I would like. Since there are only a finite, limited number of menu options, I decided to go with a basic UIView to get the easiest and biggest gain in customizability for how it should look. I am running into a lot of trouble with sizing things in the storyboard, which is causing a lot of frustration. Other than that, the storyboard works pretty good for making new things and adding it to the code. At the moment the sizing/frames seems to just be guess and check, so maybe I ought to just turn off autoresize.

Ok so I did quite a bit in terms of architecture! For one, I wanted to separate the concerns of the animation menu by allowing animations menu to have its own view controller that can control which animation type view is being shown. Went through quite a bit to get this done as Storyboard was being insanely frustrating with autosizing issues, and things disappearing/resizing to be negative pixels somehow. At this point, I made the decision I would ditch storyboard and hardcode UI elements, as I had more experience doing that. But, after doing that for a long enough time with fiddling with stuff, I realized that it is actually not a good idea as I am prototyping and could change the UI a lot, which is a huge pain with these hardcoded values. So instead, I decided to "properly" do Storyboard, rather than sort of hacking away at it until something works. Learned a bit as to how to do what I need, and got what I need so far, and it looks pretty good! Still some relative sizing issues, but nothing too major so I could probably figure out the rest later.

I also decided that I will have a textfield and picker to choose the animation type, which I feel may be the easiest way for now, as it would be simpler to just change what animation type you have, and show the view for that (this is as opposed to some table with expand/contracting fields, which although I know is possible, I am not very familiar with). Architecturally, at the moment I also think I will have each of those animation type views (I have a view for each type) create the CAAnimations (Core Animations) and pass them through NSNotificationCenter to the DrawView, which can then animate the given image. I still have to decide how I can label each animation with the key to be removed later if I follow this method of having the UIImageView agnostic to what type of animation is being applied. 

I spent a fair bit of time with simply UI debugging, which is frustrating, but I do feel like I am learning more about how it works in terms of how things interact with each. The Optional value type was really frustrating for me at first, since the idea is that the Storyboard is suppose to enforce those exist, yet many times they are still nil. I have learned a good bit of the different types of errors associated with this in terms of things not being connected, not having UI elements exist at the right layer, etc. I also spent some time figuring out message passing in iOS, and learning NSNotificationCenter to be able to have the drawView listen for notifications for animations, and pass the animation as an object.

I have been running into a lot of issues with Interface Builder and also trying to manipulate views/control flow programmatically. I spent way too much time debugging, mostly to just figure out that there are still bugs with StoryBoard/Interface Builder, and so many suggestions on StackOverflow are just to keep redoing the connections, restarting XCode and simulator, cleaning project, etc. At the end of this all and really feeling a bit hopeless with it, I decided to go with just a simple UI design without much control flow stuff. So, I am now planning on just having one static view with all of the animation types, which should be fine if I plan to keep 4-5 animation types. 

After figuring that out and cleaning the code up a bit, I got to start spending time with the path creation animation. I've learn a bit of how they work, but only along two points. Still trying to figure out a way to allow the animation to take an array of CGPoints.

Finally got a path to work! Had to make a fair number of changes. No longer use my Line class and the array of points, instead I save the point in a BezierCurve in order to easily animation the path. Now I realize I have to do a lot more with CALayers, and realizing everything I am doing is with that, and not with UIViews. As a result, I have decided to make my Animatable a CALayer, rather than UIImageView, as otherwise I can't animate it with a CAAnimation easily. 


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

1.5 hours on critique

1.5 hour working on get rotation to work with a given image on repeat

2 hours working on overall architecture and menu. Going through many iterations to figure out how to do it somewhat right, but also quickly.

3.5 hours working on code: LOTS of architecture stuff and figuring out how things interact, and storyboard stuff (and back and forth changes, as explained above)

1.25 hours working on critique feedback and coding and debugging XCode Interface Builder stuff.

1.25 hours continuing to debug and coding views

1.5 hours with more debugging Interface Builder, simplifying design to work better for prototyping, and coding animations stuff.

1 hour working on path animation, which semi-works now!

## Post-critique summary

The current set of animations seem interesting, especially with the set of options for the given animations. One thing I should consider is the concept of a duration for an animation. I should consider what images should do for when they go outside the view for drawing. I should add the animation for growing and shrinking images. It would also be cool to allow for control over how the animations work rather than just have them in a linear fashion, though this may diverge from what I am currently trying to do. There are a number of things like background color that I could add to give more power to the user, but not sure how difficult the implementation would be.

## Post-critique reflection

I definitely agree with the idea of adding some concept of duration, as it would be either near useless to chain something after 1 oscillation, or be very tedious to add multiple of those and then something else. Also, thank you for pointing out what images should do when drawing the path, as right now I think they are above everything, and so would show up above the animation menu. I also do plan on allowing an animation for scaling/expanding/shrinking. At the moment, I think will leave my animations in a linear fashion, as I suppose I am thinking the language more for making a drawing that moves around, but is not to the extent of a movie. Some things like allow something to disappear for some period of time could be useful, as right now there is no concept of synchronization between different drawings for when they should each complete.
