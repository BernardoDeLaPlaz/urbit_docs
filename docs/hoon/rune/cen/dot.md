---
navhome: /docs/
next: true
sort: 3
title: %. "cendot"
---

# `%. "cendot"` 

`[%cndt p=hoon q=hoon]`: call a gate (function), reversed.

## Expands to

```
%-(q p)
```

## Syntax

Regular: *2-fixed*.

## Examples

```
~zod:dojo> =add-triple |=([a=@ b=@ c=@] :(add a b c))
~zod:dojo> %.([1 2 3] add-triple)
6
```

