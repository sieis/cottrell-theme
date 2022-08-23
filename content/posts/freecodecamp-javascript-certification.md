---
title: "Freecodecamp Javascript Certification"
slug: "freecodecamp-javascript-certification"
author: "Eamonn Cottrell"
subtitle: "Reflections on freeCodeCamp's javascript certification"
date: 2021-12-18T13:39:37-05:00
draft: false
image: "/images/posts/freecodecamp/freecodecamp.png"
images: ["/images/posts/freecodecamp/freecodecamp.png"]
alt: "freeCodeCamp logo"
altimage: "/images/posts/freecodecamp/cert.png"
section: ""
description: "Reflections on freeCodeCamp's Javascript Certification"
---

## Victory! A Javascript Certificate

> (But more importantly, some good programming practice.)

*Minimal code included as I found it most important in these projects to not look up anyone else's sample code. The act of banging my head against the proverbial wall was as important in learning the programming concepts as anything.*

So, this took me a long time. 

I signed up for freeCodeCamp back in 2016, and it was one of the handful of tools I used to become familiar with coding. However, it wasn't until the past couple years (2019-2021) that I truly got more than casually serious about learning web development and computer programming. And I've continued to use myriad resources from Codecademy to Udemy to EdX to MITx to Google and YouTube. 

Last year, I became enthralled with bootcamps and nearly enrolled in a couple. I'm thankful that I decided against it, though, as I could never quite justify the price tag when I knew the breadth and depth of knowledge available for free out on the internet. 

And thus, I came back to freeCodeCamp.

Throughout the course of the Javascript Algorithms and Data Structures material, I was grateful for the bite-sized lessons that have you learning bits and pieces of the language and the mechanisms to program with it. But beyond that, the projects were where I could tell the true tests stood. They were always challenging enough to not breeze through, but not impossible to comprehend either.

## Elegance? A Roman Numeral Converter

In the final projects, I can certainly see my own amateur abilities, however, it's hard to overvalue the thrill of a working piece of code no matter how muddled its guts are. For the Roman Numeral Converter problem, we were tasked with converting any given number into its Roman Numeral counterpart. As I look back over my code now, it is a lengthy mess of ``` if ``` statements following a giant object holding the various iterations of Roman Numerals with which I glued together my solution.


A part of me knows there are more elegant ways to come to the solution, but puzzling through this on my own without seeking any outside help was where the learning truly took place.

``` javascript
let rules={
    0: "",
    1: "I",
    2: "II",
    3: "III",
    4: "IV",
    5: "V",
    6: "VI",
    7: "VII",
    8: "VIII",
    9: "IX",
    10: "X",
    20: "XX",
    30: "XXX",
    40: "XL",
    50: "L",
    60: "LX",
    70: "LXX",
    80: "LXXX",
    90: "XC",
    100: "C",
    200: "CC",
    300: "CCC",
    400: "CD",
    500: "D",
    600: "DC",
    700: "DCC",
    800: "DCCC",
    900: "CM",
    1000: "M",
    2000: "MM",
    3000: "MMM"
  }
  ```

  ## Comments ftw! A Cash Register Project

  I know comments are important. I just don't follow my own best knowledge all the time. During the five projects I grew progressively better at actually commenting well. For a couple, it was simple enough (in my mind at least) to not make notes through the code: particularly when the whole project was able to be completed in twenty or thirty lines. However, by the cash register problem I was commenting both for my own benefit as well as for the sake of good practice.

  The cash register took me two days to complete, and three complete restarts. I suspect that had I begun commenting and pseudo-coding out of the gate, this might have reduced my toil. Nevertheless, I was victorious in the end, and my misfires proved helpful in my learning.

  Including a fair bit of ``` console.log ```-ing left in the solution, it took me 89 lines of code to get to the finish line. I suspect there to be more elegant and condensed ways to arrive at this solution, but I'm a simple man with a mind grounded in the ```functional``` earth of ```for``` loops.

  ``` javascript
console.log("=====================")
  console.log("Original Amounts: ")
  console.log("=====================")
  console.log("price:", price, "\ncash:", cash, "\ntotal in drawer:", total, "\nchange:", change)
  console.log(`cash in drawer:`, cid)
  console.log("=====================")
  console.log("Computations:")
  console.log("=====================")
  ```

  ## Takeaways

  1. Comments are important; to not use them is to slap oneself.
  1. Elegance makes for more shareable code; dirty code can still work.
  1. Walking away from code sharpens intent; sleeping sharpens the mind.
  1. Projects are the only way to truly learn something.