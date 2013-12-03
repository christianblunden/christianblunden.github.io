---
author: Christian Blunden
comments: true
date: 2011-03-25 13:29:29+00:00
layout: post
slug: why-your-biztalk-project-will-fail
title: Why your BizTalk project will Fail
wordpress_id: 47334844
tag:
- Architecture
- Biztalk
- Systems Thinking
---

Firstly let me say that I have never used Biztalk (except for a brief personal experience back in early naughtys.. but I didn't inhale).  So I have always fretted over attempting to convince architects not to use it as I could not speak from experience.  Sure I had heard about all the pain that people went through on a daily basis (Thoughtworks rescues many such installations) and the general concensus was to run in the other direction as quickly as possible.  Historically I would have treated this as a technical argument, but I think the solution is a lot simpler.

So let's pretend for a second that you have a "messaging" problem, let's not get bogged down too much with the details.  Safe to say you probably arrived at this problem through accidental complexity of using a database as your integration strategy.  After time you had loads of services and applications tightly coupled together through database schema.  Hundreds and hundreds of tables, stored procedures and nightly batch jobs later, you end up with a big ball of mud that only few people really understand.  Cost and risk of change is high, as small changes require entire system tests as impacts ripple through the system.  Basically nothing gets done very quickly!

You may have even dug your way into further accidental comlexity with SOAP and an amazing Service Orientated Architecture. Now you services are tightly coupled with XML and your business processes locked in stone.  This spaghetti junction of services has lead to a high cost of change. Basically nothing gets done very quickly!

To be fair, you may have also had some essential complexity, with hundreds of services needing to collaborate with each other.  Each requiring their own formats and transformations.

Enter BizTalk. Now I am not going to say a bad word about Biztalk, that's not the point.  In fact, I'll even go as far to say that it is an amazing product (having never used it).  It will solve all your problems and eventually it will solve EVERYBODYS problems, because that's what Microsoft want and that is the point.  More featues will keep being added, it will even one day do [HATEOS](http://en.wikipedia.org/wiki/HATEOAS) REST, because the cool kids do it.  Heck it probably even does it now for all I know.

One thing it will never be is.. simple!

Not everyone will understand Biztalk, they can't possibly, it's too complex, it's too big, it requires specialization.  All your systems will have requirements funnelled through a single messaging platform and only a handful of people will be able to do the work.  You will have created a huge bottleneck for work to pass though and... Basically nothing gets done very quickly!
