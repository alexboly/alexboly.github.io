---
id: 1286
title: 'Applying the design principle of &#8220;white space&#8221; to code'
date: 2017-02-15T12:25:27+00:00
author: Alexandru Bolboaca
layout: post
guid: http://www.alexbolboaca.ro/?p=1286
permalink: /software-design/applying-the-design-principle-of-white-space-to-code
dsq_thread_id:
  - "5553198719"
categories:
  - Design
---
I&#8217;m very interested in applying general design principles to software design. I am convinced that software design is just design applied to a specific material: code. Since design as a discipline is thousands of years old (the pyramids were designed) while software as we know it today is only a few decades old, I find it obvious that there&#8217;s a lot to learn from it.

Part of my exploration was to understand more about the design principles other designers use. One very common principle is the &#8220;white space&#8221; or &#8220;negative space&#8221;.

<!--more-->

## The importance of white space / negative space

White space is very often used in design. From clean, readable web UIs, to modern furniture, modern phones, buildings and, of course, art. Here are some examples from <a href="https://webdesign.tutsplus.com/articles/using-white-space-or-negative-space-in-your-designs--webdesign-3401" target="_blank">an excellent article on the topic</a>:

[<img class="size-medium wp-image-1287 aligncenter" src="https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/linespacing.png?resize=300%2C145" alt="" width="300" height="145" srcset="https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/linespacing.png?resize=300%2C145 300w, https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/linespacing.png?w=620 620w" sizes="(max-width: 300px) 100vw, 300px" data-recalc-dims="1" />](https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/linespacing.png)

[<img class="size-medium wp-image-1288 aligncenter" src="https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/applestore.jpg?resize=300%2C187" alt="" width="300" height="187" srcset="https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/applestore.jpg?resize=300%2C187 300w, https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/applestore.jpg?w=620 620w" sizes="(max-width: 300px) 100vw, 300px" data-recalc-dims="1" />](https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/applestore.jpg)

[<img class="size-medium wp-image-1289 aligncenter" src="https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/google.png?resize=300%2C163" alt="" width="300" height="163" srcset="https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/google.png?resize=300%2C163 300w, https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/google.png?w=620 620w" sizes="(max-width: 300px) 100vw, 300px" data-recalc-dims="1" />](https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/google.png)

[<img class="size-medium wp-image-1290 aligncenter" src="https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/vase.png?resize=300%2C194" alt="" width="300" height="194" srcset="https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/vase.png?resize=300%2C194 300w, https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/vase.png?w=620 620w" sizes="(max-width: 300px) 100vw, 300px" data-recalc-dims="1" />](https://i2.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/vase.png)

Moreover, negative space is also used in designs of things that we cannot see. When we talk about sound, negative space is silence. One of my all time favourite songs, <a href="https://www.youtube.com/watch?v=IS6n2Hx9Ykk" target="_blank">&#8220;Stairway To Heaven&#8221;</a>, owes much of its appeal to the breaks that emphasize the sound. Great actors and public speakers know that silence makes their performance stand out; just listen to Morgan Freeman narrating anything (an example <a href="https://youtu.be/s1f4AoMkN0g?t=368" target="_blank">linked here</a>) and focus on the moments of silence.

## White space / Negative space in code

There&#8217;s no question in my mind that negative space should apply to code as well. But how? I struggled with this question for about two years. Last week, after a conversation on the software craftsmanship slack group (see it at the end of the post), it hit me:

**Negative space is what we take out to emphasize the rest.**

**Negative space in code is what we take out of the code to emphasize the rest.**

So, what do we take out of code? Obviously, code constructs like:

  * Comments
  * Classes
  * Methods
  * Parameters
  * Fields
  * etc.

Of course, by &#8220;taking out&#8221; I don&#8217;t mean &#8220;completely taking out&#8221;, just as much as using white space doesn&#8217;t mean every web page should be blank. It just means **take out anything that doesn&#8217;t serve a goal**.

The highest principle of design is intent; anything that expresses intent weakly or not at all should be taken out.

## Why should we care about taking things out of code?

There&#8217;s no secret that software development is a brain-intensive activity. The cognitive load is often too high for the brain to bear, and that&#8217;s when development slows down or mistakes happen.

Remembering and juggling with concepts in your head takes a lot of energy. Anything that you can leave out will make the code easier to work with. Your brain will thank you if you don&#8217;t have to try and understand something like this:

<a href="https://reidmiddleton.files.wordpress.com/2015/05/gettysburg-01.png" target="_blank" class="broken_link"><img class="aligncenter wp-image-1291 size-medium" src="https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/gettysburg-01.png?resize=300%2C131" width="300" height="131" srcset="https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/gettysburg-01.png?resize=300%2C131 300w, https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/gettysburg-01.png?resize=768%2C336 768w, https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/gettysburg-01.png?resize=1024%2C448 1024w, https://i0.wp.com/www.alexbolboaca.ro/wp-content/uploads/2017/02/gettysburg-01.png?w=1575 1575w" sizes="(max-width: 300px) 100vw, 300px" data-recalc-dims="1" /></a>

## What&#8217;s Next?

Up to you. What will you take out of your code? Or none of this matters to you? Let me know in the comments.

## Conversation with Alex Migutsky (mr_mig):

_mr_mig: @alexboly The &#8220;whitespace&#8221; seems to me to be a lack of continuous signal, a period of relaxation in a system._  _From the neural point of view, it may be a relaxation of attention &#8220;to let things sink in&#8221;._  _Can it be a relaxation of &#8220;software design flow&#8221; in a sense of giving a system time to settle in (pentesting, stress tests, QA, refactoring)?_

_@mr_mig I thought a bit more about white space. What you are proposing is more like a break in the design process, whereas white space is something left out of the design as result. (see <http://www.alexbolboaca.ro/software-craftsmanship/an-attempt-at-clarifying-the-software-design-vocabulary> for more details)_

_@mr_mig but with this in mind, I thought about what we leave out of code. And I think I&#8217;m on to something: the equivalent of white space to code is when a class has two methods instead of twenty_

_@mr_mig we tend to add more methods, but we delete them and leave space for the mind to comprehend the interface_

_@alexboly so, it&#8217;s kinda SRP?_

_@mr_mig kinda SRP and ISP_

&nbsp;