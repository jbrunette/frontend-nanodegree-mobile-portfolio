Portfolio
==================




Optimizations
======================

Cam's Pizzeria
- Optimizations that reduce number of layout events (http://gent.ilcore.com/2011/03/how-not-to-trigger-layout-in-webkit.html)
  - Optimized changePizzaSizes() to increase speed:
    - Only execute document.querySelectorAll() once to collect pizza container elements
    - Move new width calculations out of for loop as calculation only needs to be performed once
  - Optimized updatePositions() for speed:
    - Only grab scrollTop once, because scrollTop triggersa re-layout
