This is how you specify the actual notes and their timing in [[Abc notation|abc notation]]. More information can be found [here](https://abcnotation.com/wiki/abc:standard:v2.1#the_tune_body).

```abc
T:Pitch
L: 1/4
F, G, A, B, C D E F G A B c d e f g a b c' d' e' 
w: F, G, A, B, C D E F G A B c d e f g a b c' d' e' 
```
```abc
T:Accidentals and Chords
L: 1/4
^^B ^B B _B __B | [CEG] [CFA]
w:^^B ^B B \_B \_\_B | [CEG] [CFA]
```
```abc
T:Note (B) and Pause (z) lengths
L: 1/4
B/4 B/2 B B2 B4 | z/4 z/2 z z2 z4
w: B/4 B/2 B B2 B4 z/4 z/2 z z2 z4
```
```abc
T:Beams made by notes without space
L: 1/8
BB B/2B/2B/2B/2 B>B
w:B B B/2 B/2 B/2 B/2 _ B>B
```
```abc
T: Repeats, bars
L:1/4
B B |[1 B B :|[2 B B [| B B :: BB |]
w: _ \|[1 _ :\|[2 _ [\| _ :: _ \|] 
```
```abc
T: Symbols
L:1/4
(B B (B B) B) | (3B B B | .B ~B HB LB MB OB PB SB TB uB vB
w: (B B (B B) B) | (3B B B | . \~ H L M O P S T u v 
```
```abc
T: Decorations
L:1/4
!<(!B !<)!B | !>(!B !>)!B | "Cm"[CEG]
w:!<(! !<)! | !>(! !>)! | "Cm"[CEG]
```
