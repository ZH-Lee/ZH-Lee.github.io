---
layout: article
title: "Python_TimeComplexity"
categories: python
image:
  feature: python.jpg
  teaser: python.jpg
---

### list
Operation | Average Case | Worst Case|
:-: | :-: | :-:|
Copy    |  O(n)| O(n)|
Append[1]|O(1)|O(1)|
Pop last|O(1)|O(1)
Pop intermediate|O(k)|O(k)
Insert|O(n)|O(n)
Delete Item|O(n)|O(n)
Get Slice|O(k)|O(k)
Extend[1]|O(k)|O(k)
x in s|O(n)|
Get Length|O(1)|O(1)

### dict
Operation | Average Case | Worst Case|
:-: | :-: | :-:|
Copy[2]|O(n)|O(n)
Get Item|O(1)|O(n)
Set Item[1]|O(1)|O(n)
Delete Item|O(1)|O(n)
Iteration[2]|O(n)|O(n)


