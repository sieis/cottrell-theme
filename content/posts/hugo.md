---
title: "Go Go Hugo"
author: "Eamonn Cottrell"
subtitle: "Making a Hugo Theme"
date: 2021-11-04T13:11:51-05:00
draft: false
image: "/images/posts/hugo.png"
alt: "Hugo banner image"
section: ""
layout: ""
---

This past week, I've put together my first legit theme for Hugo, and it's for a pretty niche audience: recovery groups.

## The Problem: Recovery Groups are Still on Dial Up

Most groups are in the stone age when it comes to technology. If they do have a page, it's something that looks terrible, was made a century ago, and is no longer maintained.

Groups have regular literature and liturgy that circulates for participation in every meeting--often occurring many times through the week.

All groups depend on donations for their expenses, yet for most of them, COVID was the first time they'd even considered online collections.

When I identified a need for recovery groups to have a minimal online presence during the pandemic, I built a few sites, and then realized it would be more beneficial to have a theme template to offer widely.

## re-cover

The re-cover theme was born from this need. It is meant to address the more common web needs of a group. Namely, a clean, readable and easily accessible site for any member to:

1. Find basic information about the meeting. i.e. location, times, format.
1. Access the meeting guide and participate without the need for paper handouts.
1. Access any online only meeting resources.
1. Contribute donations to the group easily online.

## The Process: Adapting a Theme From a Site

I built the first two groups' sites from scratch using HTML, CSS and a hair of Javascript. They both used Bootstrap with small custom CSS modification.

And both sites were almost mirror images of each other in terms of functionality. The visuals were different because I enjoy minimalist design, but aside from some copy details and minor group specific differences, they were the same site.

This was a good exercise for me in building from scratch, but not great in terms of reusable code.

So, I fired up a new Hugo site and theme, and started backfilling it with the format and information I knew that virtually every group would need.

## General Data

For universally used copy, I made files called partials which were able to be used throughout the theme to display various things like readings. This eliminated the need to re-write and format things that pretty much all groups are going to use.

It also allows for the ability to add additional needs in the future on a case by case basis, and simply add that to the overall theme.


## Group Specifics

For group specific information, I setup a config file which can be edited all in one place up front.

After this, the site generator will automatically use all those group specific values to display the pages properly.


## Jamstacking

I've been interested in Jamstack development generally and Hugo as a static site generator specifically for a few years now.

The ecosystem provides a way for relatively green developers to jump into projects that are more technical than, say building a Squarespace site, but more accessible than languishing through impossibly complex codebases.
Ever since tinkering with Hugo for the first time while at the hospital for the birth of our second child, I've singled it out from the other players as the SSG I'd like to know better. I figure it'll be better to actually learn React before jumping into Next or Gatsby.

## Tooling & Getting Started

I am a sucker for tinkering. Projects like this are littered with learning opportunities straight out of the gate and all the way through to after it's live (I made a couple modifications this morning after waking up and realizing I hadn't included the ability to add a Google Analytics tag!)

If you're wondering where to start with web development, or with the Jamstack, or with programming...just jump in to the nearest thing that interests you.

The learning that happens along the way continues to fuel me for the next project and inspire me to keep going.

Thanks for reading, and have a great one! I'd love to connect; feel free to drop a message to me on LinkedIn or Twitter.