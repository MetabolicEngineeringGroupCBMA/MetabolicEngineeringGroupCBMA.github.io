---
publish: true
---

<https://github.com/BjornFJohansson/google-python-exercises>

![[Mestrado em Biologia Computacional Molecular e Ambiental/Google-Python-Classesb53y66.png]]

Have a look at the graphic above. The letter `P` is the first element in our list, thus it can be indexed by `0` (see the numbers in the green boxes). The list has a length of `6`, and therefore, the first element can alternatively be indexed by `-6` (negative indexing is shown in the blue boxes).

The numbers in the green and blue boxes identify single _elements_ of the list. Now, look at the numbers in the orange boxes. These determine the _slice indices_ of the list. If we use the slice’s `start` and `stop`, every element _between_ these numbers is covered by the slice. Some examples:

```python
"Python"[0:1] # P
"Python"[0:5] # Pytho
```

That’s just an easy way to remember that the ==start== value is inclusive and the ==end== value is exclusive. [Source](https://bas.codes/posts/python-slicing)
