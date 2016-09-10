---
layout: page
title: Rate based Impact Analysis
permalink: /research/rsia/
---

## Problem Definition
What component(s) in a robotic system are affected by a rate change(s)?

## Current Techniques
Current impact analysis techniques generate component a dependency graph (statically or dynamically) and return all reachable components from a change(s) as the set of affected components.

## Rate based Impact Analysis

{% include image.html href="/images/UNL/rsia_architecture.png" url="/images/UNL/rsia_architecture.png" caption=" Architecture of Rate Based Impact Analysis for robotic systems" width=600 align="center" %} 


For each component in the system, we extract outgoing communication channel's rate dependency on its incoming channels. We use this information to label outgoing edges (in)dependent of the incoming rate changes.

<div style="text-align: center;"> 
	<iframe width="400" height="250" src="https://www.youtube.com/embed/lkx_ptR8fL4" frameborder="0" allowfullscreen>
	</iframe> 
</div>

We only explore the dependent edges while exploring the impact of a rate change resulting in a reduced impact set as compared to the current IA techniques.

## Study 
We analyzed three systems Care-O-Bot, PR2, and Water Sampler. For each system, we can reduce impact sets by up to *75%*, *92%*, and *41%*.

<table class=" aligncenter" style="width: 600px;">
<tbody>
<tr>
<th><img src="/images/UNL/cob.png" width="200px" /></th>
<th><img src="/images/UNL/pr2.png" width="200px" /></th>
<th><img src="/images/UNL/h2os.png" width="200px" /></th>
</tr>
<tr>
<th style="text-align: center;"><strong>Care-O-Bot</strong></th>
<th style="text-align: center;"><strong>PR2</strong></th>
<th style="text-align: center;"><strong>Water Sampler</strong></th>
</tr>
</tbody>
</table>


### Approach Implementation
Our implementation of the proposed approach can be found on our [GitHub](https://github.com/unl-nimbus-lab/rsia) handle.

This work is to be presented at [ICRA, 2017](http://icra2017.org). It was partially supported by NSF under awards #1526652 and #1638099 and USDA-NIAF #2013-67021-20947.