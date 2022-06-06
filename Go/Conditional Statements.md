## If
```
if x < 0 {
		return sqrt(-x) + "i"
}
```

## ## If with a short statement
Like `for`, the `if` statement can start with a short statement to execute before the condition.
Variables declared by the statement are only in scope until the end of the `if`.

```
if v := math.Pow(x, n); v < lim {
		return v
}
```

## If and else
Variables declared inside an `if` short statement are also available inside any of the `else` blocks.

```
if v := math.Pow(x, n); v < lim {
		return v
} else {
		fmt.Printf("%g >= %g\n", v, lim)
}
```
