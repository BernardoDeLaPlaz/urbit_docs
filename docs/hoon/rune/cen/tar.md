---
navhome: /docs/
next: true
sort: 7
title: %* "centar"
---

# `%* "centar"`

`[%cntr p=wing q=hoon r=(list (pair wing hoon))]`: make
with arbitrary hoon.

## Expands to

```
=+  q
%=  p
r
```

## Syntax

Regular: *2-fixed*, then *jogging*.

## Discussion

`%*` makes a limb from a hoon, with changes. It's useful when you want
evaluate a hoon, pull out a single limb from the result,
and then change some parts of the limb before using it.

## Examples

```
~zod:dojo> %*($ add a 2, b 3)
5
~zod:dojo> =foo [a=1 b=2 c=3 d=4]
~zod:dojo> %*(+ foo c %hello, d %world)
[b=2 c=%hello d=%world]
~zod:dojo> =+(foo=[a=1 b=2 c=3] foo(b 7, c 10))
[a=1 b=7 c=10]
~zod:dojo> %*(foo [foo=[a=1 b=2 c=3]] b 7, c 10)
[a=1 b=7 c=10]
```
