# SourceCodeMiniature
<img src=images/demo.png align=right>Creates a miniature visualization of indented source code

This html file with embedded javascript creates a fake source code miniature look-alike visualization like shown in the image at the side.

Each line of source code will be represented by a 1 pixel line in the output. The lines are separated by a 1 pixel horizontal space. The length of the lines and the indention is randomized. 

The output can be tweaked by the following parameters in the html file.
```
min=5 
max=80
extendedmax=250
maxThreshold=0.01

LOC=1200

IndentStep=2
IndentionFactor=1/3 // normal = 1/3; 0..1
```

max and min is the mininmal / maximal line length, extendedmax will be used, when a random number in the range of 0..1 is beneath maxThreshold.

The number of lines in the output can be changed with the LOC parameter. If the indention level of the last line is not 0, lines will be added until the indention level is 0. So finally the number of lines can greater then the LOC parameter.

The IndentionStep specifies the number of pixel to be used for each indent. The IndentionFactor defines the probability of doing and indention or not. The normal value is 0.33 (1/3) for getting no indention (-> 1/3 positive indention, 1/3 negative indention), the greater the value the less indention in both directions