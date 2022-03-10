## Lab Report 5

---
### Test 490
```
[link](<foo
bar>)
```
My output: 
```
[<foo
bar>]
```
ucsd-cse15l-w22's output:
```
[]
```

I manually searched through to find this test case. For this test, my output is incorrect, but ucsd-cse15l-w22's input is correct. In order to fix my bug, I think I need to check if any element in `toReturn` contains `\n`. If it does, then I have to remove it from `toReturn`

---
### Test 485
```
[link](<>)
```
My output:
```
[<>]
```
ucsd-cse15l-w22's output:
```
[<>]
```

I manually searched through to find this test case. For this test, both mine and ucsd-cse15l-w22's outputs are incorrect, and the correct output should be `[]`. In order to fix my bug, I think I need to check if any element in `toReturn` contains `<` and `>` around it. If it does, then I have to remove `<` and `>` from that element in `toReturn`.
