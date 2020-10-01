---
layout: post
title:      "undefined method for nil:NilClass"
date:       2020-10-01 23:22:38 +0000
permalink:  undefined_method_for_nil_nilclass
---


This error has tripped me up more than anything else in rails. As soon as I see that the method I had written was undefined, I automatically assume that the problem is with that method, and on the line specified in the error. These are rarely correct assumptions. During my review for my rails project, I got tripped up on this every single time I got it, and I think it's important for me to be able to really wrap my head around how to address it before moving forward. 

In order to solve a problem, it's generally important that you can identify the entire problem. A NoMethodError usually occurs when the object a method is called on an object that doesn't have it defined, so I'm just accidentally trying to call a method on nothing. So far, the best way I've found to address this is to start by finding out what exactly is returning nil in the first place. Using the browser console, go over the pieces of code you *think* might be the problem, one by one, and determine if they're functioning how you intended them to. One of these pieces will probably return nil when you don't want it to. The most helpful thing (for me anyway) is to try not to panic. Broken code shouldn't be scary, there's always a way to fix it. Once you know what's accidentally set to nil, you can make sure that the method you're calling is defined within the class you're calling it on. I've found that after you're able to accurately identify the problem, it's a fairly easy fix. The trick is to understand the feedback rails is trying to give you. Find the piece of your code that's missing information, and give it that information. Check in your console to make sure you're now reaching the intended output, and make small adjustments as necessary. 

When debugging in general, and in particular for this error, it can be really helpful to have a set of questions you can consistently ask yourself to work through problems when you encounter them. I'm still developing my list, so its subject to change, but for now, here's what I have.

1. What is the intended output for my code?
2. Have I made sure that my problem isn't with something more superficial, like syntax or setup?
3. What exactly is my error trying to tell me?
4. What are the possible problems that could have caused this error, and how would I address each one? 

I've also enjoyed the practice of "rubber dug debugging". The idea is, essentially, that you have a rubber duck of the bathtub variety to hang out with while you code. Tell your duck about your code as you're writing it, and when you stumble on a problem, detail to your duck what your code is supposed to do, line by line. While talking with your duck, you'll find something in your code that doesn't match up with what you're telling your duck, and there you have it! 

If all else fails, diagram your code on paper. What steps does rails take when processing your code? Where is it looking for the undefined method? What class were you trying to call this method on? Visualizing code on paper is time consuming, but it lets me see me program on paper the way I see it in my head, without having to 'translate' it into words. 

Good luck in your coding ventures, and always remember not to needlessly go down a code rabbithole that ends up not being remotely related to your problem in the first place. Address things one at a time, and step by step. 
