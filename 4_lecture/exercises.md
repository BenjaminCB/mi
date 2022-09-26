# Exercise 1
### A
```
λ>:{
Prelude| let imp a b | a && b = True
Prelude|             | a && not b = False
Prelude|             | not a && b = True
Prelude|             | not a && not b = True
Prelude| :}
λ>let a = True
λ>let b = False
λ>let c = False
λ>let d = True
λ>(not a) `imp` b
True
λ>((not b) || c) && (d `imp` a)
True
λ>(a `imp` c) `imp` c
True
```

### B
```
λ>let fn a b c = (a || (a `imp` c)) `imp` b
λ>fn True True undefined
True
λ>let fn a b c = (a && ((not b) || c)) && (a `imp` (c `imp` b))
λ>fn True True True
True
```

# Exercise 2
### i
| Event | Prob |
| :---: | :--: |
| t1    | $\frac{1}{12}$ |
| t2    | $\frac{1}{12}$ |
| t3    | $\frac{1}{12}$ |
| t4    | $\frac{1}{12}$ |
| t5    | $\frac{1}{12}$ |
| t6    | $\frac{1}{12}$ |
| h1    | $\frac{1}{8}$  |
| h2    | $\frac{1}{8}$  |
| h3    | $\frac{1}{8}$  |
| h4    | $\frac{1}{8}$  |

$\frac{1}{12} + \frac{1}{8} + \frac{1}{12}$

### ii
```
λ>5/18+1/9+1/9+1/18+1/18+1/18
0.6666666666666667
```

```
λ>let a = 1/18+1/8
λ>let b = 5/18+1/9+1/9+1/18+1/18+1/18
λ>(a * b) / b
0.18055555555555555
```

```
λ>let d6 = 1/18+1/18+1/18
λ>let d4 = 1/8
λ>d6 > d4
True
```

# Exercise 3
- $P(a_1) = 0.20$
- $P(a_2) = 0.40$
- $P(a_3) = 0.40$

Conditionals can be calculated from $P(A | B) = \frac{P(A \wedge B)}{P(B)}$

# Exercise 4

# Exercise 5

# Exercise 6
|      | A=y | A=n |
| :--- | :-: | :-: |
| T=y  |     |     |
| T=n  |     |     |

Roughly $1/100$

# Exercise 7

# Exercise 8
### A
2/9 were H, 7/9 where L, 90% change for good grade for H students, only half L students get a good grade.

prob for getting a good grade
```
λ>2/10*0.9+7/10*0.5+1/10*0.1
0.54
```

prob for H student
```
λ>(2/10 * 0.9) / 0.54
0.33333333333333337
```
