---
author: Christian Blunden
comments: true
date: 2011-06-06 02:53:00+00:00
layout: post
slug: circle-triangles-and-squares
title: Circle, Triangles and Squares
wordpress_id: 55887921
---

Simple collaboration game that introduces lean thinking concepts flow, batch size and constraints.

I first introduced this game at Barcamp London 2010 as an abbreviated version of the "dot game" (created by [Allan Shalloway](http://www.netobjectives.com/bio-alan-shalloway), who in turn created it as a cut down version of another game - LSSC Europe 2010).

Setup

book or 2 of post-it notes

3 pens

Watch/Clock/Time keeping device

room + table & chairs

minimum of 5 participants + facilitator (who plays role of customer)

laptop to graph results (or a white board to make them visible)

a pre-prepared sample post-it note containing patterns of Circles Triangles and Squares. (see below)

[![Circles-triangles-squares](http://getfile5.posterous.com/getfile/files.posterous.com/temp-2011-06-06/scrHcpEsJDFkGehuwgpzAlsbbCIqEiefmltGuxbJtvJbJeeeGmIIcaBBGlvC/circles-triangles-squares.JPG)](http://getfile5.posterous.com/getfile/files.posterous.com/temp-2011-06-06/scrHcpEsJDFkGehuwgpzAlsbbCIqEiefmltGuxbJtvJbJeeeGmIIcaBBGlvC/circles-triangles-squares.JPG)

It is important that the circle pattern is easiest to draw, the triangle pattern is most difficult and the square pattern is of medium complexity.

Process

In a straight line, position the 5 workers along the table this will simulate a typical linear work flow. They will be working together to produce a copies of a sample post-it note (prepared The people will perform the following tasks in order:

**1st person** - BA peels post-it notes and passes to second person

**2nd perso**n - draws the circles as shown in the sample and passes to third person

**3rd person** - draws the triangles as shown in the sample and passes to fourth person

**4th person** - draws the squares as shown in the sample and passes to fifth person

**5th person** - acts as Tester (only accepts defect free post-it notes). Hands completed post-it notes to the customer (facilitator) hands defects back to the appropriate person to rework.

A timekeeper starts a stopwatch when the process kicks off and records time of a few key moments.

1. Start time

2. Time until first batch is completed (cycle time)

3. Time until total work is complete (lead time)

4. Total number of defects

5. Total number of completed post-its

6. Number of incomplete post-its along the production line (work in progress)

The process is run 3 times, preferably with different people or at least with people in different roles so as not to get accustomed to the work. I cap each round to a maximum of around 5 minutes. The goal is to get 30 defect free post-it notes delivered.

Cycle 1

Process is run with a batch size of 10. Which means that the 1st person peels 10 post it notes before passing the 10 post it notes to the 2nd person, who completes all 10 circles before passing on to the 3rd person... and so on down the line. Ensure that the 1st person keeps **pushing** work down the line, even though he has peeled 30 post-it notes, this is typical production like behaviour. Facilitator needs to _enforce activity_, "we don't want people idle" "we are paying you to work, not sit around"

After the round has finished, record and display results and discuss the observations as a group. Typical observations and discussions:

  * Piles of work forming in front of 3rd person (triangles) - This represents a bottleneck. What are the parallels in software?
  * Large amounts of work in progress - This represents Inventory and cost, and potential waste. What are the parallels in software?
  * Chaos and mayham. Lack of communication
  * Batch size. Where do we batch work in software? (releases, analysis, UAT, "projects")
  * Lead time / cycle time. What is this in software? Are long lead times bad? What are the implications of long lead times?
  * People will be idle (the tester and Square drawer will be starved of work)

Cycle 2

Process is run again with a batch size of 1. Which means 1st person peels a single post-it note and hands it to the 2nd person who draws the single circle and passes onto the 3rd person and so on. As before, we enforce activity. Work is **pushed **down the line from the rate the BA can peel post it notes.

Again the results are recorded and displayed and observations discussed. Typical observations include:

  * Bottlenecks remain although piles of work are less. Discuss how this could be improved (limit the rate of work pushed into system and/or pull work)
  * Less work in progress
  * Less Chaos and potentially more communication
  * Lead time will reduce (cycle time will stay the same)
  * People will still be starved of work
  * more units completed
  * Tester will see more completed post-it notes and can give more feedback to workers. Defects will decrease (slightly)

Cycle 3

Process is run for a final time again with a batch size of 1 although work is now **pulled **as necessary. Which means the 1st person will not peel another post-it note until the 2nd person requires it, and the 2nd person will only pass the post-it down the line when the 3rd person (the constraint) requires it. This effectively ties the rate of production to the rate the constraint can produce. Also it is time to build quality into the system, the team now re-positions to form a square, rather than a straight line. The tester becomes a QA and monitors each work step for quality providing feedback immediately upfront rather than at the end.

Again the results are recorded and displayed and observations are discussed. Typical observations include:

  * No piles of work in front of triangle worker
  * Work in progress dramatically decreases (costs decrease)
  * Number of completed post-its goes up
  * Lead time dramatically drops
  * Less defects
  * People are not working as hard but more effectively. Yet more work gets done more quickly and cheaper! (Paradox)
  * More collaboration.
  * Pull verse pushing work. Automatically adjusts the rate of production to the slowest member (the constraint)
  * Benefits of Economies of flow (doing one piece effectively) verse Econoomies of scale (batching work)
