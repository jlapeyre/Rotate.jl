# Rotate

###   @rotate(x_1, x_2, ... x_n)

Rotate the values referred to by `x_i`.

Assign `x_2` to `x_1`, `x_3` to `x_2`, ..., and `x_1` to `x_n`.
Each argument is interpreted as the left hand side of an assignment.

`@rotate` is equivalent to `(x_1, x_2, ..., x_n) = (x_n, x_1, ..., x_{n-1})`

Compare to `circshift`.

## Example
```julia
@rotate(x, y, a[2])
```
