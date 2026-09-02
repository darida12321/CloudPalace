**Abc** files are a way of storing music sheets in plain text format. They have a `.abc` extension. Programs exist that can typeset these files into a proper sheet music image, or play it via [[MIDI|MIDI]].

An [[Abc file|abc file]] contains [[Abc information fields|information fields]] and an [[Abc tune body|abc tune body]]. While all the specifics are good to know in general, here is practical example:

```abc
T: Brother Johnes
V:v1 clef=treble octave=0
V:v2 clef=bass   octave=-1
L:1/4
M:4/4
K:C
[V:v1] C D E C | C D E C | E F G2 | E F G2 |
w: Are you sleep-ing Are you sleep-ing, Broth-er John? Broth-er John?
[V:v2] [C4E4G4] | [C4E4G4] | [C4E4G4] | [C4E4G4] |
[V:v1] G F E C | G F E C | C z C2 | C z C2 |]
w: Time for break-fast! Time for break-fast! Please~come on! Please~come on!
[V:v2] [C4E4G4] | [C4E4G4] | z G z2 | z G z2 |]
```

````
```abc
T: Brother Johnes
V:v1 clef=treble octave=0
V:v2 clef=bass   octave=-1
L:1/4
M:4/4
K:C
[V:v1] C D E C | C D E C | E F G2 | E F G2 |
w: Are you sleep-ing Are you sleep-ing, Broth-er John? Broth-er John?
[V:v2] [C4E4G4] | [C4E4G4] | [C4E4G4] | [C4E4G4] |
[V:v1] G F E C | G F E C | C z C2 | C z C2 |]
w: Time for break-fast! Time for break-fast! Please~come on! Please~come on!
[V:v2] [C4E4G4] | [C4E4G4] | z G z2 | z G z2 |]
```
````

The [abcjs](https://docs.abcjs.net/overview/purpose.html) library converts an abc file into a playable sheet. The [[Obsidian ABC Music Notation plugin|obsidian ABC Music Notation plugin]] plugin uses that to display these.

