---
id: 1009
title: User-Centric Software Design
date: 2015-04-08T19:50:21+00:00
author: Alexandru Bolboaca
layout: post
guid: http://alexbolboaca.ro/?p=1009
permalink: /software-design/user-centric-software-design
vsw_pmvw_video_source:
  - YouTube
vsw_pmvw_video_id:
  - ""
vsw_pmvw_video_width:
  - ""
vsw_pmvw_video_height:
  - ""
vsw_pmvw_video_caption:
  - ""
vsw_pmvw_video_autoplay:
  - "0"
dsq_thread_id:
  - "4384433071"
categories:
  - Design
tags:
  - usable-software-design
---
_This is a long due blog post. I wrote it before the series of blog posts on Usable Software Design ([first](http://mozaicworks.com/blog/4-ideas-apply-better-software-design/ "4 Ideas To Apply For Better Software Design"), <a title="Usable Software Design" href="http://mozaicworks.com/blog/usable-software-design/" target="_blank">second</a> and <a title="5 Steps To Mistake Proof Software Design" href="http://mozaicworks.com/blog/5-steps-to-mistake-proof-software-design/" target="_blank">third</a>) but due to a strange series of events (including totally forgetting that I wrote it) is published after them. In a sense, the ideas from this blog post are superseded by the series on Usable Software Design. In many other senses, it contains a ton of background information useful to people who want to get a better grasp of Usable Software Design._

My recent blog post, [&#8220;The craftsman I would like to be&#8221;](http://alexbolboaca.ro//articles/the-craftsman-i-would-like-to-be "The Craftsman I Would Like to Be") generated interesting reactions both from people I know and from complete strangers. I&#8217;m glad to see that the software craftsmanship communities have reached the point where we can discuss such matters of high importance for the movement and for members such as myself.

I have to admit that I expected a bit of controversy when writing this post. After all, it&#8217;s still unclear in my mind and I&#8217;m proposing certain things that I know are impossible. That&#8217;s the point of an ideal, after all.

## The Controversy

What I didn&#8217;t expect was the amount of controversy met by my views on software design. Here&#8217;s the story.

I proposed the topic called &#8220;What is good software design?&#8221; at the fishbowl session at SoCraTes UK, and I was lucky to have it picked by the majority of the participants. The discussion was very interesting and unexpected. Instead of talking about the things you would consider about software design (SOLID principles, design patterns, differences between the OO and functional paradigms etc), the discussion drifted towards the humanistic point of view on design.

&#8220;When is the last time you saw a software design that was not only useful, but amused you?&#8221;* was the (I assume) intentionally provocative statement that sparked the discussion.<!--more--> A few things were stated and questions were asked that made the debate extremely interesting:

  * Software design is engineering, it doesn&#8217;t have to be art (is more or less what Sandro said)
  * The users don&#8217;t know what&#8217;s in the software design
  * Good design is an unclear concept**
  * Understanding the users is hard work and as a developer working with UX specialists, I realize I can&#8217;t do that

While I understood the reasoning behind these statements, I have a different view. In retrospect, I think this view comes from my rare adventure: after being taught software design by a mentor and practicing it for 5 years, I worked as a trainer and coach for another 5 years. This changed my perspective; as a programmer, I only cared about code; as a trainer/coach I had to learn to care about people. While going back to programming, the people-centric experience stays with me. This is why I believe in _User Centric Software Design_.

## User Centric Software Design

I will briefly expose my view and then detail them:

Software design means **structuring the code** so that:

  1. **it works** (it does what it&#8217;s supposed to do)
  2. it **optimizes for desirable business characteristics** (most common today, it optimizes for change)

Like any design, software design is done within **constraints** (time, resources, cost, skills etc) and has **users**.

There are **two types of users** for software design:

  1. The **developers** who will change the code later
  2. The **users of the application**

**User-centric software design** means building the design so that:

  * **the developers** who use it find it **usable**
  * it holistically combines  **the triad of form, interaction and implementation** (i.e.** ** how it looks, how it acts and how it works are synchronized)

### Desirable Business Characteristics

Unless you&#8217;re writing code that you will throw away, **it&#8217;s not enough for the business to produce code that works**. If the application you work on is successful then people will use it and they will ask for new features or improvements. Being unable to change it fast might translate into loosing money or even failing due to competition.\***

I would argue that **90% of the time, the desired business characteristic is the ability to change the code fast**. However, it&#8217;s not always the case; a common case I&#8217;ve seen is modules that need performance more than change.

### Constraints

As developers, we don&#8217;t like constraints. Neither do most architects, visual designers, industrial designers etc. &#8220;If I only had more _[resource X]_&#8221; is a very common complain.

There is however a class of designers who embraced constraints. <a title="Charles and Ray Eames" href="http://en.wikipedia.org/wiki/Charles_and_Ray_Eames" target="_blank">Charles Eames</a>, the creator of many objects that you have used, said:

> I don’t remember ever being forced to accept compromises but I have willingly accepted constraints.
Some constraints are given by the context: time, availability of skills, tools, resources, cost etc.

Some constraints are self-imposed. For example, REST is nothing more than a set of constraints we, the developers, choose to follow. The same applies to: SOLID Principles, modular design, TDD etc. Why? Because working within these constraints allows better designs.

I have a long experience with constraints, after attending and facilitating over 30 code retreats. This experience taught me many things, but this is one that I rarely heard mentioned:

 **Constraints allow you to become a better designer. Embrace the constraints you have!**

### Usability of the Software Design

What if you would run usability studies on your design with a few developers? How quickly will they understand your APIs? How long until they be able to make changes in the code? When would they be able to add new features?

And, if we move to the personal level, would they enjoy working with your design?

Whenever I design an important part of a system, I use my beginner mind to make sure it&#8217;s usable. Imagine you are a new developer in the team and need to add a feature or fix a bug. What do you need to do? What can you change to simplify it?

Your design affects more things that you can imagine. It affects the morale of its users (your fellow developers),  the implementation time and consequently the business. I believe **the responsible thing to do is to make sure your design is usable.**

### The triad of form, interaction and implementation

Designing software means first that the code works as expected. This means the designer has a clear view of what the problem is. The best way I know to do this is to walk into the users shoes.

The simplest example I can give of this practice is how we name things. In a project I am working now, we had an entity called &#8220;CurrentEncounter&#8221;. Whenever we were discussing with the product owner, he was calling the same thing &#8220;Consultation&#8221;. Despite that our design was following SOLID principles and was easy to change etc, we decided to rename CurrentEncounter to Consultation everywhere in the code.

The consequence is very subtle. We were talking in the user terms, so we got more connected to the user, so presumably we understand the user problems better, therefore the design is a better fit for the user.

## How do I do User-Centric Software Design in Practice?

Before answering this question, it&#8217;s important to notice that this idea is new to me.\**** I can only give you a set of questions to ask yourself about any design.

Here it is:

  1. What are the  **desirable business characteristics** of the design? (_usually change, sometimes performance, other times low operational cost)_
  2. What  **constraints** do you have? _(technology, people, skills, time, costs&#8230;)_
  3. Are there **parts of code difficult to change**?
  4. Are there types of **features difficult to add**?
  5. How long does it take for a **new developer** to add a **simple feature**?
  6. When code changes, are there **tests difficult to change**?
  7. What type of **user** (or persona) will **benefit** from the **feature** we work on?
  8. What **user problem** are we **solving**?
  9. What is the **user scenario** that requires the feature?
 10. Are we using in code the **user language**?

## What&#8217;s Next?

Try out these ideas. Let me know if you find them useful. Tell me if you have issues with them.

The prize will go to those people who run usability tests on their software design, and share the results with us. That would be awesome.

###### Notes

_* I fail to remember the name of the person who said this. Please help me attribute this quote._

** Especially since it&#8217;s an unclear concept, it makes such a great topic for debate.

\*** Many of my clients struggle to keep up with the required level of change, and one of the reasons is the design of their applications. JB Rainsberger is one of the people who treats this subject &#8211; see his talk on the <a title="The Economics of Software Design" href="https://www.youtube.com/watch?v=7HecgbghFTk" target="_blank">&#8220;Economics of Software Design&#8221;</a>. I wished we had data to concur with these theories, but as far as I know, we don&#8217;t.

\**** Maybe I came up with it, though knowing how this industry works, I wouldn&#8217;t be surprised other people documented this practice before and we forgot it. If you know of such resources, please let me know.