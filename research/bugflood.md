---
layout: page
title: BugFlood - A bug inspired algorithm for efficient path planning in an obstacle rich environment
permalink: /research/bug-flood/
---

**Timeline:** (May, 2015 – Present)

**Contributors:** _Nishant Sharma, Shivam Thukral_, _Sandip Aine_, _Jose Pinto_, and _Dr. P. B. Sujit_

<hr style="clear:both;visibility: hidden;" />

## Abstract

We present a path planning algorithm inspired by the bug algorithm to quickly compute paths in an obstacle rich environment (or to report that no such path exists). In our approach, upon sensing an obstacle the bug  splits into two bugs exploring the obstacle boundary in opposite directions, until the bugs find the goal in the line-of-sight. Then the bug leaves the obstacle and moves towards the goal. The process of splitting one bug into two, following the obstacle boundary and moving towards the goal continue until a bug reaches the goal. As the bugs flood the environment due to splitting, we call the algorithm -- BugFlood. The exploration creates a binary tree structure through which paths can be determined from the source to the goal. The algorithm is simple  to implement and it rapidly finds a solution if one exists. We provide worst case bounds on the path length, show that the algorithm has provable guarantees on convergence and develop heuristics to minimize the number of active bugs in the environment. We compare the performance of our algorithm with different planners from open motion planning library (OMPL) and visibility graph methods. The results show that BugFlood delivers lower cost paths compared to other planner with lower computational time and rapidly indicates if a path does not exist. 

## Resources


{% include image.html href="/images/IIITD/bug_flood.png" url="/images/IIITD/bug_flood.png" caption="<b>Bug_Flood finds a solution: </b>The bug splits into two bugs
(B1 and B2) at the hit point H traveling in opposite directions exploring the obstacle. The bug B2 detects the goal after exploring the obstacle, while B1 splits into B3 and B4 after detecting another obstacle. The bug B4 detects the goal. If B4 reaches earlier than B2 then the shortest is from the path B4 − B1, otherwise B2 is the shortest path. The simulation stops once a bug reaches the T ." width=350 align="right" text-align="justify" %} 

{% include image.html href="/images/IIITD/bug_pcom.png" url="/images/IIITD/bug_pcom.png" caption=" <b>Traditional Pcom BUG algorithm failing scenario: </b>The bug uses default strategy of moving left upon detecting an obstacle. As the bug hits every obstacle can turns left, it never reaches the goal T goes into infinite loop." width=350 align="left" text-align="justify" %} 

<hr style="clear:both;visibility: hidden;" />

**Source Code:**
<a href="https://github.com/{{ site.github_username }}/Path_Planning">
  <span class="icon  icon--github">
    <svg viewBox="0 0 16 16">
      <path fill="#828282" d="M7.999,0.431c-4.285,0-7.76,3.474-7.76,7.761 c0,3.428,2.223,6.337,5.307,7.363c0.388,0.071,0.53-0.168,0.53-0.374c0-0.184-0.007-0.672-0.01-1.32 c-2.159,0.469-2.614-1.04-2.614-1.04c-0.353-0.896-0.862-1.135-0.862-1.135c-0.705-0.481,0.053-0.472,0.053-0.472 c0.779,0.055,1.189,0.8,1.189,0.8c0.692,1.186,1.816,0.843,2.258,0.645c0.071-0.502,0.271-0.843,0.493-1.037 C4.86,11.425,3.049,10.76,3.049,7.786c0-0.847,0.302-1.54,0.799-2.082C3.768,5.507,3.501,4.718,3.924,3.65 c0,0,0.652-0.209,2.134,0.796C6.677,4.273,7.34,4.187,8,4.184c0.659,0.003,1.323,0.089,1.943,0.261 c1.482-1.004,2.132-0.796,2.132-0.796c0.423,1.068,0.157,1.857,0.077,2.054c0.497,0.542,0.798,1.235,0.798,2.082 c0,2.981-1.814,3.637-3.543,3.829c0.279,0.24,0.527,0.713,0.527,1.437c0,1.037-0.01,1.874-0.01,2.129 c0,0.208,0.14,0.449,0.534,0.373c3.081-1.028,5.302-3.935,5.302-7.362C15.76,3.906,12.285,0.431,7.999,0.431z"/>
    </svg>
  </span>
  Path Planning. 
</a>

**Note:** The above resource expects a convex environment as input. A newer object-oriented implementation of the proposed path planner that handles non-convex environments will be released soon. 

## Publications

* *N. Sharma*, Jose Pinto, and P. B. Sujit, **[“BugFlood: A bug inspired algorithm for efficient path planning in an obstacle rich environment,”](/research/bug-flood/)** in *AIAA Infotech @ Aerospace, AIAA SciTech Forum*, San Diego, California, USA, Jan, 2016.

### Under Review

* N. Sharma, S. Thukral, S. Aine, and S.P. Baliyarasimhuni, **[“A fast path planning algorithm using bug splitting technique,”](/research/bug-flood/)** at *Autonomous Robots, 2017*.
