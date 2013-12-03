---
author: Christian Blunden
comments: true
date: 2010-06-03 13:00:00+00:00
layout: post
slug: 2010/06/living-prototypes.html
title: Living prototypes
wordpress_id: 42196065
tag:
- agile team
- collaboration
- design
---

Recently on a project we had the pleasure to work with a colleague of mine Alex McNeil, in what I thought was a very interesting and successful way of developing UX friendly designs.

The story starts off with a familiar tale, we had just been given a set of designs from an external design agency, which according to the client developers had a history of excruciatingly painful changes. Even more so, was that the so-called "web" designs, were semantically incorrect, ie having a radio buttons for optional choice fields, or standard editable text fields for static read only data.

The marketing department loved this design agency and would fall into the habit of requesting 1001 changes, which would ultimately blend changes in _behaviour_ as well as _aesthetics_. The poor developers would only find this out through constant revision after revision of print outs of the designs, just to notice that "that check box is now a radio button, because the field is no-longer optional". You get the picture...

**So how did we turn this around?**

  1. _Taking control of the designs _- almost day zero of the project we took ownership of the designs and proclaimed that all changes must now go through our designer Alex, the BA and developers. Changes were still welcomed, but now we could control their arrival.
  2. _A Living Prototype_ - this idea was born from chance more than anything during the project inception after estimates were presented to the client.  In short, our estimates were far too long, in fact they needed it done "next week", an impossibility! The client would not move on this date, and when asked why the date could not be moved it was due to a national sales conference. They needed something to demo. Ahah! What we needed was a living breathing working prototype (more than a wireframe), that looked and behaved like the real thing but could be done in a week, whilst the real application proceeded along it's merry way.

**So how did this work technically?**

Although we were using Asp.Net MVC and string template, this same technique can apply to any templating engine that allows you to partition and include sub-templates within other templates.

We first created a "Demo" controller, from which Alex could begin working from and creating static html templates, styling and any "fake" javascript functionality. The master page and sub templates which were to be shared later on, were placed in relevant view folders matching the expected future controllers.

/static/js/demo.js

<meta charset="utf-8">/static/css/real-style.css

/controllers/DemoController.cs

/views/Shared/master.st

<meta charset="utf-8">/views/Demo/index.st _(drives out sub-templates, master.st and real-style.css)  
_<meta charset="utf-8">/views/Demo/page2.st  
<meta charset="utf-8">/views/Demo/page3.st  


/views/Real/indexSectionA.st

<meta charset="utf-8"><meta charset="utf-8">

/views/Real/indexSectionB.st

<meta charset="utf-8">

/views/Real/page2SectionA.st

/views/Real/page2SectionB.st  


/views/Real/page3SectionA.st

As stories were picked up and played and "Real" controllers introduced, the new pages could pick up the shared sub-templates (with styling) and inherit all of Alex's goodness. More and more of the sub-templates were included as more and more functionality delivered.

/static/js/demo.js

/static/css/real-style.css

/controllers/DemoController.cs

/controllers/RealController.cs

/views/Shared/master.st

/views/Demo/index.st

/views/Demo/page2.st

__/views/Demo/page3.st

/views/Real/real-index.st _(uses sub-templates, real.js, real-style.css)_

/views/Real/indexSectionA.st

/views/Real/indexSectionB.st

/views/Real/real-page2.st

/views/Real/page2SectionA.st

/views/Real/page2SectionB.st  


/views/Real/page2SectionB.st

As complexity grew in the "real" controllers and changes in the type of data sent to the sub-templates, the demo controller was brought up to standard so that it could send equivalent data into the view.

The greatest benefit of this living prototype method is that, because the app could be demonstrated working much sooner, it enabled many iterations of feedback before the actual stories had even been played.  This lead to far fewer changes in behaviour at implementation time. Given the chance this is a technique I would definitely use again in the future.

![](https://blogger.googleusercontent.com/tracker/6708525362457359858-5791194520505354170?l=christianralph.blogspot.com)
