# Design notebook for week ending November 23, 2014

## Description

I need to really dive into the coding/implementation this week, so I begun by trying to get rotation to work. Currently, I have a pretty good implementation of it. I am realizing that I may not actually need all the "Animation" classes as I can store the animations in UIImageViews with specific keys, which I can remove the animations simply with that. I may still have to figure out how to pause a given animation, but keep it stored.

I also went much further into how I want the overall controller/view architecture to look. At one point I scrapped my project and went for a master detail view, but realized that the master table view was really far more than I needed, and would also require much more work to really customize it the way I would like. Since there are only a finite, limited number of menu options, I decided to go with a basic UIView to get the easiest and biggest gain in customizability for how it should look. I am running into a lot of trouble with sizing things in the storyboard, which is causing a lot of frustration. Other than that, the storyboard works pretty good for making new things and adding it to the code. At the moment the sizing/frames seems to just be guess and check, so maybe I ought to just turn off autoresize.

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

1.5 hours on critique

1.5 hour working on get rotation to work with a given image on repeat

2 hours working on overall architecture and menu. Going through many iterations to figure out how to do it somewhat right, but also quickly.

## Post-critique summary

## Post-critique reflection
