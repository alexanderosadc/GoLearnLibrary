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

## Switch
 Important difference between other languages and Go's switch cases need not be constants, and the values involved need not be integers.
```
switch os := runtime.GOOS; os {
	case "darwin":
		fmt.Println("OS X.")
	case "linux":
		fmt.Println("Linux.")
	default:
		// freebsd, openbsd,
		// plan9, windows...
		fmt.Printf("%s.\n", os)
	}
```

### Switch with no condition
Switch without a condition is the same as `switch true`.

```
t := time.Now()
	switch {
	case t.Hour() < 12:
		fmt.Println("Good morning!")
	case t.Hour() < 17:
		fmt.Println("Good afternoon.")
	default:
		fmt.Println("Good evening.")
	}
```
