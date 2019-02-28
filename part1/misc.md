# Other Things I Learned Along The Way

## Bit Shifting
- you can perform bit shifting in Go quite easily
```
const BigNumber = 1 << 100
const SmallNumber = BigNumber >> 99
```
In the example above, for 'BigNumber' 1 bit is shifted left 100 places, so that it is the number represented in binary as 1 with 100 zeros after it.
Conversely, for 'SmallNumber', we shift 99 spaces back the other way, which should get us just binary 10.

- You can also think of it that '1<<1' is equal to 2
