---
title: "Google Sheets Finance Tracker"
author: "Eamonn Cottrell"
subtitle: ""
date: 2022-02-22T16:13:16-05:00
draft: false
image: "/images/projects/personal-finance-tracker.png"
alt: ""
section: ""
code: "https://eamonn.gumroad.com/l/personalfinance"
demo: "https://docs.google.com/spreadsheets/d/1GQP0bzdLkzZj69DsyRdtyTF0-KOVYVzqs3-fd67Ldi0/edit#gid=2127387066"
problem: "Problem to solve:"
solution: ""
description: ""
---

## A Yearly Tradition; a New Year's First Project

Even the simplest of things invites complication, tedium, and a tendency to overact to my own compulsive perfective nature.

I built an expense tracker with Google Sheets. Not my first. I’ve been building and using these every year since at least 2013. My wife and I share the same sheets to simply track our expenses daily. 

We are both users of credit cards and debt, but we both abhor overextending our financial means. As such, we’ve been ruthless in our paying down credit cards every month (or often, every week) such that balances are never accrued, interest never owed, and grief never spilt. 

This year, I decided to make the expense tracker an actual product that others are free to use. I’ve been fascinated with the world of independent web developers, creators and serial entrepreneurs. Time to join the ranks, I say.

So, I’ve cleaned up the sheet, condensed the multi-tabbed workbook down to one primary transactions sheet accompanied by a starter sheet and an analysis sheet, and posted the link as a product on Gumroad.

So simple, I thought. Not so. See, I’m not interested in merely pawning off another mediocre spreadsheet. I’d like to use this and the products to follow as tools to hone my craft. Namely, as practice in building, marketing, maintaining, and eventually selling online products that are useful to people. 

{{< youtube E9oeEXdJFbg >}}

I use this as a way to stay accountable to what’s actually in my bank account. I’m not rich; I’m a normal dude with a family and a bunch of expenses—foreseen and unforeseen. I have credit cards and a mortgage and a minivan. And I want to steward my money well. I don’t want to pay credit card interest. I want to save for the future. And I want to buy cool stuff from time to time without feeling guilty. Staying ahead of my expenses, and counting every single transaction as though it were already out of my bank account are habits I’ve come to live by, and I’m better for.

The product is available now, and since initially posting it, I’ve done a handful of things:

1.	Created a walkthrough video on YouTube showing the sheet in use and guiding a first-timer through the quick setup. Most of the spreadsheets for budgeting and personal finance have turned me off by trying to either do too many things out of the gate or by overcomplicating the getting started process. My primary focus is making getting started real easy, real simple and real fast. This isn’t a budget. That can come later. 

1.	Adding some quality of life changes. I’ve adjusted the charts and slicers for analysis. I’ve modified the formulas to make things smoother behind the scenes, and I am continually updating with tweaks as I use the new sheet myself and find issues in it.

1.	Added conditional formatting to have expenses be shaded in light red and income in light green.

    1.	Changed the running balance formula in column F so that the conditional formatting in column C behaved correctly.
    
    1.	Added a Data Validation to column A so that a drop down calendar for dates is available on double-click, and to ensure that a valid date is entered for analysis.
    
    1.	Further modified balance formula to handle empty income inputs on Start Sheet. This involved using IFS(), AND() and ISBLANK() functions.

I’ve made it available as a pay-what-you-want product. So, I expect most people to simply pay $0 and check it out which is great. This is an exercise in product creation and management; I don’t expect much revenue to be generated.

This particular project has been one of the single most important parts of my wife’s and my solid financial management. Simply tracking our expenses by manually inputting them daily and knowing what our running balance is has been a gamechanger. There are plentiful tools available to automate all this stuff, and that’s great if you’re on top of it. But if you’re just getting started, if you’re a little uncertain about how to actually manage your finances, the first step is to know what’s going on. Try out this sheet for a few months to get a grasp on where your money’s going. You don’t even have to change any habits. 

* Check it out: https://eamonn.gumroad.com/l/personalfinance

* Here’s the YouTube video walkthrough: https://www.youtube.com/watch?v=E9oeEXdJFbg

* Follow me on Twitter here: https://twitter.com/EamonnCottrell

* Follow me on Gumroad here: https://eamonn.gumroad.com/follow

* I write on LinkedIn: https://www.linkedin.com/in/eamonncottrell/, Hashnode: https://blog.eamonncottrell.com, and my site https://www.eamonncottrell.com/ 