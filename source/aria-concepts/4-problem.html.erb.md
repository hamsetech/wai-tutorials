---
title: The Custom Component Problem Solved by ARIA
nav_title: The Problem
order: 4
status: editors-draft
editors:
  - Matt King (Facebook)
  - Judy Brewer: "https://www.w3.org/People/Brewer/"
contributors:
  - The Education and Outreach Working Group (<a href="https://www.w3.org/WAI/EO/">EOWG</a>)
  - The ARIA Working Group (<a href="https://www.w3.org/WAI/ARIA/">ARIA</a>)
support: Developed with support from the <a href="https://www.w3.org/WAI/WCAGTA/">U.S. Access Board, WCAG TA Project, Task 2</a>.
---

## Custom Radio HTML

Consider the following HTML that could be used to replace the HTML radio group in our scenario.

~~~ html
<div id="basic" class="plan-option"><img src="basic.png" alt="Basic"></div>
<div id="plus" class="plan-option"><img src="plus.png" alt="Plus"></div>
<div id="premium" class="plan-option"><img src="premium.png" alt="Premium"></div>
~~~

This HTML contains very little accessibility semantics. 
While there may be JavaScript and CSS behind it that make it possible for some people to choose a plan,
a screen reader user would perceive only the presence of three static images -- not very helpful.

To make this new custom component accessible, it needs:

1. JavaScript and CSS that provide a keyboard interface.
2. ARIA markup that correctly expresses applicable accessibility semantics.

ARIA provides a rich vocabulary for describing the meaning and behaviors of elements to assistive technologies in the same way that semantic HTML does. 
Unlike semantic HTML, though, ARIA does not change the appearance or behavior of the content. 
Thus, when making components with ARIA, developers are responsible for implementing the keyboard interface as well as accurately describing the accessibility semantics with the ARIA markup.

The upside is that ARIA opens the door to creativity and innovation, enabling developers to make all kinds of custom components accessible to people who rely on assistive technologies. 
The following pages illustrate considerations essential to doing so successfully.