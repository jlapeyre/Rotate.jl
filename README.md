# Rotate

### @rotate(x_1, x_2, ... x_n)

Rotate the values referred to by `x_i`.

Assign  the value of `x_1` to `x_2`, `x_2` to `x_3`, ..., and `x_n` to `x_1`.
Each argument is interpreted as the left hand side of an assignment.

`@rotate` is equivalent to `(x_1, x_2, ..., x_n) = (x_n, x_1, ..., x_{n-1})`

Compare to `circshift`.

## Example
```julia
julia> using Rotate

julia> x = 1; y = 2; z = 3; a = [4, 5]; (x, y, z, a[1])
(1, 2, 3, 4)

julia> @rotate(x, y, z, a[1]); (x, y, z, a[1])
(4, 1, 2, 3)
```

### @rotaten(n, x_1, x_2, ... x_n)

Like `@rotate`, but rotate by `n`, where `n` is an integer.
Use `n = -1` for circular shift left.

