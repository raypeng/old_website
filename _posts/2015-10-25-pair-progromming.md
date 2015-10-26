---
layout:   post
title:    "Code Review << Pair Programming"
date:     2015-10-25
categories: [reflections]
---

There was this system anamoly we were trying to make sense of. The algorithm didn't perform properply as we expected. After much debugging, you know, setting trace points and adding a bunch of print statements, we finally discovered the bug came from a wrongful assumption that the data matrix comes in our wanted format while in reality 2 of its columns should really be swapped before feeding into the algorithm.

After this "magnificent" discovery, we were talking among ourselves that this bug was too hard to trace which even survived 2 rounds of peer code reviews. We wish we had adopted the pair programming approach, where ideally we would question every assumptions we made before writing the code down. Bugs might be easier to identify in real world software products yet not in this research context. There are simply too many "swapping columns" and "1-indexed vs 0-indexed" like tiny points to reason about that we easily slip our minds and leave behind a "magnificent" bug. Yet with this slipping probability `p` and with 2 developers working on coding as a pair, it is drastically harder to produce the bug -- the probability drops from `p` to `p^2`.

So, lessons learned: either reduce the slipping probability `p` (which is inherently hard) or find yourself another developer as your pair.
