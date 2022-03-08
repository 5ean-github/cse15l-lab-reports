## Week 8 Lab Report

[My MarkdownParse repository](https://github.com/5ean-github/markdown-parse)
[Their MarkdownParse repository](https://github.com/BenX-64/markdown-parse)
---
### Test 1
Expected output:
```
[`google.com, google.com, ucsd.edu]
```

![](https://i.imgur.com/kFDOg3O.png)

My output:
![](https://i.imgur.com/GFxZ5I5.png)

Their output:
![](https://i.imgur.com/7sywZJg.png)

---
### Test 2
Expected output:
```
[a.com, a.com(()), example.com]
```

![](https://i.imgur.com/oYPvWXf.png)

My output: ![](https://i.imgur.com/GOkK7di.png)

Their output: ![](https://i.imgur.com/F5e8ZSN.png)

---

### Test 3
Expected output:
```
[https://ucsd-cse15l-w22.github.io/]
```
![](https://i.imgur.com/Edg4Nh2.png)

My output:
![](https://i.imgur.com/PAPhfdS.jpg)

Their output:
![](https://i.imgur.com/D4kwg9l.png)

---
Snippet 1: I think the issue of backticks is more complicated because I have to know whether the `[` or `]` is part of the inline code, and that depends on whether or not `[` comes before `` ` ``.

Snippet 2: I think I can fix the issue of nested parentheses by adding variables that count the numbers of `(` and `)`. I can also fix the issue of escaped characters by detecting if there is a `\` in front of the parentheses and brackets.

Snippet 3: I think I can fix the issue of line breaks by detecting if there are empty lines between `[` and `]` or `(` and `)`.
