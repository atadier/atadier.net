---
title: This is the test article
date: 2023-09-09
updated: 2023-10-09
---

It's a test article.
<!-- more -->

This is the content of the article. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim [veniam](https://github.com), quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

- One
- Two
- Three

1. One
2. Two
3. Three

```py,linenos
def __length(T, depth = 0):
    """
    (sum, count) of word lengths
    return type: (int, int)
    """
    s = 0
    count = 0
    if T.key[1]:
        s = depth
        count = 1
    
    for child in T.children:
        a, b = __length(child, depth + 1)
        s += a
        count += b
    
    return (s, count)
```