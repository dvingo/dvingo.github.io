---
layout: post
title: "Infinite Canvas"
date: 2015-09-12 12:15:00 -0500
---
An infinite grid web app where all users are interacting with the same page and can contribute
certain kinds of web content (images, movies, text, links, etc).
The inspiration is from word squared: [http://www.wordsquared.com/](http://www.wordsquared.com/)
and more info [here](http://startupmonkeys.com/2010/09/02/building-a-scrabble-mmo-in-48-hours/).

Users can pan and zoom, clicking let's you interact with the content, secondary-click (right-click),
opens a menu of actions.

Some actions would be:

- paste a url to an image to appear in the grid.
- paste a website url to be displayed in an iframe–zoomed out to keep a high level view).
- you could zoom in and out of a website in an iframe.
- zoom in and out of areas of the map
- mini-map to show larger areas of the grid zoomed out.
- inline content from APIs.

One constraint I think will add more interest to the discovery process would be to
not allow "teleporting" around the map, instead forcing people to pan across with a capped
max zoomed out level.
This would force people to choose one direction to discover, and only that direction. You would necessarily
not be able to view any other area of the universe of content, which will make each area of the map
unique with the expected result of "pockets" of content that appear. It would be akin to a visual hive-mind.

Some things to think about are if you would allow people to overwrite other people's content, or
if you are forced to expand into new areas, more like scrabble. Even though not allowing teleporting
might be interesting, teleporting is essentially just linking, which would be annoying if you couldn't
link to certain areas. With linking to specific coords, you could coordinate a group of people to
all saturate a certain area of the grid. With teleporting there would be more likelihood of islands
of content being created also.

# Implementation thoughts
As mentioned in the word squared writeup, the design would be based on a database with
geospatial indexes and querying support, allowing you to query by a person's current
coordinates to show the proper content (and also link to a coordinate).
