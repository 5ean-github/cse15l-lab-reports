Code 1:

![](https://i.imgur.com/BbKZJGP.png)

[Test file 1](https://github.com/5ean-github/markdown-parse/blob/main/test-file3.md)

Symptom 1:

![](https://i.imgur.com/kW021Ap.png)

This bug happens when there is no open brackets in the markdown file because `nextOpenBracket` will be `-1`. The symptom of this code is that there will be an `IndexOutOfBoundException`. To fix this, there should be an if statement in the program to check whether there exists `[`.

---

Code 2:

![](https://i.imgur.com/ah1ggzs.png)

[Test file 2](https://github.com/5ean-github/markdown-parse/blob/main/test-file3.md)

Symptom 2:

![](https://i.imgur.com/OI25VEN.png)

This bug is similar to the last problem, and the failure-inducing input is the same. When there is no open brackets in the markdown file, it should throw an error instead of returning empty arraylist. 

---
Code 3:

![](https://i.imgur.com/D44RFTy.png)

[Test file 3](https://github.com/5ean-github/markdown-parse/blob/main/test-file2.md)

Symptom 3:

![](https://i.imgur.com/6N6EGO8.png)

This bug happens when there are image links in the markdown file. The symptom is that it will also return the links of the images. In order to fix it, the program should also check if there is `!` before the brackets.
