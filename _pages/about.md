---
layout: page
title: About
permalink: /about/
---


smooth HEP is a group of people who are interested in high-energy physics (HEP) analysis that can be done in a *differentiable* (smooth) way. This is just jargon for wanting to optimize the analysis directly with respect to the physics goals of interest using gradient-based methods, such as gradient descent. 

We can make this possible if we keep track of the derivatives of each step (i.e. line of code) of the analysis with respect to their inputs. While that may sound like a harsh requirement, this is made pretty simple thanks to the magic of *automatic differentiation*, or ‘autodiff’ for short. If you code up a program using a library that supports autodiff, the library will keep track of the gradients throughout your program by stepping through each elementary operation -- e.g. addition, subtraction, multiplication, division, which have known differentiation rules like the product rule -- and calculates the gradients using the chain rule. 

Of course, this is not without its caveats, as not all lines of code are necessarily differentiable. In particular, common operations in HEP like binning a set of data or making a cut do not vary smoothly with respect to their inputs. That’s why there’s an ongoing effort by this group to provide drop-in replacements for these operations that are differentiable, as well as entire analysis ‘blocks’ that are also differentiable, such as statistical model building using HistFactory, or inference using the profile likelihood as a test statistic.

Check out what we're working on:

