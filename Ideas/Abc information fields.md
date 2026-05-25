Information fields in [[Abc notation|abc notation]] contain data regarding everything surrounding the song. 

##### Minimal example
The `X` (reference number; first), `T` (title; second) and  `K` (key; last) fields are required.
```abc
X:2                       % Reference number
T:Example without fields  % Tune title
K:C                       % Key
CCCC |CCCC|
```


<br>
<br>

##### Detailed example
Everything else is optional. A full list can be found [here](https://abcnotation.com/wiki/abc:standard:v2.1#information_fields).
```abc
X:1                    % Reference number
T:Example with fields  % Tune title
R:hornpipe             % Rhythm
C:Daniel Mihalik       % Composer
O:Englang; Oxford.     % Origin
P:ABAB                 % Parts
G:flute                % Group, (mostly for databases)
% 
B:Daniel's songbook         % Book
D:Daniel's CDs              % Discography
S:Obtained while writing    % Source
F:https://google.com        % File
N: Transcribed in obsidian  % Notes
Z: Daniel Mihalik           % Transcription
H:I decided to write this   % History
%
M:4/4          % Meter
L:1/4          % Unit note length
Q:1/2=120      % Tempo
V:ID1          % Voice (like key)
K:C clef=bass  % Key (e.g.: C#, F#m, BDor, ...)
[V:ID1][P:A]CCCC |[P:B]CCCC|
w:words to sing  % Words
```
<br>
<br>

##### Syntax
And here is how it looks as plain text. `%` are comments. Fields can continue on another line by using `+:`. Information fields can be placed in the body by `[name:value]`.

```
X:1                    % Reference number
T:Example with fields  % Tune title
R:hornpipe             % Rhythm
C:Daniel Mihalik       % Composer
O:Englang; Oxford.     % Origin
P:ABAB                 % Parts
G:flute                % Group, (mostly for databases)
% 
B:Daniel's songbook         % Book
D:Daniel's CDs              % Discography
S:Obtained while writing    % Source
F:https://google.com        % File
N:Transcribed in obsidian   % Notes
Z:Daniel Mihalik            % Transcription
H:I decided to write this   % History
%
M:4/4          % Meter
L:1/4          % Unit note length
Q:1/2=120      % Tempo
V:ID1          % Voice (like key)
K:C clef=bass  % Key (e.g.: C#, F#m, BDor, ...)
[V:ID1][P:A]CCCC |[P:B]CCCC|
w: words to sing  % Words
```

Key (`K`) and Voice (`V`) fields can specify clef information.
- `clef=treble`: What clef to use (`treble`, `bass`, `tenor`, `alto`)
- `middle=B`: Where to put the clef.
- `transpose=0`: For playback, transpose the score by n semitones.
- `octave=0`: Raise or lower the music code.
- `stafflines=5`: The number of lines.












