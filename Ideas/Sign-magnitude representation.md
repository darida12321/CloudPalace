The **sign-magnitude** representation stores [[Signed integer representation|signed integers]] by using the most significant bit as the sign. 1 byte can store numbers between `-127` and `127`.
- ` 6`: `00000110` 
- `-6`: `10000110`

There are a few problems with this:
- 0 is represented in two different ways (-0 and 0)
- Addition and subtraction requires extra logic for negative numbers.
- Comparison requires inspecting the sign bit

