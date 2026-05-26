The **two's complement** representation stores [[Signed integer representation|signed integers]] by flipping (**complementing**) positive numbers to get negative ones, and adding one. 1 byte can store numbers between `-128` and `127`.
- ` 6`: `00000110` 
- `-6`: `11111010`

This is the most widely used [[Signed integer representation|signed integer]] representation because doing arithmetic on these is the same as doing arithmetic on [[Unsigned integer representation|unsigned integers]].

One consequence of this representation is that when a number grows too large, the magnitude can overflow to the sign bit. This is called an **integer overflow**.

