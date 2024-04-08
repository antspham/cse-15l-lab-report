1a. cd with no arguments
```
C:\Users\Anthony>cd
C:\Users\Anthony
```
I got this output because the cd command would move me to the argument given but since no argument was given I remained in the same directory meaning this output was not an error.

1b. dir with no arguments
```
C:\Users\Anthony\Downloads>dir
04/06/2024 05:06 PM 117,626,141 Calculus_Early_Transcendentals_Jon_Rogawski_4th.pdf
```
I got this output because the dir command lists all the files and folders in the current directory meaning this output was not an error.

1c. type with no arguments
```
C:\Users\Anthony>type
The syntax of the command is incorrect
```
I got this output because the type command requires an argument.
No argument makes this output an error.

2a. cd with a path to a directory as an argument
```
C:\Users\Anthony>cd Downloads
C:\Users\Anthony\Download>
```
I got this output because the cd command along with a directory as an argument will move me to that directory meaning this output was not an error.

2b. dir with a path to a directory as an argument
```
C:\Users\Anthony>dir Downloads
04/06/2024 05:06 PM 117,626,141 Calculus_Early_Transcendentals_Jon_Rogawski_4th.zip
04/06/2024 05:06 PM 124,052,691 Calculus_Early_Transcendentals_Jon_Rogawski_4th.pdf
```
I got this output because the dir command along with a directory as an argument will list the contents of that directory meaning this output was not an error.

2c. type with a path to a directory as an argument
```
C:\Users\Anthony>type Downloads
Access is denied.
```
I got this output because the type commands displays the contents of a file
This output is an error because Downloads is a directory when a file argument is required making this output an error.

3a. cd with a path to a file as an argument
```
C:\Users\Anthony\Downloads>cd Calculus_Early_Transcendentals_Jon_Rogawski_4th.pdf
The directory name is invalid
```
I got this output because the cd only takes directory as arguments.
A file was used as an argument when a directory was required making this an error.

3b. dir with a path to a file as an argument
```
C:\Users\Anthony\Downloads>dir Calculus_Early_Transcendentals_Jon_Rogawski_4th.pdf
04/06/2024 05:06 PM 124,052,691 Calculus_Early_Transcendentals_Jon_Rogawski_4th.pdf
```
I got this output because it listed the file I specified as the argument so this output was not an error.

3c. type with a path to a file as an argument
```
C:\Users\Anthony\Downloads>type Calculus_Early_Transcendentals_Jon_Rogawski_4th.pdf
%Γπ╧╙1.6
<</DecodeParms<</Columns 5/Predictor 12>>/Filter/FlateDecode/ID[<1319B96C3AB5485BB432209F093CFABB><1309F50F3F6540849A06C570FCBBB05C>]/Index[28223 21]/Info 28222 0 R/Length 72/Prev 124014088/Root 28224 0 R/Size 28244/Type/XRef/W[1 3 1]>>stream
<</Filter/FlateDecode/I 17187/L 17171/Length 10559/O 17133/S 15758/V 17149>>stream
h▐∞zwX╙W≈°ç◄2H !        {äí2¶♥Ig♥       S╘►☻"ZM↑εjÉ◄på)╬åσ¬¡áα¬VPh╡uÇ╕W◄⌐Z╦H░8¬VP¼┌Wδ≈▄Σ‼⌠}▀τyƒτ≈▀∩☼½==√₧sε╣τ▐Oƒ`↑f
ε1╥²$Oτ╛»▼ìñH½n·╤≈à∟\Dë▀╢ _>≈Tt╝<U░╛æ≥}├d?V1╟.n«Θíè≥uò?~ß3¢¶↨δ╖={ΓΦèε*ƒây▓>÷╧3ª$♠╠MM£▲@·¬╢} w☺δ╬┤T.J╗σEêOL¶°ePÆ7OìôKÆσ╧+♥ï╢y4╓e╞╝«▄ÑÉ\¬¼╦ô╝«?αwK├╛ûr⌡\S▒╧ö=u╫=σà╒Ob4E£☺mU█▒╧┼T>»⌐╔ë#≈ÄúHO↕bΣ╜¼Zƒÿ╞ô╫º⌂ε└V╞┼<╫4.▓╢α‼Γ∩6E↔╚ñ╝hë⌠ëæ^[αwgï≤üÿ¡àòu╦)w)╬≤BΩû┼▲-Z
```
I got this output because the type command shows the contents of the argument if it is a file.
This is not an error but the command prompt is just unable to show the contents because it is a pdf.
