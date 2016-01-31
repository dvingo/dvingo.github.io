---
layout: post
title: "Read large works in chunks"
date: 2016-01-31 1:39:21 -0500
---
# Idea

An email subscription service that helps you read long form publications
by sending you small snippets each day, or at some other regular interval.

The idea came about from thinking about how quite a few humans only consume
small chunks of text and less and less read long format books or magazines.
Another motivation was the desire to read more of the "classic" works, but
realizing that many of them are very dry and it could help make them
easier to consume if broken up into more manageable chunks.

# Implementation

A web service would consume the ASCII version of books from
[Project Gutenberg](https://archive.org/details/gutenberg) and store them
in a db or just on a filesystem.

A web form allows people to enter their email address and select a book to read.
Perhaps you can add multiple books to read multiple books at the same time.
There will be a relation of email address to book subscription which
would keep track of that user's offsets into the books's text files.
