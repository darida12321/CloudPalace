An abc file has the `.abc` extension, and starts with the `%abc` string, and potentially a version number.
It can have a **file header** containing [[Abc information fields|information fields]], followed by one or more **abc tunes**. (If there are multiple tunes, the file is called a **tunebook**.) Tunes have a **tune header** containing [[Abc information fields|information fields]], and a [[Abc tune body|tune body]] which contains the actual notes of the song.

```
%abc-2.1
%%% abc file header
C: composer

%%% abc tune header %%%
X:2      % Identifier
T:Title2 % Title
K:C      % Key
%%% abc tune body %%%
DEF FED:|

%%% abc tune header %%%
X:2      % Identifier
T:Title2 % Title
K:C      % Key
%%% abc tune body %%%
CDE FGa:|
```
