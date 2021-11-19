---
title: "Recursion"
subtitle: "or How I Learned to Stop Thinking and Love the Thoughts"
date: 2021-10-24T13:52:01-05:00
draft: false
image: "/images/posts/recursion.png"
section: "posts"
---

I'm not a genius, but I have managed to accumulate a fair amount of know-how about a lot of things from specialty coffee to writing fiction to web development.

One of the problems I run into when I'm diving into a new (or old) subject is my seeming inability to stop prodding at its underlying roots.

When looking for a TV series to watch, I become lost in a rabbit hole of browser tabs, backstories and articles on the proper way to consume content that was intended to simply be entertaining.

When siphoning through project ideas, I can easily become engrossed in the process of making and organizing the very spreadsheets and Notion documents that are meant to simply hold the list of ideas.

When learning new technical skills, I can lose hours scratching the details of a particular problem, debugging a function or searching for how to phrase a question I need to answer but don't quite understand.

And those hours are precious to me. Perhaps the most important rhythm for my life today is balancing the active duty work time I'm responsible for with the intrinsically rewarding study time I need to grow in a way that allows for the maximum amount of quality family time with my wife and young children.

What a conundrum! I want my 36hr day, universe! :)

When revisiting recursion at its most basic level with a very rudimentary example this past week, I dove back into a topic that I've grasped on a number of previous occasions, but never truly grokked.

I think I've got it this time. And it came way after I knew how this worked. I actually understand it now.

You know what made the difference? Slowing down.

Understanding Why is More Important Than Knowing Why
Check this out. It's like a loop, but better. Often touted as a more elegant, powerful solution than a simple for loop, recursion makes use of the ability to call functions within functions in a manner of bundling up the solution.
```
function factorialize(num) {
  if (num==0) {
    return 1;
  } else {
    return num * factorialize (num-1);
  }
}
// factorialize(5) will return 120
```

Recursion calls the very function it's evaluating from within itself. It's pretty cool, but also mind-bending. In the first bit, we close a potential infinite loop by letting the function know that when num is equal to zero, just return 1.

Remember that 0! = 1...(but be careful not to blow your mind apart if you're interested in exploring why this is actually true)


So here's where I'd gotten before in my quest to know about recursion. It comes naturally to me to dive into video explanations and walkthroughs, but they often don't allow for any deep learning to take place.

Until I am within the problem myself, I often lack the ability to fully understand its solution.

Back to the problem at hand: we have a one line solution for the factorials of all numbers other than 0:
return num * factorialize (num-1)
What's happening here?

Num is 5, so we're returning 5 * factorialize (5-1).

Okay, so next time, we're returning 4 * factorialize (4-1).

And then 3 * factorialize (3-1).

And then 2 * factorialize (2-1).

And finally, 1 * factorialize (1-1)...which is 1 * 1.

Here's where it's easier for me to box each of those lines back up in reverse order. We got down to our base case in the last line by taking the factorial of 0 which is 1. This gives us actual numbers to plug back into the previous line.

Factorialize (2-1) is equal to 1 * 1 at this point. So on that line, we then know that factorialize (3-1) is equal to 2*1. Parse through the final line of 1 * factorialize (1-1) slowly if this isn't clicking yet. This is the critical part where we start to take numbers back up through the recursive call.

Thus, we've got numbers to plug into the line before it: 3*2.... and then that rolls up into the line before it: 4 * 6. And finally, that wraps back up into the first line since by this point we know that factorialize (5-1) evaluates to 24. So the final calculation gives us the final, real, answer: 5 * 24 = 120.

I write it all out because to conceptualize it, I had to quite literally spell everything out before it clicked. There are a ton of YouTube videos that explain exactly this in more colorful ways, but until I broke it down piecemeal myself, I knew that it worked while not entirely understanding the depth of how it worked.

This is emblematic of software development and computer programming in general. And many, if not all, things in life for that matter. Learning by doing, by building, by screwing up and trying again, is by far the most impactful method of acquiring even a modicum of skill in this fascinating world of ones and zeros.


## Thanks!

Hey, thanks for reading. I'm incredibly interested in web development, and write about my journey here and on LinkedIn. I've produce a handful of podcasts that sap any of my leftover creative energy!

Follow me on [LinkedIn](https://linkedin.com/in/eamonncottrell) & [Twitter](https://twitter.com/eamonncottrell); I've resigned to lite participation on these two social networks :)